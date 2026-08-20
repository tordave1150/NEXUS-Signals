---
title: Asian Options and Martingale Optimal Transport
note_type: source
primary_topic: Investment
secondary_topics: [Quantitative Finance, Derivatives]
concepts: [Asian Option, Martingale Optimal Transport, Robust Pricing]
entities: [Florian Stebegg, Linn Engstrom, Sigrid Kallblad, Johan Karlsson]
tags: [asian-options, martingale-transport, robust-pricing]
source_type: Facebook Post
source_title: Option Pricing ไม่ได้มีแค่ Black-Scholes
source_author: GroundUp Academy
source_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid0sshFLUxwRF7VyxhzaJQfqLsfLQJWB22AnByEVYpbDrgYM3eXoNBdPmheZ22FfRzhl&id=61569334229421&__cft__[0]=AZad5Bv_eUqbTmxikhMscg4qcctykhkRyY9wt_U2EKW2mzMg8LenesA1oX1hHpWntIYqonKu5N6n7Dy5XWLFuX6-3gH85jlv6cDP5C6drZ6z1CsCU270eWoqRKIIhCPeY_af0j-E8jZR1IajExBWmt36BoBD7O-Ogsf5Irary5UFfA&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid0sshFLUxwRF7VyxhzaJQfqLsfLQJWB22AnByEVYpbDrgYM3eXoNBdPmheZ22FfRzhl&id=61569334229421"
source_date: 2026-05-27
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Asian Option]]", "[[Robust Pricing]]"]
---

# Asian Options and Martingale Optimal Transport

> [!summary] TL;DR
> Asian options ขึ้นกับเส้นทางราคา ไม่ใช่เฉพาะปลายทาง; Martingale Optimal Transport (MOT) ใช้ marginal distributions จากตลาดและ no-arbitrage/martingale constraints เพื่อหาขอบล่าง–บนของราคาแทนการเลือก stochastic model เดียว

## Verification

งานของ Stebegg ยืนยันการหา model-independent bounds สำหรับ Asian options แบบ discrete/continuous averaging และ characterize maximizing/minimizing models ในบางกรณี งาน Engstrom–Kallblad–Karlsson ใช้โครงสร้าง multi-marginal กับ entropic regularisation เพื่อเร่งการคำนวณ robust bounds สำหรับ Asian/lookback options

## Caveat

“Model-independent” ยังพึ่ง marginal calibration, market-quality assumptions, discretization และ constraint set; bounds อาจกว้างเกินใช้จริง และไม่เท่ากับราคาที่ trade ได้เมื่อรวม bid-ask, liquidity และ hedging costs

## Sources

- [Original Facebook post](https://www.facebook.com/permalink.php?story_fbid=pfbid0sshFLUxwRF7VyxhzaJQfqLsfLQJWB22AnByEVYpbDrgYM3eXoNBdPmheZ22FfRzhl&id=61569334229421&__cft__[0]=AZad5Bv_eUqbTmxikhMscg4qcctykhkRyY9wt_U2EKW2mzMg8LenesA1oX1hHpWntIYqonKu5N6n7Dy5XWLFuX6-3gH85jlv6cDP5C6drZ6z1CsCU270eWoqRKIIhCPeY_af0j-E8jZR1IajExBWmt36BoBD7O-Ogsf5Irary5UFfA&__tn__=%2CO%2CP-R)
- [Stebegg — arXiv:1412.1429](https://arxiv.org/abs/1412.1429)
- [Engstrom et al. — arXiv:2406.09959](https://arxiv.org/abs/2406.09959)

