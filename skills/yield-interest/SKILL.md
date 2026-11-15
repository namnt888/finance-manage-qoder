---
name: yield-interest
description: Tính & ghi nhận lãi túi sinh lời (MSB Saving, Shinhan Premier, Vpbank Premier) theo threshold + daily_interest.
triggers:
  - /interest
  - yield interest
status: skeleton
phase: P4
---

# Skill: Yield Pocket Interest (`yield-interest`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P4** (xem `PLAN.md`).

## 1. Mục đích
Lãi ước tính theo ngày trên số dư duy trì ≥ threshold; ghi nhận interest txn vào bank gốc.

## 2. Trigger / Input
- `/interest` — Tính & ghi nhận lãi túi sinh lời (MSB Saving, Shinhan Premier, Vpbank Premier) theo threshold + daily_interest.

## 3. Contract & Bất biến (pre-filled)
- Note chuẩn: `[<Pocket>] Interest [startDate to endDate] (N days)`.
- Lãi = daily_interest_vnd × N ngày (chỉ khi số dư ≥ threshold).
- Pocket linked `parent_bank_id` — lãi ghi vào bank gốc.

## 4. Workflow (TODO — pre-fill sau)
- [ ] Đọc pocket MD (threshold, daily).
- [ ] Tính N ngày + lãi.
- [ ] Gọi kernel ghi interest txn vào parent bank.
- [ ] Verify balance.

## 5. Output
- Interest txn trong ledger.

## 6. Dependencies (TODO — chưa tạo)
- kernel: interest RPC (TODO)
- accounts/yield-pockets/*
- [[monthly-report]]
