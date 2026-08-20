---
title: Self-Driving Portfolio ด้วย Agent ประมาณ 50 ตัว
note_type: source
primary_topic: Investment
secondary_topics: [Artificial Intelligence, Portfolio Management]
concepts: [Strategic Asset Allocation, Multi-Agent System, Investment Policy Statement]
entities: [Andrew Ang, Nazym Azimbayev, Andrey Kim]
tags: [self-driving-portfolio, asset-allocation, multi-agent]
source_type: Facebook Post
source_title: จะเกิดอะไรขึ้นถ้าใช้ AI บริหารกองทุน
source_author: QuantCorner
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-077__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-077__"
source_date: 2026-05-14
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Strategic Asset Allocation]]", "[[Multi-Agent Systems]]"]
---

# Self-Driving Portfolio ด้วย Agent ประมาณ 50 ตัว

> [!summary] TL;DR
> Paper เสนอ strategic asset-allocation pipeline ที่ให้ agents ประมาณ 50 ตัวสร้าง capital-market assumptions, แข่งขันกันสร้างพอร์ต, peer review/โหวต และทำ board memo โดยใช้ Investment Policy Statement เป็น constraint กลาง

## Architecture

- Macro และ asset-class agents ประเมิน regime/expected returns
- Portfolio agents ใช้วิธีกว่า 20 แบบ รวม researcher และ adversarial diversifier
- Review/CIO agents วิจารณ์ รวม และเลือก candidate portfolios
- Meta-agent เทียบ forecast กับ realized returns แล้วเสนอแก้ code/prompts พร้อมบันทึกการเปลี่ยนแปลง

## Reconciliation

แหล่งต้นทางยืนยันสถาปัตยกรรมและจำนวน agents แต่เป็น demonstration ของกระบวนการ ไม่ใช่ track record ของกองทุนหรือหลักฐานผลตอบแทนเหนือมนุษย์ การให้ meta-agent rewrite ระบบต้องมี change approval, versioning, rollback, independent validation และ hard constraints ที่แก้เองไม่ได้

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-077__)
- [Ang, Azimbayev & Kim — The Self-Driving Portfolio](https://arxiv.org/abs/2604.02279)


