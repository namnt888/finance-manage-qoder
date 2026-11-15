---
name: samsung-image-to-txn
description: Ảnh sao kê / bill / notification → trích xuất txn (Pixtral Vision) → review → submit qua kernel.
triggers:
  - /image
  - samsung image to txn
status: skeleton
phase: P2
---

# Skill: Image to Transaction (`samsung-image-to-txn`)

> 🚧 **SKELETON** — khung sườn. Workflow chi tiết sẽ pre-fill sau khi kernel (MCP + engine + scripts) hoàn thành. Thuộc **P2** (xem `PLAN.md`).

## 1. Mục đích
Vision OCR trích xuất amount/date/merchant/note từ ảnh; LUÔN cho user review trước khi submit.

## 2. Trigger / Input
- `/image` — Ảnh sao kê / bill / notification → trích xuất txn (Pixtral Vision) → review → submit qua kernel.

## 3. Contract & Bất biến (pre-filled)
- Ảnh → draft txn, KHÔNG auto-submit.
- Notes giữ nguyên văn bản gốc.
- Resolve ngày tương đối trước khi ghi.

## 4. Workflow (TODO — pre-fill sau)
- [ ] Nhận ảnh.
- [ ] Vision extract → draft txn.
- [ ] User review/confirm.
- [ ] Gọi [[submit-txn]].

## 5. Output
- Draft txn → ledger sau khi duyệt.

## 6. Dependencies (TODO — chưa tạo)
- kernel: vision extract (TODO)
- [[submit-txn]] · [[reconcile-statement]]
- knowledge 18 (TODO port)
