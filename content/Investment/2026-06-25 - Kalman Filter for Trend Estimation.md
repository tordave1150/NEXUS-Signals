---
title: Kalman Filter for Trend Estimation
note_type: source
primary_topic: Investment
secondary_topics: [Signal Processing, Algorithmic Trading]
concepts: [Kalman Filter, State Space Model, Kalman Gain]
entities: [S&P 500 E-mini Futures]
tags: [kalman-filter, trend, signal-processing]
source_type: Facebook Post and Research Paper
source_title: Trend without hiccups — a Kalman filter approach
source_author: Investic Academy and paper authors
source_url: "https://www.facebook.com/investic.academy/posts/pfbid033JBTRQm1Yjq9xHmVxaUQ64meJuJf2vXtaYVtZLoafKmDSeEySVUWbtUZFZ844zm8l?__tn__=%2CO*F"
canonical_url: "https://www.facebook.com/investic.academy/posts/pfbid033JBTRQm1Yjq9xHmVxaUQ64meJuJf2vXtaYVtZLoafKmDSeEySVUWbtUZFZ844zm8l"
source_date: 2026-06-25
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Kalman Filter]]", "[[State Space Model]]"]
---

# Kalman Filter for Trend Estimation

## How It Works

Kalman filter ใช้วงจร predict → correct ใน state-space model แล้วใช้ Kalman gain ถ่วงน้ำหนักระหว่าง prior/model กับ observation ใหม่ตาม uncertainty ของทั้งสองฝั่ง จึงเป็นมากกว่า moving average คงที่

## Reported Evidence

Paper *Trend without hiccups: a Kalman filter approach* นำเสนอ 4 แบบสำหรับ S&P 500 mini-future และรายงานว่าแบบที่ผสม smoothing กับ extremum position ให้ net performance ดีกว่า moving-average benchmark โพสต์ยกผล test ประมาณ €4,266 เทียบ €935 และ Sharpe 1.40 เทียบ 0.41

## Caveat

ผลตัวเลขเฉพาะขึ้นกับ sample, contract roll, cost, model/noise covariance และ strategy rules Kalman filter ไม่ได้แยก “trend จริง” จาก noise อย่างปราศจากสมมติฐาน หาก tuning จาก test period หรือ regime เดียวก็ overfit ได้ ต้องทำ walk-forward, sensitivity analysis และ benchmark หลังต้นทุน

## Sources

- [Original Facebook post](https://www.facebook.com/investic.academy/posts/pfbid033JBTRQm1Yjq9xHmVxaUQ64meJuJf2vXtaYVtZLoafKmDSeEySVUWbtUZFZ844zm8l?__tn__=%2CO*F)
- [arXiv paper](https://arxiv.org/abs/1808.03297)


