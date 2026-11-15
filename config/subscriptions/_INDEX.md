---
title: "Subscriptions & Prepaid (shared slots)"
status: skeleton__todo_port
---

# 🔁 Subscriptions (`config/subscriptions/_INDEX.md`)

> 🚧 SKELETON — DB gốc `subscriptions` (18). Port ở P1.

## Bất biến nghiệp vụ (pre-fill từ knowledge 22)
- `price_per_cycle` là **TỔNG** chu kỳ, KHÔNG phải per-slot.
- `perSlot = ROUND(price_per_cycle / total_slots)`.
- Slot unused vẫn tính vào chia sẻ (xem knowledge 22:448-450).

## TODO
- [ ] Port `subscriptions` + slot sharing.
- [ ] Sinh MD active-subscriptions 1 chiều từ DB.
- Liên kết: `skills/submit-txn/SKILL.md`, knowledge 22 (TODO port).
