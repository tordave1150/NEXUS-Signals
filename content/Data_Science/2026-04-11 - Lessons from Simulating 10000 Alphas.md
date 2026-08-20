---
title: บทเรียนจากการจำลอง 10,000 Alphas
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Statistics]
concepts: [Alpha Research, Feature Selection, Overfitting, Normalization]
entities: [QuantCorner, WorldQuant BRAIN]
tags: [quant-research, alpha, feature-engineering]
source_type: Facebook Post
source_title: บทเรียนจากการ sim 10,000 Alpha จาก Brain
source_author: QuantCorner
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-041__"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xlURL-041__"
source_date: 2026-04-11
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: Medium-High
related: ["[[Alpha Research]]", "[[Overfitting]]"]
---

# บทเรียนจากการจำลอง 10,000 Alphas

> [!summary] TL;DR
> ผู้เขียนรายงานจากการทดลองส่วนตัวว่า alpha ที่ผ่านเกณฑ์มักใช้ field น้อย สูตรสั้น มี pairing ที่อธิบายเชิงเศรษฐศาสตร์ได้ และใช้ normalization/neutralization เพื่อควบคุม noise

## Key Takeaways

- ค่าเฉลี่ยที่ผู้เขียนรายงานคือประมาณ 2.2 fields และ expression ยาวราว 76 ตัวอักษรสำหรับกลุ่มผ่าน เทียบกับราว 108 ตัวอักษรในกลุ่มไม่ผ่าน
- ตัวอย่าง pairing ได้แก่ fundamental กับ price/volume, estimate revision กับ momentum และ earnings signal กับ trend confirmation
- `rank`, `zscore`, `ts_delta`, `ts_corr` และ `group_neutralize` ถูกใช้เพื่อทำสเกล จับการเปลี่ยนแปลง และลด sector bias
- หลักคิดที่นำกลับมาใช้ได้คือเริ่มจากสมมติฐานที่อธิบายได้ แล้วคุมความซับซ้อนก่อนเพิ่มตัวแปร

## Caveat

ตัวเลขเป็นผลจากชุดทดลองของผู้เขียน ไม่ใช่ benchmark ที่ทำซ้ำได้จากโพสต์ เพราะไม่มี universe, sample period, fitness constraints และไฟล์ผลลัพธ์ จึงควรถือเป็น heuristic ไม่ใช่กฎสากล

## 🔎 In-depth Details

การจำลอง 10,000 สูตรทำให้ “จำนวนการทดลอง” เป็นส่วนหนึ่งของผลลัพธ์: alpha ที่ดีที่สุดอาจดูดีเพราะ selection bias แม้ทุกสูตรจะไม่มี edge จริง Experiment log จึงต้องเก็บ hypothesis, data fields, operators, parameter variants, rejected trials และเหตุผลการเปลี่ยนสูตร เพื่อให้ประเมิน search budget และ correlation ระหว่าง trials ได้

ใช้ BRAIN เป็น research environment ไม่ใช่เครื่องรับรอง robustness: แยก discovery/validation/untouched holdout, cluster alphas ตาม return correlation, ตรวจ turnover/capacity และใช้ metric ที่ปรับ multiple testing เช่น deflated Sharpe หรือ Probability of Backtest Overfitting เมื่อเป็นไปได้ “สูตรสั้น” มีคุณค่าเพราะตรวจเหตุผลและลด search space ได้ แต่ไม่ใช่หลักฐานว่า signal จริง

> [!important] Stop rule
> กำหนดจำนวน trials และเกณฑ์ยอมรับก่อนเริ่มค้น; หากเปลี่ยนเกณฑ์หลังเห็นผล ให้เปิด experiment ใหม่แทนการนับเป็นการทดสอบเดิม

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid06zftkfDbth9ktqYcM2iLzPkq22R12CgeMonj2LHpqxVNV3NW5js1wi12ZwvKMA7xl?__cft__[0]=AZY0KMlG5aL_1FovSK02d4tqDb-CeVf0-M25GVgCSVolu-7Lew8bEJD42VPuyKSQAR9rTw_WPocLYYPQwqVqq3h3MwvSaPJC8s9z01kjL4f2GFycu1KEhq3Kl5DkPpAOogYlSTUyiXmsdLEN6cJa6NVcxoqfQTzGaJeggFtwvVgpLQ&__tn__=%2CO%2CP-RURL-041__)
- [Merged post — WorldQuant simulation heuristics](https://www.facebook.com/permalink.php?story_fbid=pfbid02SotRfe7e1cfXuoXRMHgJfhhPqBnfZix8j2BTXwGiRXQAkegqeuLfqiHDmf1TFA4pl&id=61583197281536)
- [WorldQuant BRAIN official overview](https://www.worldquant.com/brain/)
- [Bailey et al. — The Probability of Backtest Overfitting](https://doi.org/10.21314/JCF.2016.322)


