---
name: refund
description: Hoàn tiền giao dịch + xử lý FX fee deferred (JCB fx_fee_on_refund), trạng thái refund state machine.
triggers:
  - /refund
  - refund
status: skeleton
phase: P5
---

# Skill: Refund & FX Fee (`refund`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P5** (xem `PLAN.md`).

## 1. Mục đích
Refund theo state machine (refundGuards); FX fee deferred bị loại trừ khỏi cashback; hoàn FX fee nếu card có `fx_fee_on_refund`.

## 2. Trigger / Input
- `/refund` — Hoàn tiền giao dịch + xử lý FX fee deferred (JCB fx_fee_on_refund), trạng thái refund state machine.

## 3. Contract & Bất biến (pre-filled)
- FX fee deferred KHÔNG tính cashback (financial.service).
- `fx_fee_on_refund` (vd JCB): hoàn cả FX fee khi refund.
- Refund phải trace về txn gốc (correlation id).

## 4. Workflow (TODO — pre-fill sau)
- [ ] Resolve txn gốc.
- [ ] Tính refund + FX fee (nếu áp dụng).
- [ ] Gọi kernel refund RPC (state machine).
- [ ] Verify cashback đã clawback đúng.

## 5. Output
- Refund events + cashback adjustment.

## 6. Dependencies (TODO — chưa tạo)
- kernel: refund RPC (TODO port refundGuards)
- [[submit-txn]] · [[card-advisor]]
- knowledge 19 (TODO port)
