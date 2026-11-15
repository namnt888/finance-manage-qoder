---
title: "MCC Dictionary (Merchant Category Code)"
status: skeleton__todo_port
---

# 🏷️ MCC Dictionary (`config/mcc/_INDEX.md`)

> 🚧 SKELETON — DB gốc `categories` (38) + `category_keywords` (145) + `shops` (23). Port ở P1.

## Mục đích
Phân loại merchant theo MCC → map sang `category_code` cho cashback engine (included/excluded MCC).

## Schema dự kiến (TODO port)
- [ ] Port `categories`, `category_keywords`, `shops`.
- [ ] Điền Included/Excluded MCCs từng thẻ (chờ link điều khoản — xem `accounts/cards/*.md` §3).
- Liên kết: `skills/card-advisor/SKILL.md`, knowledge 02 (TODO port).
