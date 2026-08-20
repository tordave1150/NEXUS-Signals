---
title: AI Generated Stock Dashboard with Twelve Data
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Web Development]
concepts: [Market Data API, Vanilla JavaScript, Local Storage]
entities: [Twelve Data, InvestorStack]
tags: [stock-dashboard, twelve-data, api]
source_type: Facebook Post
source_title: ให้ AI สร้าง Stock Dashboard
source_author: InvestorStack
source_url: "https://www.facebook.com/InvestorStack/posts/pfbid02PPnHZhwmU4QCXf5CmtgVRYY8SL9ZWxghjLY9djTw5RMB8FGZcf8h9eoZZmbkpfaPl?__tn__=%2CO*F"
canonical_url: "https://www.facebook.com/InvestorStack/posts/pfbid02PPnHZhwmU4QCXf5CmtgVRYY8SL9ZWxghjLY9djTw5RMB8FGZcf8h9eoZZmbkpfaPl"
source_date: 2026-05-25
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Market Data API]]", "[[Dashboard]]"]
---

# AI Generated Stock Dashboard with Twelve Data

> [!summary] TL;DR
> Prompt ให้ AI สร้าง dashboard แบบ static HTML/CSS/JS ใช้ Twelve Data `/quote` และ `/time_series`, เก็บ watchlist/settings ใน localStorage, แสดง unavailable state แทนข้อมูลปลอม และ cache ประวัติเพื่อลด quota

## Verification & Caveat

เอกสาร Twelve Data ยืนยัน API key, quote/time-series และ batch symbols แต่แต่ละ symbol ยังใช้ API credit และ real-time/extended-hours/metrics บางชนิดขึ้นกับ plan จุดอ่อนสำคัญคือ API key ใน browser/local file ถูกผู้ใช้เห็นได้, CORS/plan limits เปลี่ยนได้ และคำว่า “real-time” ต้องตรวจ exchange entitlement กับ timestamp จริง

## Sources

- [Original Facebook post](https://www.facebook.com/InvestorStack/posts/pfbid02PPnHZhwmU4QCXf5CmtgVRYY8SL9ZWxghjLY9djTw5RMB8FGZcf8h9eoZZmbkpfaPl?__tn__=%2CO*F)
- [Twelve Data API documentation](https://twelvedata.com/docs)
- [Twelve Data batch requests](https://support.twelvedata.com/en/articles/5203360-batch-api-requests)

