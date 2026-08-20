---
title: Order Flow and Cryptocurrency Returns
note_type: source
primary_topic: Investment
secondary_topics: [Cryptocurrency, Market Microstructure]
concepts: [Order Flow, Aggressor Side, Return Prediction]
entities: [Alexia Anastasopoulos, Nikola Gradojevic, Fred Liu, Alex Maynard, Ilias Tsiakas]
tags: [order-flow, cryptocurrency, machine-learning]
source_type: Facebook Post and Research Paper
source_title: Order Flow and Cryptocurrency Returns
source_author: PopQuants and paper authors
source_url: "https://www.facebook.com/popquants/posts/pfbid02RpfMwuuwE9GBZUR5VdcTYcT8ckmLRB9hbQkaWJiS3LRveMs5SdFGhDmbCPA4do4yl?__cft__[0]=AZayia7Y09xHlpkUGhyQbZPDGQrmK-N05wG3D9AZtOGIsk6S4nyuVmpu8V4Uditwu_NCXygYxL8djj5CPVySHLLNbOH0U0DkUYk4-zQWTqzphCeEFpS2jozNNkUNraxflBWLwcUbBo4bp_mP7FvGl4bJtAwSybycRnUSM-fIuy1saw&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02RpfMwuuwE9GBZUR5VdcTYcT8ckmLRB9hbQkaWJiS3LRveMs5SdFGhDmbCPA4do4yl"
source_date: 2026-06-18
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Order Flow]]", "[[Cryptocurrency Returns]]"]
---

# Order Flow and Cryptocurrency Returns

## Main Idea

Order flow แยกแรงซื้อ/ขายเชิงรุกจาก volume รวม: การซื้อที่ offer สะท้อน aggressive buy และการขายที่ bid สะท้อน aggressive sell งานวิจัยถามว่าข้อมูลนี้ช่วยอธิบายหรือทำนายผลตอบแทนคริปโตได้หรือไม่

## Verified Findings

บทความของ Anastasopoulos, Gradojevic, Liu, Maynard และ Tsiakas รายงานว่า ML models ที่ condition บน order flow มีมูลค่าทางเศรษฐกิจสำหรับ long-only strategy ในตัวอย่าง และ standardized order flow มี distribution ที่จัดการง่ายกว่าผลตอบแทนซึ่ง skew/kurtosis สูง

## Caveat

คำว่า “ทำกำไรได้จริง” ในโพสต์กว้างกว่าหลักฐานใน sample ต้องตรวจ data venue, cross-exchange aggregation, stablecoin quote conversion, fees, slippage, market impact, survivorship และ publication-era competition ผล out-of-sample ใน paper ไม่รับประกัน live alpha หลังต้นทุน

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02RpfMwuuwE9GBZUR5VdcTYcT8ckmLRB9hbQkaWJiS3LRveMs5SdFGhDmbCPA4do4yl?__cft__[0]=AZayia7Y09xHlpkUGhyQbZPDGQrmK-N05wG3D9AZtOGIsk6S4nyuVmpu8V4Uditwu_NCXygYxL8djj5CPVySHLLNbOH0U0DkUYk4-zQWTqzphCeEFpS2jozNNkUNraxflBWLwcUbBo4bp_mP7FvGl4bJtAwSybycRnUSM-fIuy1saw&__tn__=%2CO%2CP-R)
- [Journal article](https://www.sciencedirect.com/science/article/pii/S1386418126000029)
- [Research paper PDF](https://www.efmaefm.org/0EFMAMEETINGS/EFMA%20ANNUAL%20MEETINGS/2025-Greece/papers/OrderFlowpaper.pdf)


