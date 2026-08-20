---
title: แหล่งข้อมูล Historical Options แบบ Parquet
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Options]
concepts: [Options Data, Volatility Modeling, Data Quality]
entities: [Philipp Dubach]
tags: [options, dataset, quantitative-finance]
source_type: Facebook Post
source_title: แหล่งดาวน์โหลดข้อมูล Options ฟรี
source_author: Chaipat Nengcomma
source_url: "https://www.facebook.com/chaipat.ncm/posts/pfbid023mA1aDoJcFGZHe21cg5Mvsjp8TEXdJimhoXQ7UyUx8opzKuBrGefc6xm7LpdA6gxl?__cft__[0]=AZb27S4MyW6r4rNqb6ANhzBx0vBk0_ZxckNAy19MbLWPGxAQYa-_5xxOhdEsRdttrYlOSXk2NHSrjfrR6ssN5G7lyqFFavVGHv2l90ZL50qF9fGK0LKPqOmYMjt8dnsHbwRvESKvOaAqfPliC7UU8wBfF-UEGsXgY9tsvZX_DPatXw&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/chaipat.ncm/posts/pfbid023mA1aDoJcFGZHe21cg5Mvsjp8TEXdJimhoXQ7UyUx8opzKuBrGefc6xm7LpdA6gxl"
source_date: 2026-03-31
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: Medium-High
related: ["[[Options Data]]", "[[Volatility Modeling]]"]
---

# แหล่งข้อมูล Historical Options แบบ Parquet

> [!summary] TL;DR
> Dataset ของ Philipp Dubach ให้ historical option chains 104 symbols ช่วง 2008–2025 และ underlying SPY/IWM/QQQ ช่วง 1999–2025 ภายใต้ MIT license เหมาะกับงานเรียนรู้และ prototype แต่ต้อง audit คุณภาพก่อนวิจัยจริง

## Important Details

ไฟล์เป็น Parquet และอ่านด้วย `pandas.read_parquet(...)` ได้ มี repository แยก options กับ underlying prices โพสต์เตือนว่าการดาวน์โหลดไฟล์ใหญ่ผ่าน Cloudflare R2 อาจสะดุด

## Verification & Reconciliation

ข้อมูลช่วงเวลา จำนวน symbols และ license ได้รับการยืนยันจาก release metadata ที่อ้าง repository ต้นทาง แต่ควรตรวจ schema, corporate actions, duplicate quotes, stale prices, zero bids, contract multipliers, timezone และ survivorship ก่อน backtest รวมถึงห้ามถือว่าชุดข้อมูลฟรีเทียบเท่า OPRA-grade data

## Sources

- [Original Facebook post](https://www.facebook.com/chaipat.ncm/posts/pfbid023mA1aDoJcFGZHe21cg5Mvsjp8TEXdJimhoXQ7UyUx8opzKuBrGefc6xm7LpdA6gxl?__cft__[0]=AZb27S4MyW6r4rNqb6ANhzBx0vBk0_ZxckNAy19MbLWPGxAQYa-_5xxOhdEsRdttrYlOSXk2NHSrjfrR6ssN5G7lyqFFavVGHv2l90ZL50qF9fGK0LKPqOmYMjt8dnsHbwRvESKvOaAqfPliC7UU8wBfF-UEGsXgY9tsvZX_DPatXw&__tn__=%2CO%2CP-R)
- [Options data repository](https://github.com/philippdubach/options-data)
- [Underlying data repository](https://github.com/philippdubach/options-dataset-hist)

