---
title: ห้า Repository สำหรับ Agent Development
note_type: source
primary_topic: Data_Science
secondary_topics: [Software Engineering, Artificial Intelligence]
concepts: [Agent Skills, Multi-Model Gateway, Agent Orchestration, TDD]
entities: [GitHub, Cloudflare Workers, Claude Code]
tags: [github, agent-development, repositories]
source_type: Facebook Post
source_title: 5 repos ที่น่าจับตาสัปดาห์นี้
source_author: Agent Dev Thai
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-063__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-063__"
source_date: 2026-05-10
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Agent Orchestration]]", "[[Agent Skills]]"]
---

# ห้า Repository สำหรับ Agent Development

> [!summary] TL;DR
> รายการคัด repos ครอบคลุม HTML slide generation, multi-model API bridge, protocol-enforced orchestration, ตัวอย่าง trading bot และ skill orchestration แบบ TDD

## Repository Map

- `guizang-ppt-skill`: สร้าง single-file HTML decks พร้อม layouts/themes และ presenter workflow
- `HelloGML`: API bridge สำหรับ Claude/OpenAI/Gemini บน Cloudflare Workers
- `harmonist`: บังคับ message contracts ระหว่าง agents เชิงกลไก
- `coinbase-trading-bot`: ตัวอย่าง EMA crossover + ATR filter และ paper trading
- `evanflow`: จัด skills เป็น pipeline ที่มี checkpoints และ feedback loop

## Caveat

จำนวน stars เปลี่ยนตลอดและไม่ใช่ตัววัดคุณภาพหรือความปลอดภัย ก่อนใช้ต้องตรวจ license, commit activity, dependencies, secret handling, test coverage และขอบเขต permission โดยเฉพาะ repo ที่แตะตลาดหรือ credentials

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-063__)
- [guizang-ppt-skill](https://github.com/op7418/guizang-ppt-skill)
- [HelloGML](https://github.com/Hello-Application-XH/HelloGML)
- [harmonist](https://github.com/GammaLabTechnologies/harmonist)
- [coinbase-trading-bot](https://github.com/AI4FinanceFoundation/coinbase-trading-bot)
- [evanflow](https://github.com/evanklem/evanflow)


