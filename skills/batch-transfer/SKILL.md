---
name: batch-transfer
description: Cuối tháng gõ /batch → agent đọc template xlsx đã attach, tự fill số tiền theo dư nợ, xuất file batch + lưu list txn sẵn.
triggers:
  - /batch
  - batch transfer
status: skeleton
phase: P3
---

# Skill: Universal Batch Transfer (`batch-transfer`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P3** (xem `PLAN.md`).

## 1. Mục đích
Zero-code onboarding: attach `<bank>.xlsx` → `inspect` tự nhận diện header/start_row/styles/bank dropdown → `generate` clone 100% file mẫu, chỉ thay data rows.

## 2. Trigger / Input
- `/batch` — Cuối tháng gõ /batch → agent đọc template xlsx đã attach, tự fill số tiền theo dư nợ, xuất file batch + lưu list txn sẵn.

## 3. Contract & Bất biến (pre-filled)
- 2 mode: `DIRECT_CARD_PAY` (cleared_account_id NULL) vs `LINKED_BANK_WAIT_DEBIT` (cleared_account_id NOT NULL).
- `BATCH_CLEARING_ID` = `88888888-9999-9999-9999-888888888888`.
- Generate clone nguyên bản xlsx (Font/Border/Cell Style/Merged/Data Validation/customXml/bank lookup sheet).
- Template registry: `batches/templates/_TEMPLATE_SCHEMAS.md`.

## 4. Workflow (TODO — pre-fill sau)
- [ ] Đọc template schema (hoặc `inspect` xlsx mới).
- [ ] Query dư nợ từng thẻ theo kỳ → build items (receiver, bank_number, amount, note, mapped_bank_name).
- [ ] `generate` xlsx → `batches/exports/`.
- [ ] Lưu list txn sẵn (batch run) → user review trước khi submit.

## 5. Output
- File `batches/exports/<BANK>_Batch_<MonYYYY>.xlsx`.
- Batch run JSON trong `runs/` (list txn chờ duyệt).

## 6. Dependencies (TODO — chưa tạo)
- kernel: `scripts/batch_xlsx.py inspect|generate` (TODO)
- DB: `v_batch_pending_clear` (TODO)
- [[card-repayment]]
- knowledge 03/16 (TODO port)
