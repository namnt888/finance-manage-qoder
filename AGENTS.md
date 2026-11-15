# finance-manage-qoder — Agent Rules

> Repo Agent-First / Zero App-Code. **SCAFFOLD** — chưa implementation. Mọi agent đọc file này trước khi làm việc.

## Đọc theo thứ tự
1. [`PLAN.md`](PLAN.md) — phase hiện tại, bước tiếp theo, gate, anti-drift.
2. [`skills/invariants.md`](skills/invariants.md) — bất biến chung (BẮT BUỘC).
3. [`docs/architecture/agent-first-blueprint.md`](docs/architecture/agent-first-blueprint.md) — kiến trúc đã duyệt.
4. `docs/knowledge/<doc>.md` liên quan (port từ money-gemini; chưa port thì đọc bản gốc read-only).
5. `skills/<skill>/SKILL.md` của tác vụ.

## Nguyên tắc cứng
- **Zero-hallucination:** KHÔNG tự tính balance/debt/cashback/lãi — gọi kernel RPC/view.
- **Một cổng ghi:** mọi txn qua `submit_agent_txn` (append-only + idempotency + correlation id).
- **No hardcode:** bank name/code/rate → DB/config. `BATCH_CLEARING_ID` `88888888-9999-9999-9999-888888888888` chỉ trong kernel constants.
- **2 cycle tag:** `persisted_cycle_tag` (card) ≠ `debt_cycle_tag` (person/sheet) — không trộn.
- **MD projection 1 chiều:** sửa rule → DB trước → regenerate MD. Không sửa tay MD generated.
- **Không auto-submit:** batch/refund/adjustment luôn cho user review.
- **Bảo mật:** không production `service_role`; không commit `.env.local`/secret; repo private.

## Kiến trúc (tóm tắt)
| Tầng | Vai trò | Vị trí |
| :--- | :--- | :--- |
| Agent + Skills | Reasoning, routing, gọi tool | `skills/` |
| MCP Kernel | Cổng ghi/đọc, giữ credential | `kernel/mcp` (TODO) |
| Engine | Cashback/balance/debt deterministic (port `cashback.pure.ts`) | `kernel/engine` (TODO) |
| Neon Ledger | Append-only + SQL views + RPC | `db/` (TODO) |
| Projection | Google Sheets (GAS v25) + Obsidian + MD | `dashboards/`, `accounts/`, GAS |

## Commands (TODO — kernel chưa tạo)
- Kernel CLI: `python3 scripts/neon_cli.py ...` (P2)
- Batch: `python3 scripts/batch_xlsx.py inspect|generate` (P3)
- Build/test engine: `pnpm build` / `pnpm test` (P3, sau khi port)

## Workflow
1. Xác định phase/sprint trong `PLAN.md`. Không làm việc ngoài phase hiện tại (anti-drift).
2. **1 sprint = 1 branch = 1 PR** (base `main`). Slug mô tả việc, không prefix `feat/`/`fix/`.
3. Gate không đạt = DỪNG + rollback, không đi tiếp.
4. Sau mỗi bước: build/test kernel trước khi sang bước kế.
5. File xóa → `.archive/<sprint-slug>/` kèm header `@archived` trước khi `git rm`.

## Nguồn sự thật & ranh giới
- `money-gemini` (sibling): DB schema + engine + knowledge — **read-only reference**, không sửa khi làm việc ở repo này.
- `finance-manage-ag` (sibling): draft — **read-only, không touch**. Reuse asset có kiểm chứng.
- Repo này là nơi **thực thi** kiến trúc mới.

## Domain knowledge
Xem [`docs/knowledge/_INDEX.md`](docs/knowledge/_INDEX.md) — bridge 22 docs nghiệp vụ (đang chờ port). Doc-drift đã biết: lấy **DB schema làm chuẩn**, không lấy doc cũ (`rate_percent/category_ids[]` sai; thực tế `rate/max_budget/sub_caps`).