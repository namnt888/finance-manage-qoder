---
name: transfer
description: Chuyển khoản giữa các tài khoản ngân hàng / ví / tiền mặt (internal transfer, không phải trả nợ thẻ).
triggers:
  - /transfer
  - transfer
status: skeleton
phase: P2
---

# Skill: Internal Transfer (`transfer`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P2** (xem `PLAN.md`).

## 1. Mục đích
Chuyển tiền giữa 2 account nội bộ; bảo toàn tổng số dư, ghi 2 leg (out/in) cùng correlation id.

## 2. Trigger / Input
- `/transfer` — Chuyển khoản giữa các tài khoản ngân hàng / ví / tiền mặt (internal transfer, không phải trả nợ thẻ).

## 3. Contract & Bất biến (pre-filled)
- Mỗi transfer = 2 leg atomically (debit nguồn / credit đích) chung `correlation_id`.
- Không tự tính số dư — kernel/view đảm nhiệm.
- Idempotency key chống trùng.

## 4. Workflow (TODO — pre-fill sau)
- [ ] Resolve account nguồn + đích.
- [ ] Gọi kernel transfer RPC.
- [ ] Verify balances 2 account.

## 5. Output
- 2 ledger legs + balance cập nhật.

## 6. Dependencies (TODO — chưa tạo)
- kernel: transfer RPC (TODO)
- [[submit-txn]] · [[card-repayment]]
- knowledge 11 (TODO port)
