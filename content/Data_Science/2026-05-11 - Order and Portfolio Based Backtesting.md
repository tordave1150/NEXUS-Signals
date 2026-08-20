---
title: Order-Based และ Portfolio-Based Backtesting
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Software Engineering]
concepts: [Backtesting, Order Lifecycle, NAV, Rebalancing]
entities: [InvestorStack]
tags: [backtesting, portfolio, pnl]
source_type: Facebook Post
source_title: เมื่อ AI เขียน Backtest ให้ทั้งระบบ
source_author: InvestorStack
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-069__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-069__"
source_date: 2026-05-11
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: summarized
confidence: Medium
related: ["[[Backtesting]]", "[[Portfolio Accounting]]"]
---

# Order-Based และ Portfolio-Based Backtesting

> [!summary] TL;DR
> แยก backtest ตามหน่วยบัญชี: order/trade-based จับคู่ lifecycle ของคำสั่งและ P&L รายไม้ ส่วน portfolio-based คำนวณ holdings, cash, weights, rebalancing และ NAV ของหลายสินทรัพย์ตามเวลา

## Core Flows

- Order-based: market data → strategy → signals → fills/order matching → P&L → metrics
- Portfolio-based: multi-asset data → selection/weights → allocation/rebalancing → NAV → risk-adjusted metrics

## Caveat

Flow ดูตายตัวแต่รายละเอียดไม่ตายตัว AI ที่เขียน code เร็วไม่ได้รับประกัน correctness ต้องกำหนด clock/calendar, corporate actions, dividends, FX, borrow, partial fills, latency, fees, taxes, cash constraints และ look-ahead controls พร้อม golden tests และ reconciliation กับตัวอย่างคำนวณมือ

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-069__)

