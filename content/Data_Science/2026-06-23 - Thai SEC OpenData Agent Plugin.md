---
title: Thai SEC OpenData Agent Plugin
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Agent Skills]
concepts: [SEC Open API, Agent Plugin, Data Pipeline]
entities: [Thai SEC, sec-opendata-th, Codex, Claude Code]
tags: [thai-sec, plugin, open-data]
source_type: Facebook Post and GitHub Repository
source_title: sec-opendata-th
source_author: QuantCorner and nutdnuy
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid02418p1Q3ZH95yFcLE8FAZbrhG42VtRBbB9CimxkrxiLjoE5dUX7g31BecjtiT4v4tl?__cft__[0]=AZbTuz7AKJG054-Oklk-7RcSGX-XzeZZ7uCd8ldTf7oYU88Qg29OPI511r8tHRm5QgPrRJsfyBFk1c4mMHhQBx01kIH4teGtG9Qx9IYOK8oMH06KQ0xk7yksP2qAH7HtarN88HQ806eizYkBbulKGlkHjER-zVaXmuwfUtNWRgmVfw&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid02418p1Q3ZH95yFcLE8FAZbrhG42VtRBbB9CimxkrxiLjoE5dUX7g31BecjtiT4v4tl"
source_date: 2026-06-23
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Thai SEC Open API]]", "[[Agent Skill]]"]
---

# Thai SEC OpenData Agent Plugin

## What It Does

`sec-opendata-th` เป็น Python client พร้อม plugin/skill สำหรับ Codex และ Claude Code ใช้ดึงข้อมูลตลาดทุนไทยจาก SEC OpenAPI เช่น funds, NAV, factsheets, bonds, PVD, digital assets, licence checks และ One Report/56-1

## Setup Summary

- สร้าง subscription key ที่ SEC API Developer Portal
- ใช้ `SEC_API_KEY` เป็น fallback หรือแยก key ตาม product/category
- Repository มี `.codex-plugin/plugin.json`, marketplace metadata และ skill `sec-open-api`
- ฝั่ง Claude มี marketplace/plugin manifests และ slash commands เช่นค้นกองทุน NAV และ generic request

## Verification & Security

README ทางการยืนยันขอบเขต endpoint, การติดตั้ง และ MIT license รวมถึงระบุว่า portal เก่าหยุดใช้ 30 มิถุนายน 2026 ห้ามใส่ key ใน chat, screenshot, repository หรือ log ควรใช้ secret manager/environment ที่จำกัดสิทธิ์ ตรวจ schema และเก็บ raw responses/retrieval timestamps เพราะ API และข้อมูลอาจเปลี่ยน

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid02418p1Q3ZH95yFcLE8FAZbrhG42VtRBbB9CimxkrxiLjoE5dUX7g31BecjtiT4v4tl?__cft__[0]=AZbTuz7AKJG054-Oklk-7RcSGX-XzeZZ7uCd8ldTf7oYU88Qg29OPI511r8tHRm5QgPrRJsfyBFk1c4mMHhQBx01kIH4teGtG9Qx9IYOK8oMH06KQ0xk7yksP2qAH7HtarN88HQ806eizYkBbulKGlkHjER-zVaXmuwfUtNWRgmVfw&__tn__=%2CO%2CP-R)
- [Official repository](https://github.com/nutdnuy/sec-opendata-th)
- [SEC Open Data portal](https://secopendata.sec.or.th/)


