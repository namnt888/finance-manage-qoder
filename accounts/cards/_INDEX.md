---
title: "Danh Mục Thẻ Tín Dụng Active (Routing Index)"
updated: 2026-11-15
status: skeleton_structural_prefilled
---

# 💳 Danh Mục Thẻ Tín Dụng (`accounts/cards/_INDEX.md`)

> **Tầng 1 (Fast Routing Index)** cho AI Agent khi tư vấn thẻ hoặc chạy `/batch`.
> Cấu trúc pre-fill từ DB snapshot. Rate chi tiết từng thẻ: xem file thẻ (TODO).

| Thẻ Tín Dụng | Hạn Mức (VND) | Ngày Chốt | Family Group | Linked Bank (`/batch`) | Engine |
| :--- | :---: | :---: | :--- | :--- | :--- |
| [[acb-platinum\|ACB Platinum]] | 150,000,000 | 24 | Standalone | Trả thẳng | `standard` |
| [[acb-platinum-mom\|Acb Platinum #mom]] | 50,000,000 | 24 | Standalone | Trả thẳng | `standard` |
| [[bidv-cashback\|Bidv Cashback]] | 45,000,000 | — | Standalone | Trả thẳng | `standard` |
| [[hdbank-ezcard-rei\|HDBank EzCard #Rei]] | 25,000,000 | — | Standalone | Trả thẳng | `hdb_ezcard` |
| [[hdbank-ezcard-mom\|HDBank EzCard #mom]] | 30,000,000 | — | Standalone | Trả thẳng | `hdb_ezcard` |
| [[msb-online-mom\|MSB Online - Mom]] | 48,000,000 | 25 | Standalone | MSB Mom | `msb_online` |
| [[msb-online-rei\|MSB Online - Rei]] | 30,000,000 | 25 | Standalone | MSB | `msb_online` |
| [[msb-mdigi-mom\|MSB mDigi - Mom]] | 48,000,000 | 25 | MSB Online - Mom | MSB Mom | `msb_mdigi` |
| [[msb-mdigi-rei\|MSB mDigi - Rei]] | 30,000,000 | 25 | MSB Online - Rei | MSB | `msb_mdigi` |
| [[mbb-jcb-platinum\|Mbb JCB Platinum]] | 55,000,000 | 9 | Mbb JCB Ultimate | Trả thẳng | `mbb_jcb` |
| [[mbb-jcb-ultimate\|Mbb JCB Ultimate]] | 55,000,000 | 8 | Standalone | Trả thẳng | `standard` |
| [[sacombank-cashback\|Sacombank Cashback]] | 40,000,000 | — | Standalone | Trả thẳng | `standard` |
| [[sacombank-o2\|Sacombank O2]] | 40,000,000 | 7 | Sacombank Cashback | Trả thẳng | `standard` |
| [[shinhan-cashback-365\|Shinhan Cashback 365]] | 103,200,000 | — | Standalone | Shinhan | `shinhan_365` |
| [[shinhan-supreme\|Shinhan Supreme]] | 103,200,000 | 26 | Shinhan Cashback 365 | Shinhan | `shinhan_supreme` |
| [[techcombank-everyday-rei\|Techcombank Everyday #Rei]] | 85,000,000 | 0 | Standalone | Techcombank - Nam | `techcom_everyday` |
| [[techcombank-everyday-mom\|Techcombank Everyday Mom]] | 44,000,000 | 0 | Standalone | Techcombank - Mom | `techcom_everyday` |
| [[techcombank-spark-mom\|Techcombank Spark Mom]] | 50,000,000 | — | Standalone | Techcombank - Mom | `standard` |
| [[vcb-visa-signature\|VCB Visa Signature]] | 150,000,000 | 20 | Standalone | Vcb Salad | `standard` |
| [[vib-online-2in1\|VIB Online 2in1]] | 400,000,000 | 27 | Vib Max | VIB | `standard` |
| [[vib-online-2in1-mom\|VIB Online 2in1 - Mom]] | 58,000,000 | 27 | Standalone | VIB mom | `standard` |
| [[vib-super-card\|VIB Super Card]] | 400,000,000 | 27 | Vib Max | VIB | `vib_super_card` |
| [[vib-travel-elite\|VIB Travel Elite]] | 400,000,000 | 27 | Vib Max | VIB | `standard` |
| [[vpbank-diamond-world\|VPBank Diamond World]] | 270,000,000 | 28 | Standalone | VPBank | `vpbank_diamond` |
| [[vib-max\|Vib Max]] | 400,000,000 | 27 | Standalone | VIB | `standard` |
| [[vpbank-lady\|Vpbank Lady]] | 54,000,000 | — | Standalone | VPBank | `standard` |
