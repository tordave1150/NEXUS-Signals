---
title: MiroFish Multi-Agent Social Simulation
note_type: source
primary_topic: Data_Science
secondary_topics: [Agentic AI, Simulation]
concepts: [Multi-Agent Simulation, Knowledge Graph, Persona]
entities: [MiroFish, OASIS]
tags: [multi-agent, social-simulation, knowledge-graph]
source_type: Facebook Post and GitHub Repository
source_title: MiroFish swarm intelligence prediction engine
source_author: Superbear
source_url: "https://www.facebook.com/superbear.dev/posts/pfbid0od6exrmqAMxZb9MLCmPGSwsi6ft8CkmGWzzR6vTsqYt57oXswqJQiMtdcE7ETQFgl?__cft__[0]=AZY3lFe-ouy5fCuHmlAsBDFDNqrprtnbpTnxgbRVPrgVuTQ3zbO65ohpEo9Xd-QRMrD3fCLR1i-TwfF0fGxt9SniGJ8ReF6Mdg_zVdpGTUD_MRKSuYnB4kd3NDBsOakcnCjUIJqBN1EZ_YVM9th0hTpIgOb-EfaHrQNoH2x6tObAXg&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/superbear.dev/posts/pfbid0od6exrmqAMxZb9MLCmPGSwsi6ft8CkmGWzzR6vTsqYt57oXswqJQiMtdcE7ETQFgl"
source_date: 2026-06-10
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Agent-Based Modeling]]", "[[Social Simulation]]"]
---

# MiroFish Multi-Agent Social Simulation

> [!summary] TL;DR
> MiroFish เป็น prediction engine ที่สร้างสภาพแวดล้อมและ persona จำนวนมากเพื่อจำลองปฏิสัมพันธ์ทางสังคม แล้วสังเคราะห์รายงานและเปิดให้ถามตอบกับผลจำลองได้

## Workflow

1. สร้าง graph จากข้อมูลต้นทาง
2. กำหนด environment, personas, goals, memory และ relationships
3. รัน social simulation บน OASIS
4. สร้างรายงานและโต้ตอบกับผลลัพธ์

## Verification & Risk

Repository ทางการยืนยัน workflow และ dependency หลัก (Node 18+, Python 3.11–3.12 และ LLM API) แต่ยังไม่ควรตีความผลเป็นการพยากรณ์ที่ calibrated: issue ของโครงการเองชี้ว่าไม่มีการรับรอง causal validity หรือ scientific calibration แบบ agent-based model คลาสสิก อีกทั้งมีรายงานเรื่องการขาด authentication เมื่อเปิดบริการออกสู่เครือข่าย จึงควรรัน local-only หลัง firewall และห้ามใช้ผลจำลองเป็นสัญญาณลงทุนโดยไม่มี backtest/validation ภายนอก

## Sources

- [Original Facebook post](https://www.facebook.com/superbear.dev/posts/pfbid0od6exrmqAMxZb9MLCmPGSwsi6ft8CkmGWzzR6vTsqYt57oXswqJQiMtdcE7ETQFgl?__cft__[0]=AZY3lFe-ouy5fCuHmlAsBDFDNqrprtnbpTnxgbRVPrgVuTQ3zbO65ohpEo9Xd-QRMrD3fCLR1i-TwfF0fGxt9SniGJ8ReF6Mdg_zVdpGTUD_MRKSuYnB4kd3NDBsOakcnCjUIJqBN1EZ_YVM9th0hTpIgOb-EfaHrQNoH2x6tObAXg&__tn__=%2CO%2CP-R)
- [Official repository](https://github.com/666ghj/MiroFish)




