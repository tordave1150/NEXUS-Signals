---
title: Three-Matrix Portfolio Learning
note_type: source
primary_topic: Investment
secondary_topics: [Portfolio Construction, Machine Learning]
concepts: [Return Rank Transition, Volatility Rank Transition, Correlation Distance]
entities: [Igor Halperin]
tags: [portfolio-optimization, markov-chain, ranking]
source_type: Facebook Post and Research Paper
source_title: Are Three Matrices All You Need To Beat the Market?
source_author: QuantCorner and Igor Halperin
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid01UU4NSLPumsEE99kC8Dois4r2yGLojjWsXkuuHfnTcvDnE8s9QiP3WpAvffzpWR5l?__cft__[0]=AZagv9dQ0OqV0dp2ODALmh9dswyVgE5Ns6nmPv3FULo4p_oXhLRQGMVkixBYnjRnO6md6xn4WqWieX3HpvK-4-Qvf6gxFxGJhe1LmHqziZsACq28yG3xMO5U8TG4eDCgB21UcEKbzsW0eTtGIBWJw2rvRvJznlmBdoVu_sh9THjaqw&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid01UU4NSLPumsEE99kC8Dois4r2yGLojjWsXkuuHfnTcvDnE8s9QiP3WpAvffzpWR5l"
source_date: 2026-08-10
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: verified
confidence: High
related: ["[[Portfolio Optimization]]", "[[Cross-Sectional Ranking]]"]
---

# Three-Matrix Portfolio Learning

## Finding

paper แทน expected-return vector และ covariance matrix ด้วย correlation-distance matrix และ Markov transition matrices ของอันดับผลตอบแทนกับอันดับความผันผวนรายเดือนในหุ้น S&P 500 ผู้เขียนพบว่า volatility rank พยากรณ์ล่วงหน้าได้มากกว่า return rank และนำคะแนนไปผสม market-neutral momentum กับ long-only sleeve

## Evidence and Limits

ผู้เขียนรายงาน Sharpe สุทธิค่าซื้อขาย 5 bps เท่ากับ 1.06 และ 1.32 ใน OOS สองช่วง เทียบตลาด 0.78 และ 1.14; residual-distance diversification เพิ่มเป็น 1.08 และ 1.44 ตัวเลขเหล่านี้เป็นผลของงานเดียวและข้อมูลถึงกรกฎาคม 2026 จึงต้อง replication ด้วยข้อมูล point-in-time, exposure attribution และต้นทุนที่เหมาะกับขนาดพอร์ต ก่อนตีความคำว่า beat the market

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid01UU4NSLPumsEE99kC8Dois4r2yGLojjWsXkuuHfnTcvDnE8s9QiP3WpAvffzpWR5l?__cft__[0]=AZagv9dQ0OqV0dp2ODALmh9dswyVgE5Ns6nmPv3FULo4p_oXhLRQGMVkixBYnjRnO6md6xn4WqWieX3HpvK-4-Qvf6gxFxGJhe1LmHqziZsACq28yG3xMO5U8TG4eDCgB21UcEKbzsW0eTtGIBWJw2rvRvJznlmBdoVu_sh9THjaqw&__tn__=%2CO%2CP-R)
- [Research paper](https://arxiv.org/abs/2607.27461)




