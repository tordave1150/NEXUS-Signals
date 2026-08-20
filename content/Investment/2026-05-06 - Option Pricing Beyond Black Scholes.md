---
title: Option Pricing จาก Dynamic Hedging ถึง Put-Call Parity
note_type: source
primary_topic: Investment
secondary_topics: [Derivatives, Mathematics]
concepts: [Black-Scholes, Ito Lemma, Dynamic Hedging, Put-Call Parity, Gamma]
entities: [Nassim Nicholas Taleb, Louis Bachelier]
tags: [options, black-scholes, put-call-parity]
source_type: Facebook Post
source_title: เบื้องหลังราคา Options จากสมการ Black-Scholes สู่โลกจริง
source_author: GroundUp Academy
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-058__"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xlURL-058__"
source_date: 2026-05-06
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Options]]", "[[Put-Call Parity]]"]
---

# Option Pricing จาก Dynamic Hedging ถึง Put-Call Parity

> [!summary] TL;DR
> โพสต์สรุป Taleb ว่า Black–Scholes derivation ใช้ Itô และ dynamic hedging กำจัด drift ภายใต้สมมติฐาน ขณะที่ put-call parity ให้ข้อจำกัดราคาแบบ no-arbitrage ที่ไม่ต้องสมมติ distribution เฉพาะ

## Reconciliation

- Gamma คืออัตราการเปลี่ยน Delta เมื่อ underlying เปลี่ยน ไม่ใช่ “ความเสี่ยงที่หายไป”; delta hedge ยังเหลือ gamma, theta, volatility, jump และ rebalancing risk
- Continuous frictionless hedging เป็นอุดมคติ การใช้งานจริงมี discrete hedging, gaps, costs และ liquidity
- Put-call parity เชื่อม call, put, underlying และ present value ของ strike สำหรับ strike/expiry เดียวกัน แต่ไม่ได้แทน pricing model ทั้งหมดหรือให้ probability distribution ครบถ้วนเพียงลำพัง
- ข้อเสนอของ Taleb แสดง risk-neutral valuation ภายใต้ put-call parity โดยหลีกเลี่ยง dynamic-hedging proof; นี่เป็นกรอบวิชาการ ไม่ใช่คำกล่าวว่า desks “ไม่ใช้ Black-Scholes” ทุกแห่ง

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-058__)
- [Taleb — Risk Neutral Option Pricing Without Dynamic Hedging](https://nassimtaleb.org/2014/03/risk-neutral-option-pricing-without-dynamic-hedging-measure-theoretic-proof/)
- [Options Industry Council — Put/Call Parity](https://www.optionseducation.org/advancedconcepts/put-call-parity)
- [Options Industry Council — Understanding Greeks](https://www.optionseducation.org/advancedconcepts/understanding-options-greeks)


