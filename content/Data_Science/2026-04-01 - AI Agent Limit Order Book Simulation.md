---
title: AI Agent สำหรับจำลอง Limit Order Book
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Artificial Intelligence]
concepts: [Limit Order Book, Market Impact, Agent-Based Modeling]
entities: [QuantCorner, Jan Rosenzweig]
tags: [market-microstructure, ai-agents, order-book]
source_type: Facebook Post
source_title: ใช้ AI Agent ทำนายปริมาณการซื้อขาย Option
source_author: QuantCorner
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid02sMsuVTk6s7wfedQaYx4g4bxy3Tsg8yWeNkRFoagphgfKwLNQMEMEFvh5ULKeTKwGl?__cft__[0]=AZYQ4hX_ypXGOjJ0-6cWoyyK00n8PKB-bXg4AidmARt4_z_n9eLs2xq6D_arXP_UDrM6lnUkTIf6xsYeh-Q-1z09GjzAkv9KDYx17Ahz-Lxies_NCB36QIvCogurDrk5lkNcA6SQSB6Qa-a65NK6RHXOTAxENisD7sVxItx6fxxgHg&__tn__=%2CO%2CP-R"
alternate_source_urls: ["https://www.facebook.com/quantcornerthailand/posts/pfbid0oLHC1eYYC4hWeUEyt3jkRKugaGaiTGMvdtYnyV8meUMRQKqRRhXhCCjM9aT6tBeal?__cft__[0]=AZasYkKEvkau72uX8e98ulTbF5p-m6LowyZ7VfBoH4QdR-qxF551PWBnF9zJguYXG9LLZm-L7vqFD45MHEX3kUFFy2Njmo0QWjPJA2kg2BeGwUvUyfR1vC8PxN_REsBouJO3Op1G6vV9yEJu2QGdc6a_P22L82Xf-DmmUHWI_sjqIQ&__tn__=%2CO%2CP-R"]
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid02sMsuVTk6s7wfedQaYx4g4bxy3Tsg8yWeNkRFoagphgfKwLNQMEMEFvh5ULKeTKwGl"
source_date: 2026-04-01
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: Medium
related: ["[[Limit Order Book]]", "[[Market Impact]]"]
---

# AI Agent สำหรับจำลอง Limit Order Book

> [!summary] TL;DR
> Agent-based LOB simulation ใช้ผู้เล่นที่รับ state เลือก action และเรียนรู้ภายใต้ inventory/execution constraints เพื่อศึกษาพฤติกรรมเชิงกลยุทธ์ที่ historical replay หรือ Monte Carlo แบบคงที่อธิบายได้ไม่ครบ

## Key Takeaways

- LOB depth, queue priority และ order flow กำหนด liquidity และ market impact
- Liquidity provider แลก spread capture กับ adverse-selection/inventory risk
- Historical replay สมจริงแต่สำรวจ counterfactual จำกัด; Monte Carlo ยืดหยุ่นแต่พึ่ง assumptions
- Agent-based model ต้องจำลอง feedback จากคำสั่งของตัวเองต่อตลาด

## Verification & Reconciliation

คำกล่าวว่า agents “พัฒนาเป็น liquidity providers โดยธรรมชาติ” ขึ้นกับ reward, simulator, latency, fees และ constraints ไม่ใช่กฎสากล และความ robust across options/futures ยังต้องมี paper/results รองรับ ชื่อโพสต์ใช้คำว่า “ทำนายปริมาณซื้อขาย” แต่เนื้อหาหลักเป็นการจำลองพฤติกรรมและ execution มากกว่าการรายงาน predictive accuracy

โพสต์ session เรื่อง self-similarity ใน option orderbooks เดิมมีเพียงคำโปรยเกี่ยวกับ statistical ensembles, conservation laws และ scaling ไม่มี paper/slides/นิยามให้ตรวจ จึงรวมไว้เป็น research lead ที่นี่ ไม่แยกเป็นข้อสรุปทางวิชาการ

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid02sMsuVTk6s7wfedQaYx4g4bxy3Tsg8yWeNkRFoagphgfKwLNQMEMEFvh5ULKeTKwGl?__cft__[0]=AZYQ4hX_ypXGOjJ0-6cWoyyK00n8PKB-bXg4AidmARt4_z_n9eLs2xq6D_arXP_UDrM6lnUkTIf6xsYeh-Q-1z09GjzAkv9KDYx17Ahz-Lxies_NCB36QIvCogurDrk5lkNcA6SQSB6Qa-a65NK6RHXOTAxENisD7sVxItx6fxxgHg&__tn__=%2CO%2CP-R)
- [Identical repost](https://www.facebook.com/quantcornerthailand/posts/pfbid0oLHC1eYYC4hWeUEyt3jkRKugaGaiTGMvdtYnyV8meUMRQKqRRhXhCCjM9aT6tBeal?__cft__[0]=AZasYkKEvkau72uX8e98ulTbF5p-m6LowyZ7VfBoH4QdR-qxF551PWBnF9zJguYXG9LLZm-L7vqFD45MHEX3kUFFy2Njmo0QWjPJA2kg2BeGwUvUyfR1vC8PxN_REsBouJO3Op1G6vV9yEJu2QGdc6a_P22L82Xf-DmmUHWI_sjqIQ&__tn__=%2CO%2CP-R)
- [Merged research lead — AI agents and self-similarity in option orderbooks](https://www.facebook.com/CQFInstitute/posts/pfbid08X2E1PAB6sFj4ttuXwDa1p8nJBJApqLH7k3Rp8JVJquih3ZdCpiCVBiPbnnpAnbbl)
