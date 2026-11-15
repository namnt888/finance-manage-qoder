---
name: wealth-gold
description: Mua/bán vàng & chứng chỉ quỹ: quantity/price, Wealth tab, lãi/lỗ vị thế.
triggers:
  - /gold
  - wealth gold
status: skeleton
phase: P6
---

# Skill: Wealth & Gold (`wealth-gold`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P6** (xem `PLAN.md`).

## 1. Mục đích
Quản lý vị thế vàng (quantity × price) và investment; tính giá vốn + lãi/lỗ.

## 2. Trigger / Input
- `/gold` — Mua/bán vàng & chứng chỉ quỹ: quantity/price, Wealth tab, lãi/lỗ vị thế.

## 3. Contract & Bất biến (pre-filled)
- Gold: quantity/price riêng biệt, không nhầm với amount VND.
- Wealth accounts type `invest`/`investment`.

## 4. Workflow (TODO — pre-fill sau)
- [ ] Nhận lệnh mua/bán (quantity, price).
- [ ] Gọi kernel wealth RPC.
- [ ] Cập nhật vị thế + giá vốn.
- [ ] Verify Wealth dashboard.

## 5. Output
- Wealth txn + position cập nhật.

## 6. Dependencies (TODO — chưa tạo)
- kernel: wealth RPC (TODO)
- accounts/wealth/_INDEX.md
- [[monthly-report]]
- knowledge 05 (TODO port)
