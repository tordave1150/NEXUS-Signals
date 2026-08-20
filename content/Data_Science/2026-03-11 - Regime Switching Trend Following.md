---
title: Trend Following ด้วย Regime-Switching Model
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Statistics]
concepts: [Trend Following, Markov Switching, Market Regime]
entities: [Chaipat Nengcomma]
tags: [trend-following, regime-switching, quantitative-finance]
source_type: Facebook Post
source_title: Optimal Trend Following Rules in Two-State Regime-Switching Models
source_author: Chaipat Nengcomma
source_url: "https://www.facebook.com/chaipat.ncm/posts/pfbid0GSoB3rETNxdavGJBTgaBw35apbDQFYG9skB4THga1sF8NgbDXAJHR4KfUHWZJed9l?__cft__[0]=AZaTqlNWo7w3fLj5i2okHavH2s3F49YNZfR3LJ2UN8N6aOHm2MuCyNhs5cmtYIR_0ZJ6stw50xOnK7xNQfvEDxk0Z6il-0cVCmLEGOUjMM0I2WwPCL2xnpYCWrA6t0jubHh6Mz8jNomHoz6kvodMETXkooHI68k8qMQgQbPC48MEdQ&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/chaipat.ncm/posts/pfbid0GSoB3rETNxdavGJBTgaBw35apbDQFYG9skB4THga1sF8NgbDXAJHR4KfUHWZJed9l"
source_date: 2026-03-11
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: Medium
related: ["[[Trend Following]]", "[[Market Regime]]"]
---

# Trend Following ด้วย Regime-Switching Model

> [!summary] TL;DR
> โมเดล regime switching พยายามปรับ trend rule ให้เข้ากับสถานะ bull/bear และ duration dependence แทนการใช้ SMA/EMA/Momentum ค่าคงที่ในทุกตลาด

## Important Details

โพสต์อธิบาย Expanded-State Markov Switching Model ที่รวม short-term momentum กับ medium-term mean reversion เพื่อประมาณ transition ระหว่างสองสถานะ และอ้างว่าผลทดสอบเหนือ buy-and-hold, EMA(10) และ MOM(12)

## Verification & Reconciliation

ยังไม่มีชื่อผู้เขียน ลิงก์ paper dataset ตลาด ช่วงเวลา ต้นทุน และกติกา out-of-sample ในข้อความหลัก จึงยังไม่ควรถือผล outperform เป็นหลักฐานทั่วไป Regime models มีความเสี่ยงจาก look-ahead, unstable transition probabilities และ state-label ambiguity

## Things Worth Remembering

ประโยชน์หลักคือการคิดแบบ conditional strategy; ต้องตรวจว่า regime signal ใช้ข้อมูลที่มีอยู่จริง ณ เวลาเทรดและยังได้ผลหลัง costs

## Sources

- [Original Facebook post](https://www.facebook.com/chaipat.ncm/posts/pfbid0GSoB3rETNxdavGJBTgaBw35apbDQFYG9skB4THga1sF8NgbDXAJHR4KfUHWZJed9l?__cft__[0]=AZaTqlNWo7w3fLj5i2okHavH2s3F49YNZfR3LJ2UN8N6aOHm2MuCyNhs5cmtYIR_0ZJ6stw50xOnK7xNQfvEDxk0Z6il-0cVCmLEGOUjMM0I2WwPCL2xnpYCWrA6t0jubHh6Mz8jNomHoz6kvodMETXkooHI68k8qMQgQbPC48MEdQ&__tn__=%2CO%2CP-R)
