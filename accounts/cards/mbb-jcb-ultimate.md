---
account_id: "7f20a018-2ef4-4b89-b451-6bac2dc8a473"
name: "Mbb JCB Ultimate"
type: "credit_card"
is_active: true
credit_limit: 55000000
effective_shared_limit: 55000000
family_parent_id: null
family_parent_name: null
billing_day: 8
payment_due_day: 23
account_number: null
receiver_name: null
linked_bank_name: null
batch_transfer_mode: "DIRECT_CARD_PAY"
cashback_engine_type: "standard"
min_cycle_spend: 0
global_cap: null
fx_fee_rate: null
fx_fee_on_refund: false
rule_status: "structural_prefilled__rules_todo"
---

# 💳 Mbb JCB Ultimate

> 🚧 **SKELETON** — thông tin cấu trúc pre-fill từ DB snapshot (version-controlled). **Rate cashback chi tiết / MCC / điều khoản: TODO** — chờ link từng thẻ để viết lại rule.

## 1. Thông Tin Hạn Mức & Thanh Toán Batch (`/batch`)
- **Hạn mức hiệu lực:** `55,000,000 VND` (Hạn mức độc lập)
- **Ngày chốt sao kê (`billing_day`):** `8`
- **Ngày đến hạn thanh toán (`payment_due_day`):** `23`
- **Cơ chế Batch Transfer:** `DIRECT_CARD_PAY` — Trả thẳng vào thẻ, khôi phục `available_balance` ngay (không qua TK liên kết)
- **Số TK nhận (`account_number`):** `— (TODO)`
- **Tên người nhận (`receiver_name`):** `— (TODO)`

## 2. Cấu Hình Cashback (TODO — pre-fill sau khi có link)
- **Engine:** `standard`
- **Min cycle spend (`min_cycle_spend`):** `0 VND`
- **Global cap (`global_cap`):** `—`

| Category | Rate | Max Budget | Min Spend | Excluded | Merchant |
| :--- | :---: | :---: | :---: | :---: | :--- |
| _(TODO — điền sau)_ | — | — | — | — | — |

## 3. Chi Tiết Điều Khoản & MCC Từ Ngân Hàng (TODO)
- **Link điều khoản ngân hàng:** _(Dán link PDF/Web của ngân hàng vào đây)_
- **MCC hợp lệ (Included MCCs):** `[]`
- **MCC loại trừ (Excluded MCCs):** `[]`
- **Ghi chú Edge Cases:** _(Cập nhật sau)_
