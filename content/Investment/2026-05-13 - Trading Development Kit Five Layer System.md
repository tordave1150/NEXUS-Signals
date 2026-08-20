---
title: Trading Development Kit - Five-Layer System
note_type: source
primary_topic: Investment
secondary_topics: [Data_Science, Software Engineering]
concepts: [Trading Rules, Playbooks, Hooks, Subagents, Plugins]
entities: [Claude, Trading Development Kit]
tags: [trading-system, agent-workflow, risk-rules]
source_type: PDF
source_title: The Trading Development Kit
source_author: Unknown
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-075__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-075__"
alternate_source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-074__"
source_date: 2026-05-13
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Trading System]]", "[[Agent Skills]]", "[[Risk Controls]]"]
---

# Trading Development Kit - Five-Layer System

> [!summary] TL;DR
> เอกสาร 18 หน้าเสนอให้เขียนระบบเทรดเป็น artifacts ห้าชั้น: rules/risk, playbooks, deterministic hooks, specialist subagents และ deployable plugins เพื่อเพิ่มความสม่ำเสมอและ auditability

## Five Layers

1. **Memory:** `CLAUDE.md`, `Risk.md`, `Risk.local.md` เก็บกฎ, limits และ session behavior
2. **Knowledge:** playbooks เช่น breakout, pullback, mean-reversion โหลดตามงาน
3. **Guardrails:** hooks เช่น PreMarket, PostTrade, EndOfDay สำหรับ context/log/state
4. **Delegation:** market researcher, risk manager และ journal analyzer แยก context
5. **Distribution:** package skills, agents, hooks และ commands เป็น plugin ที่ version ได้

## Reconciliation

เอกสารช่วยจัด SOP แต่ข้อความ “discretion loses, systems win” เป็นคำขวัญ ไม่ใช่หลักฐานผลตอบแทน ไฟล์ instruction ไม่บังคับ risk limits เอง เว้นแต่ harness และ execution layer ทำ enforcement แบบ deterministic ระบบต้องแยกคำแนะนำ LLM ออกจาก broker permissions, เก็บ immutable logs, test hooks และห้าม commands bypass risk gates

URL-074 เป็นโพสต์สรุปเอกสารเดียวกัน จึงรวมไว้ใน Source Note นี้แทนการสร้างโน้ตซ้ำ

## Sources

- [Original PDF](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-075__)
- [Facebook summary](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-074__)

