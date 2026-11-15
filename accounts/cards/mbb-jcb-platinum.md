---
account_id: "2044ab3d-e848-4ac7-b1df-175c31b856b2"
name: "Mbb JCB Platinum"
type: "credit_card"
is_active: true
credit_limit: 55000000
effective_shared_limit: 55000000
family_parent_id: "7f20a018-2ef4-4b89-b451-6bac2dc8a473"
family_parent_name: "Mbb JCB Ultimate"
billing_day: 9
payment_due_day: 23
account_number: null
receiver_name: null
linked_bank_name: null
batch_transfer_mode: "DIRECT_CARD_PAY"
cashback_engine_type: "mbb_jcb"
min_cycle_spend: 2000000
global_cap: 500000
fx_fee_rate: null
fx_fee_on_refund: false
rule_status: "structural_prefilled__rules_todo"
---

# 💳 Mbb JCB Platinum

> 🚧 **SKELETON** — thông tin cấu trúc pre-fill từ DB snapshot (version-controlled). **Rate cashback chi tiết / MCC / điều khoản: TODO** — chờ link từng thẻ để viết lại rule.

## 1. Thông Tin Hạn Mức & Thanh Toán Batch (`/batch`)
- **Hạn mức hiệu lực:** `55,000,000 VND` (Hạn mức chia sẻ với `Mbb JCB Ultimate` (headroom tính theo root))
- **Ngày chốt sao kê (`billing_day`):** `9`
- **Ngày đến hạn thanh toán (`payment_due_day`):** `23`
- **Cơ chế Batch Transfer:** `DIRECT_CARD_PAY` — Trả thẳng vào thẻ, khôi phục `available_balance` ngay (không qua TK liên kết)
- **Số TK nhận (`account_number`):** `— (TODO)`
- **Tên người nhận (`receiver_name`):** `— (TODO)`

## 2. Cấu Hình Cashback (TODO — pre-fill sau khi có link)
- **Engine:** `mbb_jcb`
- **Min cycle spend (`min_cycle_spend`):** `2,000,000 VND`
- **Global cap (`global_cap`):** `500,000` VND

| Category | Rate | Max Budget | Min Spend | Excluded | Merchant |
| :--- | :---: | :---: | :---: | :---: | :--- |
| _(TODO — điền sau)_ | — | — | — | — | — |

## 3. Chi Tiết Điều Khoản & MCC Từ Ngân Hàng (TODO)
- **Link điều khoản ngân hàng:** _(Dán link PDF/Web của ngân hàng vào đây)_
- **MCC hợp lệ (Included MCCs):** `[]`
- **MCC loại trừ (Excluded MCCs):** `[]`
- **Ghi chú Edge Cases:** _(Cập nhật sau)_
