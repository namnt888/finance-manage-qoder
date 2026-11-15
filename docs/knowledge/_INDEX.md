---
title: "Domain Knowledge Bridge (port từ money-gemini)"
status: skeleton__todo_port
---

# 📚 Domain Knowledge (`docs/knowledge/_INDEX.md`)

> 🚧 **SKELETON** — knowledge gốc nằm ở `money-gemini/docs/knowledge/*.md` (đã test, đúng thực tế).
> Phase P1 sẽ **port** sang đây (đọc-only reference, không sửa bản gốc). Mỗi doc gắn với skill tương ứng.

| # | File gốc (money-gemini) | Chủ đề | Skill dùng | Port status |
| :-- | :--- | :--- | :--- | :---: |
| 01 | `01-accounts-and-bank.md` | Tạo account, add bank | submit-txn | ⏳ TODO |
| 02 | `02-cashback-engine.md` | Cashback rules, calculation | card-advisor | ⏳ TODO |
| 03 | `03-batch-transfer.md` | Batch, export, bank mapping | batch-transfer | ⏳ TODO |
| 05 | `05-gold-management.md` | Gold quantity/price, Wealth | wealth-gold | ⏳ TODO |
| 06 | `06-person-debt-formulas.md` | Debt formulas, repayment | debt-rollover | ⏳ TODO |
| 07 | `07-volprofit-cashback.md` | Vol/Profit, estimatedCashbacks, min_spend | card-advisor | ⏳ TODO |
| 08 | `08-searchable-select.md` | SearchableSelect (UI — bỏ, agent-first) | — | ➖ N/A |
| 09 | `09-available-balance-convention.md` | Available balance, credit-card init txn | card-repayment | ⏳ TODO |
| 10 | `10-batch-items-table.md` | Batch items table (UI — bỏ) | — | ➖ N/A |
| 11 | `11-linked-account-transfer.md` | Linked card→bank, 2-way confirm | card-repayment | ⏳ TODO |
| 12 | `12-people-table-redesign.md` | People table (UI — bỏ) | — | ➖ N/A |
| 12b | `12-account-filter-cascade.md` | Account filter cascade (UI — bỏ) | — | ➖ N/A |
| 14 | `14-auto-installment-gen.md` | Auto installment generation | submit-txn | ⏳ TODO |
| 15 | `15-account-profit-sharing.md` | Profit sharing, consolidated pockets | yield-interest | ⏳ TODO |
| 16 | `16-export-mechanisms.md` | 3 export: People sync, Txn exporter, Batch | batch-transfer | ⏳ TODO |
| 17 | `17-people-debt-rollover.md` | Rollover, cascade cancel, Move Cycle | debt-rollover | ⏳ TODO |
| 18 | `18-transaction-submission-workflow.md` | Submission flow (Quick Add / AI) | submit-txn | ⏳ TODO |
| 19 | `19-fx-fee-workflow.md` | FX fee auto-create, deferred, billing confirm | refund | ⏳ TODO |
| 20 | `20-deploy-configs.md` | Multi-row deploy_configs | month-run | ⏳ TODO |
| 21 | `21-reconcile-statement.md` | Bank statement reconciliation | reconcile-statement | ⏳ TODO |
| 22 | `22-subscriptions-prepaid-flow.md` | Subscriptions & prepaid, shared slots | submit-txn | ⏳ TODO |

## Ghi chú port
- Doc UI thuần (08/10/12/12b) **không port** — agent-first không có UI component.
- Doc nghiệp vụ: port nguyên văn công thức + edge-case, thay tham chiếu code bằng tham chiếu kernel/view.
- **Doc-drift đã biết** (từ blueprint §3.5): `ai/tools.ts` + SKILL add-cashback-rules + README mô tả `rate_percent/category_ids[]` nhưng DB thực tế là `rate/max_budget/sub_caps`. Khi port → lấy **DB schema làm chuẩn**, không lấy doc cũ.