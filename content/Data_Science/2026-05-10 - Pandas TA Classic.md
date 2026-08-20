---
title: Pandas TA Classic - Technical Indicators for Pandas
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Python]
concepts: [Technical Indicators, Feature Engineering, Pandas Extension]
entities: [Pandas TA Classic, TA-Lib]
tags: [pandas-ta, technical-analysis, python]
source_type: Facebook Post
source_title: Xgboosted Pandas TA Classic
source_author: DeepRepo.ai
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-064__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-064__"
source_date: 2026-05-10
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Technical Analysis]]", "[[Feature Engineering]]"]
---

# Pandas TA Classic - Technical Indicators for Pandas

> [!summary] TL;DR
> Community-maintained Pandas extension สำหรับคำนวณ technical indicators และ candlestick patterns โดยทำงานได้แม้ไม่ติดตั้ง TA-Lib และใช้สร้าง features สำหรับ research/backtest ได้

## Verification & Reconciliation

README ปัจจุบันระบุ 192 indicators/utilities และ 62 native candlestick patterns รวม 252 รายการเฉพาะ โดย TA-Lib เป็น optional accelerator/oracle สำหรับบาง indicators ไม่ใช่ dependency บังคับ ตัวเลข “มากกว่า 200” ในโพสต์จึงถูกในภาพรวมแต่ควรอ้างเวอร์ชัน

Indicator library ช่วยคำนวณ feature ไม่ได้พิสูจน์ว่า signal มี edge ต้องควบคุม look-ahead, warm-up, parameter search, multiple testing และ transaction costs

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-064__)
- [Official pandas-ta-classic repository](https://github.com/xgboosted/pandas-ta-classic)

