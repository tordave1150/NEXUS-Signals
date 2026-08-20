---
title: LLM Stock Forecasting Review from a Hedge Fund Perspective
note_type: source
primary_topic: Investment
secondary_topics: [Data_Science, Machine Learning]
concepts: [Data Leakage, Transaction Costs, Time-Series Validation]
entities: [Olivia Zhang, Zhilin Zhang, arXiv]
tags: [llm-finance, data-leakage, evaluation]
source_type: Facebook Post
source_title: รีวิว LLM สำหรับทำนายราคาหุ้น
source_author: PopQuants
source_url: "https://www.facebook.com/popquants/posts/pfbid0isfp6Vh7yQ5PBy65ssWmqQPMNKsXzXUBiCjEMTgstFLAkuWfbS1G8aQJG7upaFaFl?__tn__=%2CO*F"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid0isfp6Vh7yQ5PBy65ssWmqQPMNKsXzXUBiCjEMTgstFLAkuWfbS1G8aQJG7upaFaFl"
source_date: 2026-05-27
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Data Leakage]]", "[[Walk Forward Validation]]"]
---

# LLM Stock Forecasting Review from a Hedge Fund Perspective

> [!summary] TL;DR
> Review paper แบ่งงาน LLM-for-stock-forecasting เป็น sentiment, filings/earnings calls, cross-asset relationships, tokenized time series และ multi-agent trading พร้อมชี้ว่า dataset สั้น, leakage, metric ไม่ตรง P&L และ market frictions ทำให้ผลวิจัยดูดีเกินจริง

## Practical Checklist

- ใช้ forward-only rolling/expanding splits และ group events เพื่อกัน leakage
- ครอบคลุมหลาย market regimes และ deduplicate inputs
- วัด P&L, Sharpe/Sortino, max drawdown, turnover และ capacity หลัง costs
- เทียบ transparent non-LLM baseline ไม่ใช่เฉพาะ LLM อื่น

## Verification

หน้า arXiv ยืนยันชื่อผู้เขียน ขอบเขต และ acceptance ใน IEEE Conference on Artificial Intelligence ปี 2026 ตัวเลข compounding/cost ในโพสต์เป็นตัวอย่างเชิงสมมติ ไม่ควรถูกอ่านเป็นผล strategy จริง

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid0isfp6Vh7yQ5PBy65ssWmqQPMNKsXzXUBiCjEMTgstFLAkuWfbS1G8aQJG7upaFaFl?__tn__=%2CO*F)
- [arXiv:2605.05211](https://arxiv.org/abs/2605.05211)

