---
title: Code as Agent Harness
note_type: source
primary_topic: Data_Science
secondary_topics: [Agentic AI, Software Engineering]
concepts: [Agent Harness, Verification, Multi-Agent Systems]
entities: [University of Illinois Urbana-Champaign, Meta, Stanford]
tags: [agent-harness, code-agents, multi-agent]
source_type: Facebook Post and Research Paper
source_title: Code as Agent Harness
source_author: Tdin Vi and paper authors
source_url: "https://www.facebook.com/tdin.moong/posts/pfbid02YVA58PZSZhzfm64W5Q3U4Dd8ugYBMvNNijyWHijF87bGXMygDRAo3JmQMCfFBgnCl?__tn__=%2CO*F"
source_urls: ["https://www.facebook.com/tdin.moong/posts/pfbid02YVA58PZSZhzfm64W5Q3U4Dd8ugYBMvNNijyWHijF87bGXMygDRAo3JmQMCfFBgnCl?__tn__=%2CO*F", "https://arxiv.org/pdf/2605.18747"]
canonical_url: "https://www.facebook.com/tdin.moong/posts/pfbid02YVA58PZSZhzfm64W5Q3U4Dd8ugYBMvNNijyWHijF87bGXMygDRAo3JmQMCfFBgnCl"
canonical_urls: ["https://www.facebook.com/tdin.moong/posts/pfbid02YVA58PZSZhzfm64W5Q3U4Dd8ugYBMvNNijyWHijF87bGXMygDRAo3JmQMCfFBgnCl", "https://arxiv.org/abs/2605.18747"]
source_date: 2026-06-10
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Agentic AI]]", "[[Software Verification]]"]
---

# Code as Agent Harness

> [!summary] TL;DR
> งาน survey เสนอให้มอง code เป็นโครงสร้างปฏิบัติการของ agent: ใช้คิด ลงมือทำ จำลองสภาพแวดล้อม เก็บ state และตรวจผลได้ในรูปแบบที่ executable และ inspectable

## Three-Layer Framework

1. **Harness interface** — code สำหรับ reasoning, acting และ environment modeling
2. **Harness mechanisms** — planning, memory, tool use, วงจร plan–execute–verify และ telemetry/optimization
3. **Scaling** — การแบ่งบทบาทของหลาย agent, shared code artifacts/state และการประสาน feedback

## Applications and Open Problems

ขอบเขตครอบคลุม coding assistants, GUI/OS automation, embodied agents, scientific discovery, personalization และ DevOps/enterprise ส่วนโจทย์เปิดคือ evaluation ที่กว้างกว่า task success, semantic verification เมื่อ feedback ไม่ครบ, regression-free evolution, shared-state conflicts/transactions, human oversight และ multimodal grounding

## Reconciliation

URL-117 เป็นโพสต์แนะนำและ URL-118 เป็น PDF ของงานเดียวกัน จึงรวมเป็นโน้ตเดียว การตรวจสอบใช้ abstract และ HTML ต้นฉบับของ arXiv เมื่อ PDF ไม่แสดงใน Browser ไม่ถือว่า paper ถูกบล็อก

## Sources

- [Facebook post](https://www.facebook.com/tdin.moong/posts/pfbid02YVA58PZSZhzfm64W5Q3U4Dd8ugYBMvNNijyWHijF87bGXMygDRAo3JmQMCfFBgnCl?__tn__=%2CO*F)
- [arXiv paper](https://arxiv.org/pdf/2605.18747)
- [Readable arXiv HTML](https://arxiv.org/html/2605.18747v1)




