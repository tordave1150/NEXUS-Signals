---
title: Mislearning ของ Factor Premia เมื่อเกิด Structural Break
note_type: source
primary_topic: Investment
secondary_topics: [Statistics, Data_Science]
concepts: [Structural Break, Bayesian Learning, Factor Premia, Predictive Likelihood Ratio]
entities: [Yimeng Qiu, PopQuants]
tags: [factor-investing, structural-break, bayesian]
source_type: Facebook Post
source_title: กลยุทธ์แย่ลงหรือว่าตลาดเปลี่ยนไปแล้ว
source_author: PopQuants
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-057__"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xlURL-057__"
source_date: 2026-05-05
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Structural Break]]", "[[Factor Investing]]"]
---

# Mislearning ของ Factor Premia เมื่อเกิด Structural Break

> [!summary] TL;DR
> เปรียบเทียบ stable model กับ break-aware model ผ่าน predictive likelihood ratio เพื่อวัดว่า observation ล่าสุดสอดคล้องกับโลกที่มี structural break มากกว่าโลกที่ premium เปลี่ยนช้าหรือไม่

## Core Idea

โพสต์ยกตัวอย่าง `Δt = log(pB/pS)` เมื่อ likelihood ภายใต้ break model สูงกว่าจะได้ Δt สูง บ่งชี้ว่าโมเดลที่ประเมิน structural change ต่ำอาจกำลังเรียนรู้ผิด แต่ไม่ใช่สัญญาณให้ short factor โดยอัตโนมัติ

## Verification & Correction

พบ paper ต้นทาง *Mislearning of Factor Risk Premia under Structural Breaks* ซึ่งนิยาม mislearning intensity จาก predictive likelihood ratios ตรงกับโพสต์ อย่างไรก็ตามข้อเสนอท้ายโพสต์ว่า “ควร update โมเดล” เป็นคำแนะนำทั่วไป ไม่ใช่ผลเชิงกลยุทธ์ของ paper: abstract ระบุว่าผลลัพธ์ภายหลังแตกต่างตาม factor system/anomaly family และ Δt สูงไม่ได้ทำนาย short-run collapse แบบ deterministic

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-057__)
- [Qiu — Mislearning of Factor Risk Premia under Structural Breaks](https://arxiv.org/abs/2603.21672)


