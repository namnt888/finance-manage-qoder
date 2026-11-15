---
name: card-repayment
description: Trả nợ thẻ tín dụng: phân biệt trả thẳng (DIRECT_CARD_PAY) vs chuyển vào bank liên kết chờ auto-debit (LINKED_BANK_WAIT_DEBIT).
triggers:
  - /pay-card
  - card repayment
status: skeleton
phase: P3
---

# Skill: Card Repayment (`card-repayment`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P3** (xem `PLAN.md`).

## 1. Mục đích
Thanh toán dư nợ thẻ theo đúng `batch_transfer_mode` của từng thẻ; khôi phục headroom theo root family.

## 2. Trigger / Input
- `/pay-card` — Trả nợ thẻ tín dụng: phân biệt trả thẳng (DIRECT_CARD_PAY) vs chuyển vào bank liên kết chờ auto-debit (LINKED_BANK_WAIT_DEBIT).

## 3. Contract & Bất biến (pre-filled)
- `DIRECT_CARD_PAY`: tiền vào thẳng card → khôi phục `available_balance` ngay.
- `LINKED_BANK_WAIT_DEBIT`: tiền vào bank liên kết → chờ ngày auto-debit mới clear nợ thẻ.
- Headroom family tính theo root (`parent_id ?? id`), không theo hạn mức thẻ con.
- `BATCH_CLEARING_ID` = `88888888-9999-9999-9999-888888888888` (chỉ trong kernel constants).

## 4. Workflow (TODO — pre-fill sau)
- [ ] Đọc `batch_transfer_mode` + `linked_bank_name` từ card MD.
- [ ] Tính số tiền trả theo dư nợ kỳ (persisted_cycle_tag).
- [ ] Gọi kernel repayment RPC đúng mode.
- [ ] Verify headroom root + trạng thái chờ clear.

## 5. Output
- Ledger repayment + (nếu wait debit) bản ghi pending clear.

## 6. Dependencies (TODO — chưa tạo)
- kernel: repayment RPC (TODO)
- [[batch-transfer]] · [[submit-txn]]
- knowledge 09/11 (TODO port)
