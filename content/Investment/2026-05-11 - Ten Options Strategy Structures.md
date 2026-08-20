---
title: สิบโครงสร้างกลยุทธ์ Options
note_type: source
primary_topic: Investment
secondary_topics: [Derivatives, Risk Management]
concepts: [Covered Call, Protective Put, Vertical Spread, Straddle, Iron Condor]
entities: [QuantCorner]
tags: [options, derivatives, payoff]
source_type: Facebook Post
source_title: 10 กลยุทธ์ Option
source_author: QuantCorner
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-065__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-065__"
source_date: 2026-05-11
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Options]]", "[[Option Payoff]]"]
---

# สิบโครงสร้างกลยุทธ์ Options

> [!summary] TL;DR
> เลือกโครงสร้าง options จากการถือ underlying, มุมมองทิศทาง, implied volatility, ระยะเวลา และ payoff ที่ยอมรับได้ ไม่ใช่จากชื่อกลยุทธ์เพียงอย่างเดียว

## Strategy Map

- ถือหุ้นและสร้างรายได้/hedge: covered call, married put, protective collar
- มองขึ้นหรือลงแบบมีกรอบ: bull call spread, bear put spread
- คาดการเคลื่อนไหวแรงแต่ไม่เลือกทิศ: long straddle, long strangle
- คาดราคาอยู่ใกล้ช่วงเป้าหมาย: long call butterfly, iron condor, iron butterfly

## Reconciliation

คำอธิบาย payoff หลักสอดคล้องกับ Options Industry Council แต่สิทธิ exercise “ก่อนวันหมดอายุ” ใช้กับ American-style options; European-style exercise ได้ที่ expiry เท่านั้น ผลจริงยังขึ้นกับ premium, IV change, theta, dividends, assignment, liquidity และค่าธรรมเนียม

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-065__)
- [Options Industry Council — All Strategies](https://www.optionseducation.org/strategies/all-strategies-en)


