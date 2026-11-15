---
title: "People · Debt Matrix"
type: dashboard
status: skeleton__todo_dataview
phase: P5
---

# 📊 People · Debt Matrix (`dashboards/02-people-debt-matrix.md`)

> 🚧 SKELETON — Obsidian DataviewJS **read-only**. Query sẽ pre-fill sau khi kernel view `v_person_debt` tồn tại (P5).

## Mục đích
Ma trận nợ person theo debt_cycle_tag, rollover, yêu thích, sync sheet.

## Cột hiển thị (dự kiến)
- Nợ ròng từng person theo kỳ
- Rollover / cascade cancel
- Favorite + sync_to_sheet
- Lịch sử trả nợ

## DataviewJS (TODO — pre-fill sau)
```dataviewjs
// TODO: query kernel view `v_person_debt` (read-only projection).
// dv.table([...], await kernelQuery("v_person_debt"))
```

## Nguồn
- Kernel view: `v_person_debt` (TODO tạo ở P5)
- Bất biến: `skills/invariants.md` (zero-hallucination — dashboard chỉ đọc view)
