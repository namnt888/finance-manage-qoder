---
title: "Bank Mappings (tên ngân hàng → mã code cho batch)"
status: skeleton__todo_port
---

# 🏦 Bank Mappings (`config/bank-mappings/_INDEX.md`)

> 🚧 SKELETON — DB gốc `bank_mappings` (~47 rows). Port sang Neon ở P1. KHÔNG hardcode tên/mã bank trong code.

## Mục đích
Map tên ngân hàng hiển thị → mã code (vd `SHBVN`, `MBB`, `VIB`) dùng cho cột `mapped_bank_name` trong batch xlsx + dropdown validation.

## Schema dự kiến (TODO port)
| Cột | Kiểu | Ghi chú |
| :--- | :--- | :--- |
| `bank_name` | text | Tên hiển thị |
| `bank_code` | text | Mã chuẩn (NAPAS/ISO) |
| `mbb_name` / `vib_name` | text | Tên theo dropdown từng template |

- [ ] Port `bank_mappings` từ money-gemini → Neon (P1).
- [ ] Sinh MD reference 1 chiều từ DB.
- Liên kết: `skills/batch-transfer/SKILL.md`, `batches/templates/_TEMPLATE_SCHEMAS.md`.
