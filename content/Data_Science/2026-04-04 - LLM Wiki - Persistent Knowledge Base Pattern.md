---
title: LLM Wiki - Persistent Knowledge Base Pattern
note_type: source
primary_topic: Data_Science
secondary_topics: [Knowledge Management, Artificial Intelligence]
concepts: [LLM Wiki, RAG, Knowledge Compilation, Progressive Synthesis]
entities: [Andrej Karpathy, Obsidian]
tags: [llm-wiki, rag, knowledge-base]
source_type: GitHub Gist
source_title: LLM Wiki
source_author: Andrej Karpathy
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-043__"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xlURL-043__"
source_date: 2026-04-04
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: High
related: ["[[RAG]]", "[[Knowledge Graph]]", "[[Obsidian]]"]
---

# LLM Wiki - Persistent Knowledge Base Pattern

> [!summary] TL;DR
> Karpathy เสนอให้ LLM ดูแล wiki แบบ Markdown ที่สะสมผลสรุป ลิงก์ ความขัดแย้ง และ synthesis ไว้ถาวร แทนการค้น raw documents และประกอบคำตอบใหม่ทุกครั้งแบบ RAG อย่างเดียว

## Architecture

1. **Raw sources** เป็นหลักฐานต้นทางและไม่แก้ไข
2. **Wiki** เป็นชั้นความรู้ที่ LLM สรุป เชื่อมโยง และปรับปรุง
3. **Schema** เช่น `AGENTS.md` กำหนดโครงสร้างและ workflow ให้ agent ทำงานสม่ำเสมอ

Operations หลักคือ ingest, query และ lint พร้อม `index.md` สำหรับนำทางเชิงเนื้อหาและ `log.md` สำหรับประวัติการเปลี่ยนแปลง แนวทางนี้ยังแนะนำ Git, Obsidian, Dataview และ local search เป็นส่วนเสริมตามขนาดงาน

## Reconciliation

เอกสารต้นทางระบุเองว่าเป็น pattern เชิงแนวคิด ไม่ใช่ implementation หรือหลักฐานว่า wiki เหนือกว่า RAG ทุกกรณี ระบบจริงยังต้องจัดการ provenance, review, access control, stale claims และ retrieval เมื่อคลังโตขึ้น

## RAG and Wiki Are Complementary

RAG ดึงหลักฐานที่เกี่ยวข้อง ณ เวลา query จึงเหมาะกับ corpus ใหญ่หรือข้อมูลที่เปลี่ยนเร็ว ส่วน persistent wiki เก็บ synthesis, การตัดสินใจ และความขัดแย้งที่ผ่านการทบทวนแล้ว จึงลดการย่อยซ้ำ การทดลอง Big Debt Cycle ใน Obsidian เป็นตัวอย่างการใช้ Markdown/links/graph view เพื่อสำรวจความสัมพันธ์ แต่เป็นประสบการณ์ใช้งาน ไม่ใช่ benchmark ว่า graph view เพิ่มความถูกต้อง

## 🔎 In-depth Details

สถาปัตยกรรมที่แข็งแรงควรแยกสามชั้นชัดเจน: **source layer** ที่ immutable, **evidence index** สำหรับ retrieval และ **canonical notes** ที่มนุษย์ตรวจได้ ทุก claim ใน canonical note ควรชี้กลับไปยัง source/date และมีสถานะ freshness; เมื่อแหล่งใหม่ขัดแย้ง ให้เก็บทั้งสองมุมมองพร้อมเหตุผล reconciliation แทน overwrite แบบเงียบ

ตัวชี้วัดควรแยก retrieval recall, citation entailment, synthesis accuracy, staleness และ maintenance cost เพราะระบบอาจค้นเก่งแต่สรุปผิด หรือ wiki อ่านดีแต่ล้าสมัย การ “compile knowledge” จึงไม่ใช่ทางแทน RAG แต่เป็นชั้นควบคุมคุณภาพและความจำระยะยาวเหนือ retrieval

## Sources

- [Original post / Gist pointer](https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-043__)
- [Merged post — RAG and persistent wiki](https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xlURL-055__)
- [Merged post — Big Debt Cycle Obsidian experiment](https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xlURL-042__)
- [Lewis et al. — Retrieval-Augmented Generation](https://arxiv.org/abs/2005.11401)


