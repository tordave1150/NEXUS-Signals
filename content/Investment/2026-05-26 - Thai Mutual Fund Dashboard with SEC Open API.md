---
title: Thai Mutual Fund Dashboard with SEC Open API
note_type: source
primary_topic: Investment
secondary_topics: [Data_Science, Mutual Funds]
concepts: [NAV, Fund Comparison, Local Proxy]
entities: [SEC Thailand, InvestorStack]
tags: [thai-mutual-funds, sec-api, dashboard]
source_type: Facebook Post
source_title: ให้ AI สร้าง Dashboard กองทุนไทย
source_author: InvestorStack
source_url: "https://www.facebook.com/InvestorStack/posts/pfbid0fwJUvLJhiSdGxmoujKvbWsJ71Uqnn8UcDffUyMQ9uKqZEesJ3bJQvpcTWXjxj6kPl?__tn__=%2CO*F"
canonical_url: "https://www.facebook.com/InvestorStack/posts/pfbid0fwJUvLJhiSdGxmoujKvbWsJ71Uqnn8UcDffUyMQ9uKqZEesJ3bJQvpcTWXjxj6kPl"
source_date: 2026-05-26
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Mutual Fund NAV]]", "[[SEC Open API]]"]
---

# Thai Mutual Fund Dashboard with SEC Open API

> [!summary] TL;DR
> แนวทางสร้าง dashboard กองทุนไทยด้วย SEC Open API โดยใช้ Node proxy เก็บ subscription keys ฝั่ง server, cache รายชื่อกองทุน/NAV และคำนวณ return, annualized volatility, max drawdown, Sharpe และ normalized NAV

## Critical Reconciliation

SEC Developer Portal ยืนยันบริการ Fund Factsheet/Fund Daily Info แต่ endpoint และการสมัครใช้งานอาจเปลี่ยนหลังการย้าย portal ต้องเช็ก schema สดก่อนเขียน production code สูตรใน prompt มีข้อควรระวัง: NAV ไม่รวมทุกมิติของ total return, Sharpe ที่ fix risk-free 1.5% อาจไม่เหมาะ และการเทียบ share class ต้องจับ `proj_id`/`class_abbr_name` อย่างถูกต้อง

## Sources

- [Original Facebook post](https://www.facebook.com/InvestorStack/posts/pfbid0fwJUvLJhiSdGxmoujKvbWsJ71Uqnn8UcDffUyMQ9uKqZEesJ3bJQvpcTWXjxj6kPl?__tn__=%2CO*F)
- [SEC API Developer Portal changes](https://api-portal.sec.or.th/changes)

