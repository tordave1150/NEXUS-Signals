---
title: Hybrid Financial Sentiment Data Funnel
note_type: source
primary_topic: Investment
secondary_topics: [Data_Science, Natural Language Processing]
concepts: [FinBERT, LLM Gatekeeper, Market Neutral, Tail Risk]
entities: [Gemini, Johannes Stübinger, Luis Wöhner]
tags: [financial-sentiment, finbert, llm]
source_type: Facebook Post
source_title: Edge อยู่ที่การกรองข่าวไหนควรทิ้ง
source_author: Investic Academy
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-068__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-068__"
source_date: 2026-05-12
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Financial Sentiment]]", "[[Market Neutral]]"]
---

# Hybrid Financial Sentiment Data Funnel

> [!summary] TL;DR
> งานวิจัยใช้ FinBERT คัด sentiment ปริมาณมาก แล้วให้ Gemini เป็น contextual gatekeeper กรอง novelty, relevance, price impact และ prior expectations ก่อนสร้าง dollar-neutral long/short signals

## Reported Results

งานรายงานข้อมูลมากกว่า 9 ล้านรายการและช่วงทดสอบ 16 ปี โดย mean excess return 51.02% ต่อปีหลัง transaction costs, Sharpe 1.06 และ Sortino 2.61 ตัวเลขในโพสต์เรื่อง max drawdown ราว 64%, volatility ราว 49%, skewness 6.11 และ kurtosis 68.2 ชี้ว่าผลตอบแทนมี tail dependence สูงและค่าเฉลี่ยอาจถูกขับโดยเหตุการณ์ไม่กี่ครั้ง

## Reconciliation

ผลเป็น proof-of-concept ของ pipeline ไม่ใช่หลักฐานว่า LLM trading ชนะตลาดได้ทั่วไป ต้องตรวจ universe construction, point-in-time data, prompt/model version stability, cost assumptions, exposure neutrality และ sensitivity ต่อ tail events ก่อนทำซ้ำ

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-068__)
- [Hybrid Sentiment Analysis in Financial Markets](https://doi.org/10.3390/ai7040138)


