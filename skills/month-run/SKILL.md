---
name: month-run
description: Orchestration chốt tháng: đóng cycle thẻ, chạy batch, ghi lãi, rollover nợ, sinh report, sync sheet — theo thứ tự bất biến.
triggers:
  - /month-run
  - month run
status: skeleton
phase: P6
---

# Skill: Month Run Orchestrator (`month-run`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P6** (xem `PLAN.md`).

## 1. Mục đích
Một lệnh chốt tháng chạy đúng trình tự các skill, idempotent, có correlation id cho cả run.

## 2. Trigger / Input
- `/month-run` — Orchestration chốt tháng: đóng cycle thẻ, chạy batch, ghi lãi, rollover nợ, sinh report, sync sheet — theo thứ tự bất biến.

## 3. Contract & Bất biến (pre-filled)
- Thứ tự: close cycle → batch → interest → rollover → report → sheet sync.
- Mỗi bước idempotent (chạy lại không trùng).
- `month_run` ghi trạng thái từng bước.

## 4. Workflow (TODO — pre-fill sau)
- [ ] Khởi tạo month_run (YYYY-MM).
- [ ] Chạy tuần tự các bước (gọi skill con).
- [ ] Ghi trạng thái + correlation id.
- [ ] Verify toàn bộ trước khi đóng run.

## 5. Output
- `runs/<YYYY-MM>/month_run.json` + report + batch exports.

## 6. Dependencies (TODO — chưa tạo)
- kernel: month_run orchestrator (TODO)
- Tất cả skill con
- [[monthly-report]] · [[batch-transfer]]
