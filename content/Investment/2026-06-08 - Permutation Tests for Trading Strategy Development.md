---
title: Permutation Tests for Trading Strategy Development
note_type: source
primary_topic: Investment
secondary_topics: [Statistics, Backtesting]
concepts: [Permutation Test, Walk-Forward Test, Data Snooping]
entities: [Timothy Masters, GroundUp Academy]
tags: [permutation-test, walk-forward, strategy-validation]
source_type: Facebook Post and Video Reference
source_title: Monte Carlo permutation tests for trading strategies
source_author: GroundUp Academy
source_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid02cagvjC7FmZjkP1dDF6wPZy3JPwaAMfGFhjpA593QyNZXvrtqRV1SCTDGajfipHjdl&id=61569334229421&__tn__=%2CO*F"
canonical_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid02cagvjC7FmZjkP1dDF6wPZy3JPwaAMfGFhjpA593QyNZXvrtqRV1SCTDGajfipHjdl&id=61569334229421"
source_date: 2026-06-08
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: summarized
confidence: Medium
related: ["[[Backtesting]]", "[[Monte Carlo Method]]"]
---

# Permutation Tests for Trading Strategy Development

> [!summary] TL;DR
> Workflow เสนอให้ใช้ permutation tests ควบคู่กับ walk-forward testing เพื่อถามว่าผลงานที่เห็นดีกว่าสิ่งที่เกิดจากข้อมูลสุ่มจริงหรือไม่ และลดความเสี่ยงจากการค้นพารามิเตอร์จน overfit

## Four Stages

1. ประเมินกลยุทธ์ใน in-sample
2. ทำ in-sample permutation test จำนวนมาก เช่น 1,000+ ครั้ง และใช้เกณฑ์เข้มอย่าง p < 1%
3. ทดสอบ walk-forward out-of-sample
4. ทำ walk-forward permutation test เพื่อประเมินกระบวนการเลือกโมเดลทั้งชุด

## Caveat

การสับข้อมูลอาจทำลาย volatility clustering, autocorrelation และ long memory ทำให้ null distribution ไม่สมจริงและ p-value มองโลกดีเกินไป ต้องออกแบบ permutation ให้รักษาโครงสร้างที่เกี่ยวข้อง เช่น block/bootstrap variants และยังต้องควบคุม multiple testing, costs, slippage และ regime shifts

## Sources

- [Original Facebook post](https://www.facebook.com/permalink.php?story_fbid=pfbid02cagvjC7FmZjkP1dDF6wPZy3JPwaAMfGFhjpA593QyNZXvrtqRV1SCTDGajfipHjdl&id=61569334229421&__tn__=%2CO*F)
- [Referenced video](https://youtu.be/NLBXgSmRBgU)




