---
name: monthly-report
description: Phân tích tài chính tháng chi tiết: thu/chi, cashback thực nhận, nợ person, biến động số dư, yield, wealth.
triggers:
  - /report
  - monthly report
status: skeleton
phase: P6
---

# Skill: Monthly Financial Report (`monthly-report`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P6** (xem `PLAN.md`).

## 1. Mục đích
Report tháng từ SQL views (deterministic), không tính tay; đối chiếu cashback ước tính vs thực nhận (real_awarded).

## 2. Trigger / Input
- `/report` — Phân tích tài chính tháng chi tiết: thu/chi, cashback thực nhận, nợ person, biến động số dư, yield, wealth.

## 3. Contract & Bất biến (pre-filled)
- Số liệu từ views, không hallucinate.
- Phân biệt cashback estimated vs `real_awarded`.
- FX fee deferred loại trừ.

## 4. Workflow (TODO — pre-fill sau)
- [ ] Chốt kỳ (month_run).
- [ ] Query views: thu/chi, cashback, debt, yield, wealth.
- [ ] Sinh report MD chi tiết + biểu đồ.
- [ ] Lưu `reports/<YYYY-MM>.md`.

## 5. Output
- Report tháng trong `reports/`.

## 6. Dependencies (TODO — chưa tạo)
- kernel: reporting views (TODO)
- [[month-run]] · [[yield-interest]] · [[debt-rollover]]
- dashboards/*
