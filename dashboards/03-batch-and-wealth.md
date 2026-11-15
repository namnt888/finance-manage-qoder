---
title: "Batch · Yield · Wealth"
type: dashboard
status: skeleton__todo_dataview
phase: P6
---

# 📊 Batch · Yield · Wealth (`dashboards/03-batch-and-wealth.md`)

> 🚧 SKELETON — Obsidian DataviewJS **read-only**. Query sẽ pre-fill sau khi kernel view `v_batch_pending_clear` tồn tại (P6).

## Mục đích
Batch pending clear 2 mode, túi sinh lời, vị thế vàng/investment.

## Cột hiển thị (dự kiến)
- Batch pending: DIRECT vs WAIT_DEBIT
- Yield pockets: threshold + lãi/ngày
- Wealth: gold quantity/price, investment
- Lãi/lỗ vị thế

## DataviewJS (TODO — pre-fill sau)
```dataviewjs
// TODO: query kernel view `v_batch_pending_clear` (read-only projection).
// dv.table([...], await kernelQuery("v_batch_pending_clear"))
```

## Nguồn
- Kernel view: `v_batch_pending_clear` (TODO tạo ở P6)
- Bất biến: `skills/invariants.md` (zero-hallucination — dashboard chỉ đọc view)
