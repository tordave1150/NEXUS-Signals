---
title: QuantAgent - Multi-Agent Trading Analysis
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Artificial Intelligence]
concepts: [Multi-Agent System, Technical Analysis, Trading Plan]
entities: [QuantAgent, LangChain, LangGraph]
tags: [quantagent, multi-agent, trading]
source_type: Facebook Post
source_title: AI Agent สำหรับสายเทรด QuantAgent
source_author: DeepRepo.ai
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-062__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-062__"
source_date: 2026-05-09
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Multi-Agent Systems]]", "[[Algorithmic Trading]]"]
---

# QuantAgent - Multi-Agent Trading Analysis

> [!summary] TL;DR
> QuantAgent แบ่งการวิเคราะห์ราคาเป็น agents เฉพาะด้าน แล้วรวม technical indicators, pattern recognition และ trend analysis เพื่อสร้างคำอธิบายและแผนเทรด

## Verification & Reconciliation

Repository ทางการยืนยันทีมจากห้ามหาวิทยาลัยและการใช้ LangChain/LangGraph แต่ข้อความว่า agent หลายตัว “แม่นยำกว่า AI ตัวเดียว” ยังไม่ใช่ข้อสรุปที่พิสูจน์จาก README การเพิ่ม agent อาจเพิ่ม diversity แต่ก็เพิ่ม correlation of errors, latency, cost และความเสี่ยงจาก judge/aggregation

ระบบใช้ข้อมูลจาก Yahoo Finance และต้องใช้ LLM API/TA-Lib บางส่วน จึงควรทดสอบ timestamp alignment, costs, slippage และ out-of-sample performance ก่อนใช้จริง

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-062__)
- [Official QuantAgent repository](https://github.com/y-research-sbu/QuantAgent)


