---
account_id: "06067af4-e4a6-41e2-9e32-1f3111636c04"
name: "Techcombank Everyday Mom"
type: "credit_card"
is_active: true
credit_limit: 44000000
effective_shared_limit: 44000000
family_parent_id: null
family_parent_name: null
billing_day: 0
payment_due_day: 5
account_number: "7555667799"
receiver_name: "NGUYEN THI THAO TRANG"
linked_bank_name: "Techcombank - Mom"
batch_transfer_mode: "LINKED_BANK_WAIT_DEBIT"
cashback_engine_type: "techcom_everyday"
min_cycle_spend: 0
global_cap: null
fx_fee_rate: null
fx_fee_on_refund: false
rule_status: "structural_prefilled__rules_todo"
---

# 💳 Techcombank Everyday Mom

> 🚧 **SKELETON** — thông tin cấu trúc pre-fill từ DB snapshot (version-controlled). **Rate cashback chi tiết / MCC / điều khoản: TODO** — chờ link từng thẻ để viết lại rule.

## 1. Thông Tin Hạn Mức & Thanh Toán Batch (`/batch`)
- **Hạn mức hiệu lực:** `44,000,000 VND` (Hạn mức độc lập)
- **Ngày chốt sao kê (`billing_day`):** `0`
- **Ngày đến hạn thanh toán (`payment_due_day`):** `5`
- **Cơ chế Batch Transfer:** `LINKED_BANK_WAIT_DEBIT` — Chuyển vào TK ngân hàng liên kết **Techcombank - Mom** (`7555667799`) chờ auto-debit
- **Số TK nhận (`account_number`):** `7555667799`
- **Tên người nhận (`receiver_name`):** `NGUYEN THI THAO TRANG`

## 2. Cấu Hình Cashback (TODO — pre-fill sau khi có link)
- **Engine:** `techcom_everyday`
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
