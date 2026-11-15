---
account_id: "435a79c3-7476-4789-acbc-284cbfd4e55b"
name: "Shinhan Supreme"
type: "credit_card"
is_active: true
credit_limit: 0
effective_shared_limit: 103200000
family_parent_id: "e0000000-0000-0000-0000-000000000102"
family_parent_name: "Shinhan Cashback 365"
billing_day: 26
payment_due_day: 10
account_number: "0389191959"
receiver_name: "NGUYEN THANH NAM"
linked_bank_name: "Shinhan"
batch_transfer_mode: "LINKED_BANK_WAIT_DEBIT"
cashback_engine_type: "shinhan_supreme"
min_cycle_spend: 3000000
global_cap: 1000000
fx_fee_rate: null
fx_fee_on_refund: false
rule_status: "structural_prefilled__rules_todo"
---

# 💳 Shinhan Supreme

> 🚧 **SKELETON** — thông tin cấu trúc pre-fill từ DB snapshot (version-controlled). **Rate cashback chi tiết / MCC / điều khoản: TODO** — chờ link từng thẻ để viết lại rule.

## 1. Thông Tin Hạn Mức & Thanh Toán Batch (`/batch`)
- **Hạn mức hiệu lực:** `103,200,000 VND` (Hạn mức chia sẻ với `Shinhan Cashback 365` (headroom tính theo root))
- **Ngày chốt sao kê (`billing_day`):** `26`
- **Ngày đến hạn thanh toán (`payment_due_day`):** `10`
- **Cơ chế Batch Transfer:** `LINKED_BANK_WAIT_DEBIT` — Chuyển vào TK ngân hàng liên kết **Shinhan** (`0389191959`) chờ auto-debit
- **Số TK nhận (`account_number`):** `0389191959`
- **Tên người nhận (`receiver_name`):** `NGUYEN THANH NAM`

## 2. Cấu Hình Cashback (TODO — pre-fill sau khi có link)
- **Engine:** `shinhan_supreme`
- **Min cycle spend (`min_cycle_spend`):** `3,000,000 VND`
- **Global cap (`global_cap`):** `1,000,000` VND

| Category | Rate | Max Budget | Min Spend | Excluded | Merchant |
| :--- | :---: | :---: | :---: | :---: | :--- |
| _(TODO — điền sau)_ | — | — | — | — | — |

## 3. Chi Tiết Điều Khoản & MCC Từ Ngân Hàng (TODO)
- **Link điều khoản ngân hàng:** _(Dán link PDF/Web của ngân hàng vào đây)_
- **MCC hợp lệ (Included MCCs):** `[]`
- **MCC loại trừ (Excluded MCCs):** `[]`
- **Ghi chú Edge Cases:** _(Cập nhật sau)_
