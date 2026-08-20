---
title: สกัด Causal Knowledge Graph จาก Research Papers
note_type: source
primary_topic: Data_Science
secondary_topics: [Knowledge Management, Research Methods]
concepts: [Knowledge Graph, Causal Relation Extraction, Reification]
entities: [Obsidian]
tags: [knowledge-graph, causal-extraction, obsidian]
source_type: Facebook Post
source_title: เบื้องหลังการสร้าง knowledge graph บน Obsidian
source_author: Thanachart Ritbumroong
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-048__"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xlURL-048__"
source_date: 2026-04-22
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: summarized
confidence: Medium
related: ["[[Knowledge Graph]]", "[[Causal Inference]]"]
---

# สกัด Causal Knowledge Graph จาก Research Papers

> [!summary] TL;DR
> ผู้เขียนให้ AI สกัด construct, claim, evidence, definition, finding, implication และผู้แต่งจาก papers แล้วเขียนเป็น Obsidian nodes/links เพื่อค้นความสัมพันธ์ข้ามงานวิจัย

## Proposed Schema

- Construct–relationship–construct: `q+`, `q−`, `intent+`, `function+`, `t+` พร้อม cause/effect/modifier/comparison roles
- Claim–evidence–author และ construct–definition–author เพื่อรักษา provenance
- Finding–implication–author เพื่อเชื่อมผลที่พบกับนัยที่ผู้เขียนระบุหรืออนุมาน
- ใช้ concept node แยกจาก relation node เพราะลิงก์ธรรมดาของ Obsidianเก็บรายละเอียดของ edge ได้น้อย

## Caveat

การพบข้อความเชิงเหตุใน paper ไม่ได้พิสูจน์ causality โดยอัตโนมัติ ระบบควรเก็บว่าเป็นคำกล่าวของใคร หลักฐานชนิดใด และ relation มาจากข้อความตรงหรือการอนุมานของโมเดล ชื่อ paper ที่เป็นที่มาของ schema ไม่ได้ระบุ จึงยังตรวจย้อนกลับไม่ได้

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-048__)


