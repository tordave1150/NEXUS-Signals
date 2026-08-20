---
title: GS Quant Agent Skills
note_type: source
primary_topic: Data_Science
secondary_topics: [Quantitative Finance, Agent Skills]
concepts: [Instruction Layer, Domain Workflow, Quant Library]
entities: [Goldman Sachs, gs-quant, Claude Code, GitHub Copilot]
tags: [gs-quant, agent-skills, quant-finance]
source_type: Facebook Post and GitHub Repository
source_title: Agent Skills in gs-quant
source_author: QuantCorner and Goldman Sachs
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid0NTwbK1m3DMQAyuZbHVaPoeJUykr8DNfvFHtL2Ma8CrJBV8RmGbNwPVJyhwRrnxywl?__cft__[0]=AZbfChamL-C_4iY5GbTF7tMZbHQkN76bYZziNJq-p6bKOAbZLDog95blx7SRN570gk6s3vxSzZZKgmOR64JLq-kaR8_S5y08Q_XzPWeD41xK4RZYhCkgdhzonaaP7YIACA2ZFyll5wM3rzrzs3jhAo5OLhJdPLtkjFqSv0aeaZewcQ&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid0NTwbK1m3DMQAyuZbHVaPoeJUykr8DNfvFHtL2Ma8CrJBV8RmGbNwPVJyhwRrnxywl"
source_date: 2026-06-18
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[GS Quant]]", "[[Agent Skill]]"]
---

# GS Quant Agent Skills

## Why This Matters

Repository เชิงเทคนิคเริ่มบรรจุ “instruction layer” ให้ AI agent เข้าใจ domain conventions, workflow และข้อควรระวัง นอกเหนือจาก code, docs, examples และ tests

## Verified Details

Repository `goldmansachs/gs-quant` มี `.claude/skills` และ package สำหรับ quantitative finance/derivatives/risk management โดย README ระบุ Python 3.9+ และ Apache-2.0 ส่วน API บางชุดต้องใช้ client id/secret สำหรับลูกค้าสถาบันของ Goldman Sachs จึงไม่ควรตีความว่า agent skills ทำให้บริการทั้งหมดเปิดใช้ฟรี

## Implications

Skills ช่วยชี้วิธีเรียก function, conventions ของ instruments, risk/backtest checks และ house style แต่ยังต้องพึ่ง tests, permissions, data entitlements และ human review โดยเฉพาะ calculation, PnL, model validation และ order-related actions

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid0NTwbK1m3DMQAyuZbHVaPoeJUykr8DNfvFHtL2Ma8CrJBV8RmGbNwPVJyhwRrnxywl?__cft__[0]=AZbfChamL-C_4iY5GbTF7tMZbHQkN76bYZziNJq-p6bKOAbZLDog95blx7SRN570gk6s3vxSzZZKgmOR64JLq-kaR8_S5y08Q_XzPWeD41xK4RZYhCkgdhzonaaP7YIACA2ZFyll5wM3rzrzs3jhAo5OLhJdPLtkjFqSv0aeaZewcQ&__tn__=%2CO%2CP-R)
- [Official gs-quant repository](https://github.com/goldmansachs/gs-quant)


