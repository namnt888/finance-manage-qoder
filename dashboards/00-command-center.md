---
title: "Command Center"
type: dashboard
status: skeleton__todo_dataview
phase: P6
---

# 📊 Command Center (`dashboards/00-command-center.md`)

> 🚧 SKELETON — Obsidian DataviewJS **read-only**. Query sẽ pre-fill sau khi kernel view `v_overview` tồn tại (P6).

## Mục đích
Tổng quan: số dư các bank, tổng nợ person, cashback tháng, batch pending, yield.

## Cột hiển thị (dự kiến)
- Tổng số dư theo account (bank/wallet/cash)
- Tổng nợ person theo kỳ
- Cashback estimated vs real_awarded tháng
- Batch pending clear
- Yield lãi tháng

## DataviewJS (TODO — pre-fill sau)
```dataviewjs
// TODO: query kernel view `v_overview` (read-only projection).
// dv.table([...], await kernelQuery("v_overview"))
```

## Nguồn
- Kernel view: `v_overview` (TODO tạo ở P6)
- Bất biến: `skills/invariants.md` (zero-hallucination — dashboard chỉ đọc view)
