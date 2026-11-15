---
account_id: "688bdd49-9e2a-4cf6-9fa5-092dfb067fc1"
name: "Sacombank O2"
type: "credit_card"
is_active: true
credit_limit: 0
effective_shared_limit: 40000000
family_parent_id: "3f990ca4-3b39-42a9-bb22-9cb2b4ebe776"
family_parent_name: "Sacombank Cashback"
billing_day: 7
payment_due_day: 2
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

# 💳 Sacombank O2

> 🚧 **SKELETON** — thông tin cấu trúc pre-fill từ DB snapshot (version-controlled). **Rate cashback chi tiết / MCC / điều khoản: TODO** — chờ link từng thẻ để viết lại rule.

## 1. Thông Tin Hạn Mức & Thanh Toán Batch (`/batch`)
- **Hạn mức hiệu lực:** `40,000,000 VND` (Hạn mức chia sẻ với `Sacombank Cashback` (headroom tính theo root))
- **Ngày chốt sao kê (`billing_day`):** `7`
- **Ngày đến hạn thanh toán (`payment_due_day`):** `2`
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
