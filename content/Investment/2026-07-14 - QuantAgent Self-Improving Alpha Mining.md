---
title: QuantAgent Self-Improving Alpha Mining
note_type: source
primary_topic: Investment
secondary_topics: [Agentic AI, Quantitative Research]
concepts: [Alpha Mining, Inner Loop, Outer Loop]
entities: [QuantAgent, XGBoost]
tags: [quantagent, alpha, self-improvement]
source_type: Facebook Post and Research Paper
source_title: QuantAgent Seeking Holy Grail in Trading
source_author: Investic Academy and Wang et al.
source_url: "https://www.facebook.com/investic.academy/posts/pfbid02eWQoLXChVQVrUch9GkNEvBsxMsFTBNqRdGZGzNL4fbmKKfiQNZbnKCSNK4cuKTg6l?__cft__[0]=AZZDJwdJuCKzgKXgsQRVTPjan3tiho2TcCRPRS-dbtOSXtWgak2eX2o2SNi_pICnAUHuueMPlFZaTckizTEzKZIrGO2Rag-xL9Z7B9T_Y3uk17bKjV1nZD_xoAeyqwS9PQ0aRG4FZSrdWFEcvxA85wUl6EZoX3aGRTgx_DPwVcBswA&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/investic.academy/posts/pfbid02eWQoLXChVQVrUch9GkNEvBsxMsFTBNqRdGZGzNL4fbmKKfiQNZbnKCSNK4cuKTg6l"
source_date: 2026-07-14
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: verified
confidence: High
related: ["[[Alpha Research]]", "[[Self Improving Agent]]"]
---

# QuantAgent Self-Improving Alpha Mining

## Architecture

QuantAgent แปลง trading idea เป็น factor code ผ่าน inner loop ระหว่าง writer กับ judge แล้วใช้ outer loop รัน code/backtest และบันทึก feedback กลับ knowledge base งานทดลองนำ factors ไปเป็น features ของ XGBoost และรายงานว่า predictive MSE ลดลงเมื่อสะสม signals เพิ่ม

## Evidence Boundary

paper ยอมรับว่า individual-alpha metrics เช่น IC, return และ Sharpe ไม่ได้ดีขึ้นชัดเจนทุก iteration ผลยังเป็นการทดลองจำกัด ไม่ใช่หลักฐาน live profitability อีกทั้ง LLM judge อาจอนุมัติ code ผิด จึงต้องมี unit tests, static validation, leakage controls, transaction costs, multi-regime OOS และ multiple-testing correction

## Sources

- [Original Facebook post](https://www.facebook.com/investic.academy/posts/pfbid02eWQoLXChVQVrUch9GkNEvBsxMsFTBNqRdGZGzNL4fbmKKfiQNZbnKCSNK4cuKTg6l?__cft__[0]=AZZDJwdJuCKzgKXgsQRVTPjan3tiho2TcCRPRS-dbtOSXtWgak2eX2o2SNi_pICnAUHuueMPlFZaTckizTEzKZIrGO2Rag-xL9Z7B9T_Y3uk17bKjV1nZD_xoAeyqwS9PQ0aRG4FZSrdWFEcvxA85wUl6EZoX3aGRTgx_DPwVcBswA&__tn__=%2CO%2CP-R)
- [QuantAgent paper](https://arxiv.org/abs/2402.03755)


