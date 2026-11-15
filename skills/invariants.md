---
title: "Bất Biến Chung (Shared Invariants)"
status: skeleton_structural_prefilled
---

# 🔒 Bất Biến Chung — MỌI skill phải tuân thủ

> Pre-fill từ blueprint đã duyệt + `money-gemini/AGENTS.md`. Đây là hàng rào chống drift. Chi tiết engine/port: xem `PLAN.md`.

## 1. Zero-hallucination (số liệu)
- **KHÔNG** tự tính `available_balance`, `net_debt`, `remaining_cb_cap`, `final_price`, lãi, cashback bằng suy luận.
- **LUÔN** gọi kernel (RPC / SQL view) để PostgreSQL tính deterministic. Agent chỉ đọc kết quả.

## 2. Một cổng ghi duy nhất
- Mọi txn đi qua kernel `submit_agent_txn` (append-only ledger). Không ghi thẳng DB từ skill.
- Mỗi ghi có **idempotency key** + **correlation id** + **rule_snapshot_hash**.

## 3. Hai cycle tag — KHÔNG trộn
| Tag | Phạm vi | Dùng cho |
| :--- | :--- | :--- |
| `persisted_cycle_tag` | Card billing | Cashback, sao kê thẻ, batch trả nợ |
| `debt_cycle_tag` | Person debt / Sheet | Nợ person, rollover, sync sheet |

## 4. Family card & headroom
- Hạn mức chia sẻ theo **root** (`parent_id ?? id`). Thẻ con `credit_limit=0` → dùng `effective_shared_limit` của root.
- Headroom tính trên tổng chi tiêu cả family, không riêng thẻ con.

## 5. Batch transfer — 2 mode
- `DIRECT_CARD_PAY` (`cleared_account_id IS NULL`): tiền vào thẳng thẻ → khôi phục `available_balance` ngay.
- `LINKED_BANK_WAIT_DEBIT` (`cleared_account_id IS NOT NULL`): tiền vào bank liên kết → chờ auto-debit mới clear.
- **`BATCH_CLEARING_ID` = `88888888-9999-9999-9999-888888888888`** — chỉ khai báo trong kernel constants.
- **`SERVICE_PENDING_ID` = `77777777-8888-8888-8888-777777777777`** — ví kỹ thuật chờ xử lý.

## 6. Cashback
- Rate / cap / min_spend / MCC lấy từ **DB** (`cashback_rules`, `cashback_type_configs`), KHÔNG hardcode trong `.ts`.
- Phân biệt **estimated** vs **`real_awarded`** (thực nhận). FX fee deferred bị loại trừ khỏi cashback.
- Cumulative cap duyệt ASC; `min_cycle_spend` chưa đạt → cashback = 0 (theo engine).

## 7. MD là projection 1 chiều
- `accounts/`, `people/` sinh **1 chiều từ DB** (read-only). Không sửa tay MD generated rồi coi là source of truth.
- Rule chi tiết thẻ pre-fill từ link ngân hàng → ghi vào DB trước, MD regenerate sau.

## 8. Sheet projection
- Google Sheets là **projection** qua outbox + retry. GAS `Code.js` v25 giữ nguyên, deploy `clasp push`.
- Sau FULL_SYNC phải verify ARRAYFORMULA.

## 9. Bảo mật & dữ liệu
- **KHÔNG** dùng production `service_role` key. Migration dùng scoped export credential (read-only).
- **KHÔNG** commit `.env.local`, secret, passcode. Repo nên để **private** (chứa số TK, tên người nhận).
- Notes copy **nguyên văn**; resolve ngày tương đối ("hôm qua") → ngày tuyệt đối trước khi ghi.
- **KHÔNG** auto-submit / auto-send: batch, refund, adjustment luôn cho user review trước.

## 10. Quy trình repo
- 1 sprint = 1 branch = 1 PR. Branch slug mô tả việc (không prefix `feat/`/`fix/`).
- File xóa → `.archive/<sprint-slug>/` kèm header `@archived` trước khi `git rm`.
- Sau mỗi bước: build/test kernel trước khi sang bước kế.