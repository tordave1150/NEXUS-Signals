---
title: Meta Portfolio Method
note_type: source
primary_topic: Investment
secondary_topics: [Machine Learning, Portfolio Construction]
concepts: [Adaptive Strategy Selection, Hierarchical Risk Parity, Naive Risk Parity]
entities: [Damian Kisiel, Denise Gorse, XGBoost]
tags: [portfolio, regime-switching, xgboost]
source_type: Facebook Post and Research Paper
source_title: A Meta-Method for Portfolio Management Using Machine Learning for Adaptive Strategy Selection
source_author: WealthGuru, Damian Kisiel and Denise Gorse
source_url: "https://www.facebook.com/wealthguruconsulting/posts/pfbid02DmVvffjseQN4hjqLSwb9oq61hMUmYYd5NMiiKnWJZmPpcmtveaxECakxuKKMWmHcl?__cft__[0]=AZaHmCVDIG0n0iq7AoXLx34vTN_7rV_JzxrbwecNIkieUCIiWHMatyyVWzDGQc4EJ6JD1wvuWJKZc4ERjg3d0scsll-uoH1TNOceceW_PSvGCBkRomCyqwPH3EAJdyaO2KWwR78DzZdk4hksTcDeZ8d9QiJky3GjPHB9hhT7nBL-EA&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/wealthguruconsulting/posts/pfbid02DmVvffjseQN4hjqLSwb9oq61hMUmYYd5NMiiKnWJZmPpcmtveaxECakxuKKMWmHcl"
source_date: 2026-06-27
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Hierarchical Risk Parity]]", "[[Adaptive Portfolio]]"]
---

# Meta Portfolio Method

## Core Method

Meta Portfolio Method (MPM) ใช้ XGBoost เลือกสลับระหว่าง Hierarchical Risk Parity (HRP) ซึ่งเน้นลด drawdown กับ Naive Risk Parity (NRP) ซึ่งเติบโตเร็วกว่าใน uptrend โดย features มาจาก performance ล่าสุดของ component strategies

## Verified Findings

Paper ปี 2021 ของ Damian Kisiel และ Denise Gorse รายงาน out-of-sample risk-reward/Sharpe ที่ดีและตีความ allocation decisions ได้ใน 10 investment universes แนวคิดสำคัญคือเปลี่ยนจาก “พอร์ตใดดีที่สุดตลอดเวลา” เป็น “ช่วงถัดไปควรใช้ allocation rule ใด”

## Caveat

MPM ไม่รู้ regime โดยตรง แต่เรียน mapping จากอดีต การสลับ model เพิ่ม meta-overfitting, hyperparameter, turnover และ timing risk ต้องทำ nested walk-forward, include costs/taxes, test transition periods และเปรียบเทียบกับ static blend หรือ simple regime rules ก่อนสรุปว่า ML เพิ่มคุณค่า

## Sources

- [Original Facebook post](https://www.facebook.com/wealthguruconsulting/posts/pfbid02DmVvffjseQN4hjqLSwb9oq61hMUmYYd5NMiiKnWJZmPpcmtveaxECakxuKKMWmHcl?__cft__[0]=AZaHmCVDIG0n0iq7AoXLx34vTN_7rV_JzxrbwecNIkieUCIiWHMatyyVWzDGQc4EJ6JD1wvuWJKZc4ERjg3d0scsll-uoH1TNOceceW_PSvGCBkRomCyqwPH3EAJdyaO2KWwR78DzZdk4hksTcDeZ8d9QiJky3GjPHB9hhT7nBL-EA&__tn__=%2CO%2CP-R)
- [arXiv paper](https://arxiv.org/abs/2111.05935)


