---
title: Agentic AI สามระดับ - Chat, Workflows และ Systems
note_type: source
primary_topic: Data_Science
secondary_topics: [Artificial Intelligence, Automation]
concepts: [AI Workflows, Skills, Agent Teams]
entities: [Komes Chandavimol]
tags: [agentic-ai, workflows, automation]
source_type: Facebook Post
source_title: Welcome to the world of Agentic-AI
source_author: Seminar knowledge by Amorn
source_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid02oMv9HTxzgp5YFPXg3But8qKS4And3qXUXgtPY3jzUVSCkytqtNmwRywCNm5BFecal&id=100049294731654&__cft__[0]=AZaQoaMH4M0-iaNAUSd6MFnzix8bqw6__c6_Mfdc3bnKaMb_wQxbW2QGzL79KubM4VChVtxiyjJSjmjYuhx_bDnGGgBEK5UW3vt-A0GXeH2xWvrEdErmGQeB_Que6z2jwzV7m9BQqTpC8-rQjZlHnIGKchD-vN8XUm2f5xScA7DFIQ&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid02oMv9HTxzgp5YFPXg3But8qKS4And3qXUXgtPY3jzUVSCkytqtNmwRywCNm5BFecal&id=100049294731654"
source_date: 2026-03-31
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: Medium
related: ["[[AI Workflows]]", "[[Agent Teams]]"]
---

# Agentic AI สามระดับ

> [!summary] TL;DR
> การใช้ AI พัฒนาจาก Chat ที่มนุษย์ลงมือ → Workflows ที่มีข้อมูล/skills/ขั้นตอน → Systems ที่เชื่อมเครื่องมือและแบ่งงานเป็น agent teams; ยิ่งอัตโนมัติมากยิ่งต้องเพิ่ม controls และ observability

## Key Takeaways

- Chat เหมาะ drafting/summarization แต่เสี่ยง hallucination
- Workflow ต้องนิยามขั้นตอน ข้อมูล และ output contract ลด process drift
- Skills ใช้ progressive loading ของ instructions/resources ตามงาน
- Agent teams ช่วย parallelize แต่เพิ่ม coordination cost และ failure modes

## Verification & Reconciliation

ตัวเลข “98% token savings” และทีมเหมาะสม 3–5 agents เป็นคำกล่าวจาก session ไม่ได้มี benchmark ที่ตรวจสอบได้ในโพสต์ ส่วนการสแกนประวัติแชทเพื่อสร้าง skill ต้องพิจารณาความเป็นส่วนตัวและสิทธิ์การเข้าถึง ไม่ควรถือว่าเป็นพฤติกรรมมาตรฐานของทุกผลิตภัณฑ์

## Sources

- [Original Facebook post](https://www.facebook.com/permalink.php?story_fbid=pfbid02oMv9HTxzgp5YFPXg3But8qKS4And3qXUXgtPY3jzUVSCkytqtNmwRywCNm5BFecal&id=100049294731654&__cft__[0]=AZaQoaMH4M0-iaNAUSd6MFnzix8bqw6__c6_Mfdc3bnKaMb_wQxbW2QGzL79KubM4VChVtxiyjJSjmjYuhx_bDnGGgBEK5UW3vt-A0GXeH2xWvrEdErmGQeB_Que6z2jwzV7m9BQqTpC8-rQjZlHnIGKchD-vN8XUm2f5xScA7DFIQ&__tn__=%2CO%2CP-R)
