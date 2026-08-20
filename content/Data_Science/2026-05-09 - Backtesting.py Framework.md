---
title: Backtesting.py Framework
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Python]
concepts: [Event-Driven Backtest, Parameter Optimization, Trading Simulation]
entities: [Backtesting.py, Kernc]
tags: [backtesting-py, python, trading]
source_type: Facebook Post
source_title: Kernc Backtesting.py
source_author: DeepRepo.ai
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-071__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-071__"
source_date: 2026-05-09
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Backtesting]]", "[[Python]]"]
---

# Backtesting.py Framework

> [!summary] TL;DR
> Python framework ที่ให้ subclass `Strategy`, กำหนด indicators และ logic ใน `init`/`next`, รัน backtest, ดูสถิติ/กราฟ และค้น parameter combinations

## Verification & Caveat

Repository ทางการยืนยัน API, optimizer, composable strategies, detailed results และ interactive visualizations แต่คำว่า “ข้อมูลจริง” ในโพสต์ควรหมายถึง historical data ที่ผู้ใช้ป้อน ไม่ใช่การรับรองคุณภาพ data หรือความสมจริงของ fills

ค่า commission ถูกคิดตอนเข้าและออก, spread เป็น input คงที่ และ fractional trading มีข้อจำกัด ผู้ใช้ยังต้องจัดการ corporate actions, slippage, liquidity, look-ahead และ out-of-sample validation เอง การ optimize เร็วเพิ่มความเสี่ยง overfitting หากไม่มี multiple-testing controls

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-071__)
- [Official Backtesting.py repository](https://github.com/kernc/backtesting.py)


