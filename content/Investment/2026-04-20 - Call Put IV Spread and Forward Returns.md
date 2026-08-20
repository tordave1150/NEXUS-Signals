---
title: Call-Put Implied Volatility Spread กับผลตอบแทนล่วงหน้า
note_type: source
primary_topic: Investment
secondary_topics: [Statistics, Derivatives]
concepts: [Implied Volatility Spread, Volatility Skew, Return Predictability]
entities: [QuantCorner, S&P 500]
tags: [options, implied-volatility, reconciliation]
source_type: Facebook Post
source_title: ตลาด Option บอกอะไรกับเรา
source_author: QuantCorner
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-046__"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xlURL-046__"
source_date: 2026-04-20
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: Medium
related: ["[[Options]]", "[[Volatility Skew]]"]
---

# Call-Put Implied Volatility Spread กับผลตอบแทนล่วงหน้า

> [!summary] TL;DR
> โพสต์รายงานว่า Call IV − Put IV เชื่อมโยงเชิงบวกกับผลตอบแทน S&P 500 ใน 30 วันถัดไป แต่ตัวเลข R² 0.215 และค่าเฉลี่ย/ความน่าจะเป็นที่ระบุยังตรวจซ้ำไม่ได้จากโพสต์เพียงอย่างเดียว

## Verification & Reconciliation

งานวิจัยมีหลักฐานว่า call-put IV spread อาจมีข้อมูลทำนายผลตอบแทนหุ้นและตลาด แต่การตีความว่า Call IV สูงคือ “โลภ” และ Put IV สูงคือ “กลัว” ตรง ๆ ง่ายเกินไป เพราะ IV ต่างกันตาม strike, delta, maturity, dividends, rates, borrow fees และแรงซื้อ hedge งานวิจัยบางชิ้นยังชี้ว่าส่วนหนึ่งของ predictability มาจาก stock-borrow fees

ดังนั้นต้องกำหนด option matching, sample, look-ahead controls และ transaction costs ก่อนถือเป็น edge ตัวเลขเฉพาะในโพสต์ควรจัดเป็น **unverified empirical claim** จนกว่าจะมี dataset/code ต้นทาง

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-046__)
- [Call-Put Implied Volatility Spreads and Option Returns](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=1640322)
- [Cboe — Inside Volatility Trading](https://www.cboe.com/insights/posts/inside-volatility-trading-the-adventures-of-volatility-markets)


