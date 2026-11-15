---
account_id: "7c0a3b4c-2e06-44e5-8abc-e60cf74ecbda"
name: "VIB Travel Elite"
type: "credit_card"
is_active: true
credit_limit: 0
effective_shared_limit: 400000000
family_parent_id: "17df3cd5-a04d-4a38-8337-1ec72775cd4e"
family_parent_name: "Vib Max"
billing_day: 27
payment_due_day: 22
account_number: "322338"
receiver_name: "NGUYEN THANH NAM"
linked_bank_name: "VIB"
batch_transfer_mode: "LINKED_BANK_WAIT_DEBIT"
cashback_engine_type: "standard"
min_cycle_spend: 0
global_cap: null
fx_fee_rate: null
fx_fee_on_refund: false
rule_status: "structural_prefilled__rules_todo"
---

# 💳 VIB Travel Elite

> 🚧 **SKELETON** — thông tin cấu trúc pre-fill từ DB snapshot (version-controlled). **Rate cashback chi tiết / MCC / điều khoản: TODO** — chờ link từng thẻ để viết lại rule.

## 1. Thông Tin Hạn Mức & Thanh Toán Batch (`/batch`)
- **Hạn mức hiệu lực:** `400,000,000 VND` (Hạn mức chia sẻ với `Vib Max` (headroom tính theo root))
- **Ngày chốt sao kê (`billing_day`):** `27`
- **Ngày đến hạn thanh toán (`payment_due_day`):** `22`
- **Cơ chế Batch Transfer:** `LINKED_BANK_WAIT_DEBIT` — Chuyển vào TK ngân hàng liên kết **VIB** (`322338`) chờ auto-debit
- **Số TK nhận (`account_number`):** `322338`
- **Tên người nhận (`receiver_name`):** `NGUYEN THANH NAM`

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
