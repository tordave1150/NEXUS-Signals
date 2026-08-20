---
title: ATR Percentile Volatility Regimes
note_type: source
primary_topic: Investment
secondary_topics: [Data_Science, Technical Analysis]
concepts: [ATR Percent, Volatility Regime, Regime Filter]
entities: [TradingView]
tags: [volatility, atr, regime-filter]
source_type: Facebook Post
source_title: Indicator สำหรับ Volatility Regime
source_author: Investic Academy
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-073__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-073__"
source_date: 2026-05-13
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: summarized
confidence: Medium
related: ["[[Volatility Regime]]", "[[ATR]]"]
---

# ATR Percentile Volatility Regimes

> [!summary] TL;DR
> แปลง ATR เป็นเปอร์เซ็นต์ของราคาและเทียบกับ distribution ในอดีต เพื่อจัดระดับ compression, quiet, normal และ elevated พร้อม phase ว่าความผันผวนกำลัง rising, falling, topping หรือ bottoming

## Use as a Filter

Regime label ไม่ได้บอก long/short แต่ใช้ปรับ position size, stop distance, breakout/mean-reversion eligibility และ execution assumptions ทิศทางยังต้องมาจาก price structure, trend, momentum หรือ volume

## Caveat

ต้องกำหนด ATR length, percentile window, thresholds และ phase logic ชัดเจน ระวัง window leakage, instrument/timeframe dependence และ label instability ใกล้ threshold ควรทดสอบว่า filter เพิ่มผลลัพธ์ out-of-sample หลัง costs มากกว่าการเพิ่ม complexity

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-073__)


