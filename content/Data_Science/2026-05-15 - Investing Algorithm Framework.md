---
title: Investing Algorithm Framework
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Python]
concepts: [Vector Backtesting, Event-Driven Backtesting, Strategy Deployment]
entities: [Investing Algorithm Framework, CCXT]
tags: [backtesting, algorithmic-trading, python]
source_type: Facebook Post
source_title: Framework สำหรับ Algorithmic Trading
source_author: GroundUp Academy
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-078__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-078__"
source_date: 2026-05-15
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Backtesting]]", "[[Trading Bot]]"]
---

# Investing Algorithm Framework

> [!summary] TL;DR
> Python framework ที่พยายามใช้ strategy class เดียวตลอดวงจร research → vector screening → event-driven validation → comparison dashboard → live deployment

## Verification & Caveat

Repository ทางการยืนยัน vector/event-driven backtesting, HTML comparison dashboard, metrics และ live connectivity ผ่าน CCXT จุดเด่นคือช่วยลดการเขียน logic ซ้ำระหว่าง research/production แต่ “same class” ไม่ได้ลบช่องว่างระหว่าง simulation กับ exchange

ต้องตรวจ data timestamps, fill model, order semantics, rate limits, retries, idempotency, partial fills, secrets, reconciliation และ kill switch รวมถึง license/maintenance ก่อน production

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-078__)
- [Official investing-algorithm-framework repository](https://github.com/coding-kitties/investing-algorithm-framework)


