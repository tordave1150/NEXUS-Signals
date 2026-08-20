---
title: LLM Cost Optimization with Caching and Batch
note_type: source
primary_topic: Data_Science
secondary_topics: [AI Engineering, Cost Optimization]
concepts: [Prompt Caching, Batch API, Reasoning Budget]
entities: [OpenAI, Anthropic, Google]
tags: [llm-cost, prompt-caching, batch-api]
source_type: Facebook Post
source_title: ทำตามนี้ลด Token ได้ทันที
source_author: AI Daily
source_url: "https://www.facebook.com/AIDailyTH/posts/pfbid02gKgvvf8Lbj42ASGrAy8vaku7Py56gJ5st4VSzMWi5KKJJNSZi6LboAnH79Sx13Rcl?__tn__=%2CO*F"
canonical_url: "https://www.facebook.com/AIDailyTH/posts/pfbid02gKgvvf8Lbj42ASGrAy8vaku7Py56gJ5st4VSzMWi5KKJJNSZi6LboAnH79Sx13Rcl"
source_date: 2026-05-16
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Prompt Caching]]", "[[Batch Processing]]"]
---

# LLM Cost Optimization with Caching and Batch

> [!summary] TL;DR
> ลดต้นทุน LLM ได้ด้วยการวาง static prefix ให้คงที่เพื่อให้ cache hit, ส่งงานที่ไม่ต้องตอบทันทีผ่าน Batch API และจำกัดระดับ reasoning ให้เหมาะกับงาน แต่รายละเอียดราคา ขีดจำกัด และพารามิเตอร์ต้องตรวจเอกสารของโมเดลที่ใช้ทุกครั้ง

## Findings

- Prompt caching เหมาะกับ system prompt, tool definitions และ knowledge context ที่ซ้ำกัน โดยวางส่วนเปลี่ยนแปลงไว้ท้าย prompt
- Batch API เหมาะกับ eval, classification และ summarization ที่ยอมรอได้
- Reasoning budget/effort ช่วยควบคุม latency และ token ที่ใช้กับงานง่าย
- ควรบันทึก cached-token metrics จริง แทนการสรุปจากโครงสร้าง prompt เพียงอย่างเดียว

## Critical Reconciliation

เอกสารทางการยืนยันว่า OpenAI Batch ลดราคา 50% และ Anthropic มี cache write 1.25x/2x, cache read 0.1x พร้อม Batch ลด 50% ส่วน Gemini 2.5+ เปิด implicit caching โดยอัตโนมัติ อย่างไรก็ดี ตัวเลขอย่าง threshold, rate limit, model compatibility และการ stack ส่วนลดเปลี่ยนได้ จึงไม่ควรฝังเป็นกฎถาวรจากโพสต์นี้

## Sources

- [Original Facebook post](https://www.facebook.com/AIDailyTH/posts/pfbid02gKgvvf8Lbj42ASGrAy8vaku7Py56gJ5st4VSzMWi5KKJJNSZi6LboAnH79Sx13Rcl?__tn__=%2CO*F)
- [OpenAI Batch API](https://platform.openai.com/docs/api-reference/batch)
- [Anthropic pricing and prompt caching](https://docs.anthropic.com/en/docs/about-claude/pricing)
- [Gemini context caching](https://ai.google.dev/gemini-api/docs/caching)

