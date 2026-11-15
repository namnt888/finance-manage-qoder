---
account_id: "b691e96f-1b24-474e-b578-b5855672a8c7"
name: "MSB Online - Mom"
type: "credit_card"
is_active: true
credit_limit: 48000000
effective_shared_limit: 48000000
family_parent_id: null
family_parent_name: null
billing_day: 25
payment_due_day: 9
account_number: "0362790199"
receiver_name: "NGUYEN THI THAO TRANG"
linked_bank_name: "MSB Mom"
batch_transfer_mode: "LINKED_BANK_WAIT_DEBIT"
cashback_engine_type: "msb_online"
min_cycle_spend: 3000000
global_cap: 300000
fx_fee_rate: null
fx_fee_on_refund: false
rule_status: "structural_prefilled__rules_todo"
---

# 💳 MSB Online - Mom

> 🚧 **SKELETON** — thông tin cấu trúc pre-fill từ DB snapshot (version-controlled). **Rate cashback chi tiết / MCC / điều khoản: TODO** — chờ link từng thẻ để viết lại rule.

## 1. Thông Tin Hạn Mức & Thanh Toán Batch (`/batch`)
- **Hạn mức hiệu lực:** `48,000,000 VND` (Hạn mức độc lập)
- **Ngày chốt sao kê (`billing_day`):** `25`
- **Ngày đến hạn thanh toán (`payment_due_day`):** `9`
- **Cơ chế Batch Transfer:** `LINKED_BANK_WAIT_DEBIT` — Chuyển vào TK ngân hàng liên kết **MSB Mom** (`0362790199`) chờ auto-debit
- **Số TK nhận (`account_number`):** `0362790199`
- **Tên người nhận (`receiver_name`):** `NGUYEN THI THAO TRANG`

## 2. Cấu Hình Cashback (TODO — pre-fill sau khi có link)
- **Engine:** `msb_online`
- **Min cycle spend (`min_cycle_spend`):** `3,000,000 VND`
- **Global cap (`global_cap`):** `300,000` VND

| Category | Rate | Max Budget | Min Spend | Excluded | Merchant |
| :--- | :---: | :---: | :---: | :---: | :--- |
| _(TODO — điền sau)_ | — | — | — | — | — |

## 3. Chi Tiết Điều Khoản & MCC Từ Ngân Hàng (TODO)
- **Link điều khoản ngân hàng:** _(Dán link PDF/Web của ngân hàng vào đây)_
- **MCC hợp lệ (Included MCCs):** `[]`
- **MCC loại trừ (Excluded MCCs):** `[]`
- **Ghi chú Edge Cases:** _(Cập nhật sau)_
