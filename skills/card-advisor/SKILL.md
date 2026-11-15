---
name: card-advisor
description: Tư vấn chọn thẻ tối ưu cashback theo category / merchant / MCC, xét min_cycle_spend + cap còn lại + headroom.
triggers:
  - /card
  - card advisor
status: skeleton
phase: P4
---

# Skill: Card Advisor (`card-advisor`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P4** (xem `PLAN.md`).

## 1. Mục đích
Xếp hạng thẻ theo cashback ròng thực tế (cap còn lại, min spend đã đạt, MCC hợp lệ), không chỉ rate danh nghĩa.

## 2. Trigger / Input
- `/card` — Tư vấn chọn thẻ tối ưu cashback theo category / merchant / MCC, xét min_cycle_spend + cap còn lại + headroom.

## 3. Contract & Bất biến (pre-filled)
- Đọc engine + rule từ card MD / DB (không hardcode rate).
- Xét `remaining_cb_cap` (cumulative ASC), `min_cycle_spend`, excluded MCC.
- Family: headroom theo root.

## 4. Workflow (TODO — pre-fill sau)
- [ ] Nhận category/merchant/amount.
- [ ] Lọc thẻ hợp lệ (MCC, min spend, cap).
- [ ] Xếp hạng theo cashback ròng.
- [ ] Trả khuyến nghị + giải thích.

## 5. Output
- Bảng xếp hạng thẻ + cashback ước tính.

## 6. Dependencies (TODO — chưa tạo)
- kernel: cashback engine (TODO port `cashback.pure.ts`)
- DB: `v_cashback_remaining_cap` (TODO)
- accounts/cards/*
- knowledge 02/07 (TODO port)
