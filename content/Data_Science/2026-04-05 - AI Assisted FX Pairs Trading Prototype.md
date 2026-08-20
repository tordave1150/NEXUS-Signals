---
title: AI-Assisted FX Pairs Trading Prototype
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Artificial Intelligence]
concepts: [Pairs Trading, Cointegration, Mean Reversion]
entities: [QuantCorner, Alpha Vantage]
tags: [pairs-trading, cointegration, ai]
source_type: Facebook Post
source_title: Claude Code ทำ FX Pairs Trading
source_author: QuantCorner
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid0RB6VAepj93MyLif2T9GvN6N8EfKkhBZWJJMuGr8rEfgXT2pg1RydUDm9dBrJ5u56l?__cft__[0]=AZbOQv3zI3O9GSPtsJUC49pP9eGbEL-_a7kYpA4abfrL7EyrfVJF-RGfE3e6NlPHKGPISF1DBh0yQB3UafifWs_cvWGI28bNMy3I43wWW-LkbtsJPpRegGXCOV_VzhxDHcHBVr5vxk1uYgJLSfHoB6K_IX-MtcWU1JLg3s9XksSRPQ&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid0RB6VAepj93MyLif2T9GvN6N8EfKkhBZWJJMuGr8rEfgXT2pg1RydUDm9dBrJ5u56l"
source_date: 2026-04-05
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: Low-Medium
related: ["[[Pairs Trading]]", "[[Cointegration]]"]
---

# AI-Assisted FX Pairs Trading Prototype

> [!summary] TL;DR
> Claude Code สร้าง prototype ตั้งแต่ดึง 20 FX pairs, Engle–Granger, hedge ratio/half-life, z-score signals, backtest และ dashboard ได้เร็ว แต่ผล Sharpe 1.8 ยังไม่ใช่หลักฐาน alpha

## Verification & Reconciliation

คู่เงินมี triangular dependencies, non-synchronous closes และ macro regimes; pair selection ด้วย p<0.10 หลายคู่เสี่ยง multiple testing Cointegration ไม่รับประกัน stable spread และต้องทดสอบทั้ง legs, bid–ask, carry/swap, execution timing และ parameter re-estimation ตัวเลข annual return ~6%, max drawdown 2–4% ไม่มีช่วงข้อมูล/ต้นทุน/code จึงตรวจซ้ำไม่ได้

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid0RB6VAepj93MyLif2T9GvN6N8EfKkhBZWJJMuGr8rEfgXT2pg1RydUDm9dBrJ5u56l?__cft__[0]=AZbOQv3zI3O9GSPtsJUC49pP9eGbEL-_a7kYpA4abfrL7EyrfVJF-RGfE3e6NlPHKGPISF1DBh0yQB3UafifWs_cvWGI28bNMy3I43wWW-LkbtsJPpRegGXCOV_VzhxDHcHBVr5vxk1uYgJLSfHoB6K_IX-MtcWU1JLg3s9XksSRPQ&__tn__=%2CO%2CP-R)
