---
title: SKILL.md ต้องทำงานร่วมกับ Agent Harness
note_type: source
primary_topic: Data_Science
secondary_topics: [Software Engineering, Artificial Intelligence]
concepts: [Agent Skills, Tool Harness, Runtime, Progressive Disclosure]
entities: [Claude Code, Codex, Agent Skills]
tags: [skill-md, agent-harness, tools]
source_type: Facebook Post
source_title: กระแส SKILL.md กลับมาอีกครั้ง
source_author: Data Karate
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-060__"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xlURL-060__"
source_date: 2026-05-07
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Agent Skills]]", "[[Tool Use]]"]
---

# SKILL.md ต้องทำงานร่วมกับ Agent Harness

> [!summary] TL;DR
> `SKILL.md` บรรจุ metadata และคำแนะนำ แต่ความสามารถจริงเกิดเมื่อ agent harness มีเครื่องมือ สิทธิ์ และ runtime ที่เรียก script หรือจัดการไฟล์ได้ คู่มืออย่างเดียวไม่สามารถสร้าง artifact หรือ deploy ระบบแทนเครื่องมือได้

## Verification & Reconciliation

มาตรฐาน Agent Skills ยืนยันว่า skill เป็นโฟลเดอร์ที่มี `SKILL.md` และอาจมี `scripts/`, `references/`, `assets/` โดยโหลดแบบ progressive disclosure อย่างไรก็ตามการเปรียบว่า skill เป็นเพียง prompt “แปะในแชต” ไม่ครบถ้วน: skill ยังให้ trigger metadata, โครงสร้างไฟล์, reusable resources และ workflow ที่ version control ได้ ส่วน harness เป็นผู้จัด discovery, tool access, sandbox/permissions และ execution

ดังนั้นผลสำเร็จขึ้นกับทั้ง instruction quality, model capability, tools/runtime, permissions, environment และการตรวจผล ไม่ใช่ skill หรือ harness อย่างใดอย่างหนึ่ง

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-060__)
- [Agent Skills Specification](https://agentskills.io/specification)
- [Agent Skills — Adding Skills Support](https://agentskills.io/client-implementation/adding-skills-support)

