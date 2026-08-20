---
title: Option Implied Information for Portfolio Selection
note_type: source
primary_topic: Investment
secondary_topics: [Options, Portfolio Construction]
concepts: [Risk-Neutral Distribution, Volatility Risk Premium, Implied Skewness]
entities: [Victor DeMiguel, Andrey Plyakha, Raman Uppal, Grigory Vilkov]
tags: [options, portfolio-selection, implied-volatility]
source_type: Facebook Post and Research Paper
source_title: Improving Portfolio Selection Using Option-Implied Volatility and Skewness
source_author: GroundUp Academy
source_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid0QzHQGb73ECjhovnGXw4krEu8HbfixvYotJckjEeoSZ14AVhgmAUKoUMfk2ERm6Pil&id=61569334229421&__cft__[0]=AZaCgyeKSPVhQN43-Shq8W6P1YXl6ZuGyMz3SFNnqOKzNuA-JfOjdfAurJPDGwY0msIGw94JdJl_KZg4LI4FIKcwNYosL4Y1-45_XsStI5ajfCr0sTjWn6c0t5Qv5_zbr0NRMqWynMg4bHRILhauHa39tR8HNxeOo5DXGttUo47KKQ&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid0QzHQGb73ECjhovnGXw4krEu8HbfixvYotJckjEeoSZ14AVhgmAUKoUMfk2ERm6Pil&id=61569334229421"
source_date: 2026-06-04
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: Medium
related: ["[[Risk-Neutral Measure]]", "[[Portfolio Optimization]]"]
---

# Option Implied Information for Portfolio Selection

> [!summary] TL;DR
> ราคา option สะท้อน risk-neutral distribution (Q-world) ซึ่งรวมราคาความเสี่ยง ไม่ใช่ความน่าจะเป็นจริงแบบ P-world; งานวิจัยจึงแปลงข้อมูล option บางส่วนเพื่อช่วยประมาณความเสี่ยงและสร้างพอร์ต

## Reported Evidence

งานของ DeMiguel, Plyakha, Uppal และ Vilkov รายงานว่าการใช้ implied volatility/correlation โดยตรงมี noise สูง แต่ volatility risk premium และ option-implied skewness ช่วยประสิทธิภาพพอร์ตในตัวอย่าง โดย Sharpe ที่รายงานดีขึ้นประมาณ 30–400% สำหรับ daily rebalancing และ 11–87% สำหรับ monthly rebalancing

## Critical Reconciliation

ตัวเลขดังกล่าวเป็นผลในงานวิจัย ไม่ใช่ผลตอบแทนรับประกัน และ daily implementation มี turnover/cost สูง ควรแยก Q จาก P อย่างชัดเจน ทดสอบวิธีแปลง risk premia, ดู bid-ask/liquidity และทำ net-of-cost out-of-sample replication ก่อนใช้งานจริง

## Sources

- [Original Facebook post](https://www.facebook.com/permalink.php?story_fbid=pfbid0QzHQGb73ECjhovnGXw4krEu8HbfixvYotJckjEeoSZ14AVhgmAUKoUMfk2ERm6Pil&id=61569334229421&__cft__[0]=AZaCgyeKSPVhQN43-Shq8W6P1YXl6ZuGyMz3SFNnqOKzNuA-JfOjdfAurJPDGwY0msIGw94JdJl_KZg4LI4FIKcwNYosL4Y1-45_XsStI5ajfCr0sTjWn6c0t5Qv5_zbr0NRMqWynMg4bHRILhauHa39tR8HNxeOo5DXGttUo47KKQ&__tn__=%2CO%2CP-R)
- [Paper record](https://cepr.org/publications/dp12042)




