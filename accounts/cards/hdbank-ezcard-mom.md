---
account_id: "c1be0f0b-ec11-4ce7-852c-51e878241374"
name: "HDBank EzCard #mom"
type: "credit_card"
is_active: true
credit_limit: 30000000
effective_shared_limit: 30000000
family_parent_id: null
family_parent_name: null
billing_day: null
payment_due_day: 5
account_number: null
receiver_name: null
linked_bank_name: null
batch_transfer_mode: "DIRECT_CARD_PAY"
cashback_engine_type: "hdb_ezcard"
min_cycle_spend: 0
global_cap: 400000
fx_fee_rate: null
fx_fee_on_refund: false
rule_status: "structural_prefilled__rules_todo"
---

# 💳 HDBank EzCard #mom

> 🚧 **SKELETON** — thông tin cấu trúc pre-fill từ DB snapshot (version-controlled). **Rate cashback chi tiết / MCC / điều khoản: TODO** — chờ link từng thẻ để viết lại rule.

## 1. Thông Tin Hạn Mức & Thanh Toán Batch (`/batch`)
- **Hạn mức hiệu lực:** `30,000,000 VND` (Hạn mức độc lập)
- **Ngày chốt sao kê (`billing_day`):** `— (TODO)`
- **Ngày đến hạn thanh toán (`payment_due_day`):** `5`
- **Cơ chế Batch Transfer:** `DIRECT_CARD_PAY` — Trả thẳng vào thẻ, khôi phục `available_balance` ngay (không qua TK liên kết)
- **Số TK nhận (`account_number`):** `— (TODO)`
- **Tên người nhận (`receiver_name`):** `— (TODO)`

## 2. Cấu Hình Cashback (TODO — pre-fill sau khi có link)
- **Engine:** `hdb_ezcard`
- **Min cycle spend (`min_cycle_spend`):** `0 VND`
- **Global cap (`global_cap`):** `400,000` VND

| Category | Rate | Max Budget | Min Spend | Excluded | Merchant |
| :--- | :---: | :---: | :---: | :---: | :--- |
| _(TODO — điền sau)_ | — | — | — | — | — |

## 3. Chi Tiết Điều Khoản & MCC Từ Ngân Hàng (TODO)
- **Link điều khoản ngân hàng:** _(Dán link PDF/Web của ngân hàng vào đây)_
- **MCC hợp lệ (Included MCCs):** `[]`
- **MCC loại trừ (Excluded MCCs):** `[]`
- **Ghi chú Edge Cases:** _(Cập nhật sau)_
