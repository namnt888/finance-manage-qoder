---
name: reconcile-statement
description: Đối soát sao kê ngân hàng với ledger; phát hiện lệch, gợi ý điều chỉnh (không tự sửa).
triggers:
  - /reconcile
  - reconcile statement
status: skeleton
phase: P5
---

# Skill: Reconcile Statement (`reconcile-statement`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P5** (xem `PLAN.md`).

## 1. Mục đích
So khớp từng dòng sao kê với ledger theo amount/date/note; flag lệch, đề xuất adjustment cho user duyệt.

## 2. Trigger / Input
- `/reconcile` — Đối soát sao kê ngân hàng với ledger; phát hiện lệch, gợi ý điều chỉnh (không tự sửa).

## 3. Contract & Bất biến (pre-filled)
- Không tự động sửa ledger — chỉ đề xuất.
- Match theo correlation/idempotency key khi có.

## 4. Workflow (TODO — pre-fill sau)
- [ ] Nhận sao kê (xlsx/csv/ảnh).
- [ ] Parse → so khớp ledger.
- [ ] Liệt kê lệch + đề xuất.
- [ ] User duyệt → adjustment qua kernel.

## 5. Output
- Báo cáo đối soát trong `reconcile/`.

## 6. Dependencies (TODO — chưa tạo)
- kernel: reconcile view (TODO)
- [[samsung-image-to-txn]]
- knowledge 21 (TODO port)
