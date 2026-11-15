---
account_id: "d8a9e102-3c1a-471a-bf41-477002000001"
name: "VPBank Diamond World"
type: "credit_card"
is_active: true
credit_limit: 270000000
effective_shared_limit: 270000000
family_parent_id: null
family_parent_name: null
billing_day: 28
payment_due_day: 14
account_number: "8668668899"
receiver_name: "NGUYEN THANH NAM"
linked_bank_name: "VPBank"
batch_transfer_mode: "LINKED_BANK_WAIT_DEBIT"
cashback_engine_type: "vpbank_diamond"
min_cycle_spend: 4000000
global_cap: null
fx_fee_rate: null
fx_fee_on_refund: false
rule_status: "structural_prefilled__rules_todo"
---

# 💳 VPBank Diamond World

> 🚧 **SKELETON** — thông tin cấu trúc pre-fill từ DB snapshot (version-controlled). **Rate cashback chi tiết / MCC / điều khoản: TODO** — chờ link từng thẻ để viết lại rule.

## 1. Thông Tin Hạn Mức & Thanh Toán Batch (`/batch`)
- **Hạn mức hiệu lực:** `270,000,000 VND` (Hạn mức độc lập)
- **Ngày chốt sao kê (`billing_day`):** `28`
- **Ngày đến hạn thanh toán (`payment_due_day`):** `14`
- **Cơ chế Batch Transfer:** `LINKED_BANK_WAIT_DEBIT` — Chuyển vào TK ngân hàng liên kết **VPBank** (`8668668899`) chờ auto-debit
- **Số TK nhận (`account_number`):** `8668668899`
- **Tên người nhận (`receiver_name`):** `NGUYEN THANH NAM`

## 2. Cấu Hình Cashback (TODO — pre-fill sau khi có link)
- **Engine:** `vpbank_diamond`
- **Min cycle spend (`min_cycle_spend`):** `4,000,000 VND`
- **Global cap (`global_cap`):** `—`

| Category | Rate | Max Budget | Min Spend | Excluded | Merchant |
| :--- | :---: | :---: | :---: | :---: | :--- |
| _(TODO — điền sau)_ | — | — | — | — | — |

## 3. Chi Tiết Điều Khoản & MCC Từ Ngân Hàng (TODO)
- **Link điều khoản ngân hàng:** _(Dán link PDF/Web của ngân hàng vào đây)_
- **MCC hợp lệ (Included MCCs):** `[]`
- **MCC loại trừ (Excluded MCCs):** `[]`
- **Ghi chú Edge Cases:** _(Cập nhật sau)_
