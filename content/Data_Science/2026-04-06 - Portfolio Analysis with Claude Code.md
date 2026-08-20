---
title: Portfolio Analysis ด้วย Claude Code
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Artificial Intelligence]
concepts: [Strategy Portfolio, Correlation, Structural Risk]
entities: [QuantCorner]
tags: [portfolio-analysis, risk-management, ai]
source_type: Facebook Post
source_title: Claude Code for Portfolio Analysis
source_author: QuantCorner
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid02DWs9NWc5F3Qt3Ebj9KaM9bt5gk2AdY9sMyfUs1kudkT1FGxzy4yd5DtupyqdJmWHl?__cft__[0]=AZZUdaoTIoRyYGmJjKyI_xEkgNdftv-Aje6hfJpbyCMyAPs5yjg9YndAXD84uJYZb9ncbv6fqCmRb0pvUbDtt-s1Fa80FBtq7tMCFU-c1OaxDZwaCMlRR9k_b8q4PUJ_MYmN8LAb_Mbb9Vgng3n5uSKG2sRVrFIJfW55V4KTxno1VA&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid02DWs9NWc5F3Qt3Ebj9KaM9bt5gk2AdY9sMyfUs1kudkT1FGxzy4yd5DtupyqdJmWHl"
source_date: 2026-04-06
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: Low-Medium
related: ["[[Portfolio Risk]]", "[[Alpha Portfolio]]"]
---

# Portfolio Analysis ด้วย Claude Code

> [!summary] TL;DR
> พอร์ตกลยุทธ์ต้องวิเคราะห์ standalone, interaction และ structural risk ไม่ใช่รวมกลยุทธ์ที่ Sharpe สูงหลายตัวแล้วถือว่ากระจายความเสี่ยง

## Important Details

โพสต์วิเคราะห์ 19 strategies ด้วย cumulative returns, drawdowns, rolling correlation, regime performance, tail risk, clustering และ alpha decay รายงานว่า 7 alpha กำลังเสื่อม, 8 all-weather และ average pairwise correlation 0.152

## Verification & Reconciliation

ตัวเลขทั้งหมดไม่มี dataset/code/definition ให้ตรวจ “all-weather” และ “alpha decay” ต้องมีเกณฑ์ล่วงหน้า Correlation เฉลี่ยต่ำอาจซ่อน tail dependence และ cluster concentration การแบ่ง risk เป็นสาม layers เป็นกรอบคิดที่มีประโยชน์ แต่ไม่ใช่มาตรฐานวัดเดียว

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid02DWs9NWc5F3Qt3Ebj9KaM9bt5gk2AdY9sMyfUs1kudkT1FGxzy4yd5DtupyqdJmWHl?__cft__[0]=AZZUdaoTIoRyYGmJjKyI_xEkgNdftv-Aje6hfJpbyCMyAPs5yjg9YndAXD84uJYZb9ncbv6fqCmRb0pvUbDtt-s1Fa80FBtq7tMCFU-c1OaxDZwaCMlRR9k_b8q4PUJ_MYmN8LAb_Mbb9Vgng3n5uSKG2sRVrFIJfW55V4KTxno1VA&__tn__=%2CO%2CP-R)
