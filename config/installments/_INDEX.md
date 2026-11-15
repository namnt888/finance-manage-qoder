---
title: "Installment Plans (auto-generation)"
status: skeleton__todo_port
---

# 📆 Installments (`config/installments/_INDEX.md`)

> 🚧 SKELETON — DB gốc `installment_plans` (9) / `installment_slots` (81). Port ở P1.

## Bất biến nghiệp vụ (pre-fill từ knowledge 14)
- Auto-gen slot: `occurred_at = cycle + "-01"`, `not_calculate_balance` cho slot tương lai.
- Coi chừng subtype drift (knowledge 14:190/209) — chuẩn hóa khi port.

## TODO
- [ ] Port `installment_plans` + `installment_slots` + auto-gen logic.
- Liên kết: `skills/submit-txn/SKILL.md`, knowledge 14 (TODO port).
