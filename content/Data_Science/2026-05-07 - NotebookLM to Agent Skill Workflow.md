---
title: จาก NotebookLM สู่ Agent Skill เฉพาะทาง
note_type: source
primary_topic: Data_Science
secondary_topics: [Knowledge Management, Artificial Intelligence]
concepts: [Source Grounding, Agent Skills, Knowledge Engineering]
entities: [NotebookLM, Claude]
tags: [notebooklm, agent-skills, knowledge-engineering]
source_type: Facebook Post
source_title: NotebookLM ไม่ได้มีดีแค่สรุปเอกสาร
source_author: Thongchai Thampueak
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-061__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-061__"
source_date: 2026-05-07
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: summarized
confidence: Medium
related: ["[[Agent Skills]]", "[[Source Grounding]]"]
---

# จาก NotebookLM สู่ Agent Skill เฉพาะทาง

> [!summary] TL;DR
> ใช้ NotebookLM อ่านชุดแหล่งอ้างอิงที่คัดแล้ว จากนั้นให้ร่าง `SKILL.md` ซึ่งบรรจุ persona, workflow, rules, constraints และ best practices เพื่อนำไปใช้ซ้ำกับ agent

## Workflow

1. คัด PDF, บทความ และ transcript ที่เชื่อถือได้เข้า NotebookLM
2. ให้ระบบสร้าง skill จากแหล่งเหล่านั้นอย่างเคร่งครัด
3. ตรวจข้อเท็จจริงและแก้ instructions ก่อนวางใน skills folder หรือแนบให้โมเดล
4. ทดสอบด้วยตัวอย่างทั้งกรณีที่ควรและไม่ควร activate skill

## Caveat

`SKILL.md` ที่สร้างโดยโมเดลไม่ใช่หลักประกันว่าคำตอบถูกหรือ hallucination ต่ำลงเสมอ คุณภาพขึ้นกับ source coverage, synthesis, trigger description, harness/tools และการประเมินผล ควรเก็บ citation map จากกฎใน skill กลับไปยังเอกสารต้นทาง

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-061__)


