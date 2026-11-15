---
name: submit-txn
description: Ghi txn cá nhân (expense/income), chuyển khoản, bill chia sẻ, nợ person, trả nợ — atomic qua kernel RPC, sync Person Sheet.
triggers:
  - /submit
  - submit txn
status: skeleton
phase: P2
---

# Skill: Submit Transaction (`submit-txn`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P2** (xem `PLAN.md`).

## 1. Mục đích
Mọi giao dịch đi qua MỘT cổng ghi duy nhất (kernel `submit_agent_txn`) để PostgreSQL tính `persisted_cycle_tag`, `debt_cycle_tag`, `final_price` deterministically.

## 2. Trigger / Input
- `/submit` — Ghi txn cá nhân (expense/income), chuyển khoản, bill chia sẻ, nợ person, trả nợ — atomic qua kernel RPC, sync Person Sheet.

## 3. Contract & Bất biến (pre-filled)
- **Zero-hallucination:** KHÔNG tự tính `available_balance` / `net_debt` / `remaining_cb_cap` — luôn gọi kernel.
- Resolve account/person theo `_INDEX.md` (case-insensitive), KHÔNG auto-create.
- Notes copy nguyên văn; resolve ngày tương đối ('hôm qua') → ngày tuyệt đối trước khi ghi.
- Personal spend (không person) → `person_id=null`, `debt_cycle_tag=null`, `subtype=null`.

## 4. Workflow (TODO — pre-fill sau)
- [ ] Resolve entity (account, person, card nếu có cashback share).
- [ ] Gọi kernel RPC `submit_agent_txn(...)` với idempotency key.
- [ ] Verify post-insert: balances + debts qua view.
- [ ] Outbox → sync Person Sheet (nếu `sync_to_sheet`).

## 5. Output
- Row append-only trong ledger `transactions` + `transaction_events`.
- Sheet projection cập nhật qua outbox.

## 6. Dependencies (TODO — chưa tạo)
- kernel: `scripts/neon_cli.py submit-txn` (TODO)
- DB: RPC `submit_agent_txn` (TODO port)
- [[transfer]] · [[card-repayment]] · [[debt-rollover]]
- knowledge 18 (TODO port)
