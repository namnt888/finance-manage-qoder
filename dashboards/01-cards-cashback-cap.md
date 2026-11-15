---
title: "Cards · Cashback · Cap"
type: dashboard
status: skeleton__todo_dataview
phase: P4
---

# 📊 Cards · Cashback · Cap (`dashboards/01-cards-cashback-cap.md`)

> 🚧 SKELETON — Obsidian DataviewJS **read-only**. Query sẽ pre-fill sau khi kernel view `v_cashback_remaining_cap` tồn tại (P4).

## Mục đích
Hạn mức/headroom family, cap cashback còn lại từng thẻ, min_cycle_spend đạt/chưa.

## Cột hiển thị (dự kiến)
- Hạn mức hiệu lực + headroom theo root family
- Remaining cb cap (cumulative ASC)
- min_cycle_spend: đạt / chưa
- Engine + category rate
- Ngày chốt / đến hạn

## DataviewJS (TODO — pre-fill sau)
```dataviewjs
// TODO: query kernel view `v_cashback_remaining_cap` (read-only projection).
// dv.table([...], await kernelQuery("v_cashback_remaining_cap"))
```

## Nguồn
- Kernel view: `v_cashback_remaining_cap` (TODO tạo ở P4)
- Bất biến: `skills/invariants.md` (zero-hallucination — dashboard chỉ đọc view)
