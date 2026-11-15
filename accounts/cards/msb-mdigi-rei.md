---
account_id: "772c5eb1-d766-4f00-a259-8e70df2a1314"
name: "MSB mDigi - Rei"
type: "credit_card"
is_active: true
credit_limit: 0
effective_shared_limit: 30000000
family_parent_id: "addd010b-14eb-4043-a72f-1a3df1d31660"
family_parent_name: "MSB Online - Rei"
billing_day: 25
payment_due_day: 9
account_number: "04201012971663"
receiver_name: "NGUYEN THANH NAM"
linked_bank_name: "MSB"
batch_transfer_mode: "LINKED_BANK_WAIT_DEBIT"
cashback_engine_type: "msb_mdigi"
min_cycle_spend: 0
global_cap: 300000
fx_fee_rate: null
fx_fee_on_refund: false
rule_status: "structural_prefilled__rules_todo"
---

# 💳 MSB mDigi - Rei

> 🚧 **SKELETON** — thông tin cấu trúc pre-fill từ DB snapshot (version-controlled). **Rate cashback chi tiết / MCC / điều khoản: TODO** — chờ link từng thẻ để viết lại rule.

## 1. Thông Tin Hạn Mức & Thanh Toán Batch (`/batch`)
- **Hạn mức hiệu lực:** `30,000,000 VND` (Hạn mức chia sẻ với `MSB Online - Rei` (headroom tính theo root))
- **Ngày chốt sao kê (`billing_day`):** `25`
- **Ngày đến hạn thanh toán (`payment_due_day`):** `9`
- **Cơ chế Batch Transfer:** `LINKED_BANK_WAIT_DEBIT` — Chuyển vào TK ngân hàng liên kết **MSB** (`04201012971663`) chờ auto-debit
- **Số TK nhận (`account_number`):** `04201012971663`
- **Tên người nhận (`receiver_name`):** `NGUYEN THANH NAM`

## 2. Cấu Hình Cashback (TODO — pre-fill sau khi có link)
- **Engine:** `msb_mdigi`
- **Min cycle spend (`min_cycle_spend`):** `0 VND`
- **Global cap (`global_cap`):** `300,000` VND

| Category | Rate | Max Budget | Min Spend | Excluded | Merchant |
| :--- | :---: | :---: | :---: | :---: | :--- |
| _(TODO — điền sau)_ | — | — | — | — | — |

## 3. Chi Tiết Điều Khoản & MCC Từ Ngân Hàng (TODO)
- **Link điều khoản ngân hàng:** _(Dán link PDF/Web của ngân hàng vào đây)_
- **MCC hợp lệ (Included MCCs):** `[]`
- **MCC loại trừ (Excluded MCCs):** `[]`
- **Ghi chú Edge Cases:** _(Cập nhật sau)_
