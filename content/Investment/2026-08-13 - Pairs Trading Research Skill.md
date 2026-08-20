---
title: Pairs Trading Research Skill
note_type: source
primary_topic: Investment
secondary_topics: [Statistical Arbitrage, Research Automation]
concepts: [Cointegration, False Discovery Rate, Formation OOS Split, Cost-Aware Backtest]
entities: [pairs-trading-research-skill, Nutdnuy]
tags: [pairs-trading, cointegration, validation]
source_type: Facebook Post and GitHub Repository
source_title: pairs-trading-research-skill
source_author: QuantCorner and Nutdnuy
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid02KNQ8Wc5PYPfWaeLsUQDa9Z6XGoC7UZUWFABjCHZJHgxzsRWc1kZ2u5P2xK2La2wVl?__cft__[0]=AZaC1MsM4rbmDEGDn8p-q5w39EJCI8_BNLyJDEkjytcApG3ycLTydDeeRGEKZGIfowce7_vPhBWuee8rCCCjTQK8JOeslbqVvQ7nqzrwQukc31yoiwXpTZlxA0SpnhK6wT1BYrvj6NgY4o3Pja7JqPN-1EWCO7Nw62iN2TPP4jYqAw&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid02KNQ8Wc5PYPfWaeLsUQDa9Z6XGoC7UZUWFABjCHZJHgxzsRWc1kZ2u5P2xK2La2wVl"
source_date: 2026-08-13
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: verified
confidence: High
related: ["[[Pairs Trading]]", "[[Cointegration Research]]"]
---

# Pairs Trading Research Skill

## Verified Workflow

repository ให้ workflow ที่ตรวจสอบย้อนหลังได้สำหรับค้นหาและทดสอบคู่: ลด candidate ด้วย PCA/DBSCAN, ทดสอบ Engle-Granger และ ADF, วัด half-life/zero crossings/rolling stability, ควบคุม false discovery ด้วย Benjamini-Hochberg แล้วล็อก formation/OOS split ก่อน backtest rolling z-score พร้อม transaction cost, borrow cost และ turnover

## Boundaries

ระบบสร้าง metrics และ audit report แต่ `pass` ไม่ได้ยืนยันเหตุผลเชิงเศรษฐกิจ, borrow availability, liquidity, market impact, คุณภาพ corporate action หรือการไม่มี survivorship/selection bias ตัว repository เป็น research tool และไม่เชื่อม broker หรือส่งคำสั่งซื้อขาย

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid02KNQ8Wc5PYPfWaeLsUQDa9Z6XGoC7UZUWFABjCHZJHgxzsRWc1kZ2u5P2xK2La2wVl?__cft__[0]=AZaC1MsM4rbmDEGDn8p-q5w39EJCI8_BNLyJDEkjytcApG3ycLTydDeeRGEKZGIfowce7_vPhBWuee8rCCCjTQK8JOeslbqVvQ7nqzrwQukc31yoiwXpTZlxA0SpnhK6wT1BYrvj6NgY4o3Pja7JqPN-1EWCO7Nw62iN2TPP4jYqAw&__tn__=%2CO%2CP-R)
- [Repository URL from queue](https://github.com/nutdnuy/pairs-trading-research-skill?fbclid=IwY2xjawTuxWlwZG9mAWV4dG4DYWVtAjEwAGJyaWQRMU9kTGJLWFFxZFF2MTVxb2xzcnRjBmFwcF9pZBAyMjIwMzkxNzg4MjAwODkyAAEeTso3QLe9AR-ZaBGyEfxt6HOme9YUWCbCIQ134hxqdnvuxMEhRQOFOT8nmQQ_aem_X8SCkXjFW3uzEx_l8yO-Ig)
- [Canonical repository](https://github.com/nutdnuy/pairs-trading-research-skill)




