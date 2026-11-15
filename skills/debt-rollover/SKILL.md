---
name: debt-rollover
description: Rollover nợ person sang kỳ mới, cascade cancel, Move Cycle — thay heuristic match bằng correlation id.
triggers:
  - /rollover
  - debt rollover
status: skeleton
phase: P5
---

# Skill: Person Debt Rollover (`debt-rollover`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P5** (xem `PLAN.md`).

## 1. Mục đích
Chuyển dư nợ person giữa các `debt_cycle_tag`; cascade cancel các khoản phụ thuộc; KHÔNG trộn với `persisted_cycle_tag`.

## 2. Trigger / Input
- `/rollover` — Rollover nợ person sang kỳ mới, cascade cancel, Move Cycle — thay heuristic match bằng correlation id.

## 3. Contract & Bất biến (pre-filled)
- `debt_cycle_tag` (person/sheet) ≠ `persisted_cycle_tag` (card billing) — không bao giờ trộn.
- Rollover dùng correlation id (thay match person+amount+notes LIKE heuristic cũ).
- Cascade cancel phải atomic.

## 4. Workflow (TODO — pre-fill sau)
- [ ] Chọn person + kỳ nguồn/đích.
- [ ] Tính dư nợ rollover.
- [ ] Gọi kernel rollover RPC (correlation id).
- [ ] Verify debt matrix + sheet.

## 5. Output
- Ledger rollover events + debt matrix cập nhật.

## 6. Dependencies (TODO — chưa tạo)
- kernel: rollover RPC (TODO)
- DB: `v_person_debt` (TODO)
- [[submit-txn]] · [[monthly-report]]
- knowledge 06/17 (TODO port)
