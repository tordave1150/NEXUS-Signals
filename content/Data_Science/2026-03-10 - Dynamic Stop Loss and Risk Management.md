---
title: Dynamic Stop Loss และ Risk Management
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Statistics]
concepts: [Stop Loss, Stochastic Volatility, Capital Preservation]
entities: [Chaipat Nengcomma]
tags: [risk-management, stop-loss, volatility]
source_type: Facebook Post
source_title: Risk management mastery - The key to successful trading
source_author: Chaipat Nengcomma
source_url: "https://www.facebook.com/chaipat.ncm/posts/pfbid0eTu88cTqthQGLV6hJkMjRCbf9NpNnisz1Wmcr86WDgMXFak2dKTGgV1CNz53ryiHl?__cft__[0]=AZa2pTZsyldRgFsqbOymYHZ3JwIlUNlUXJhsYoz7MXQu89wsaO6zR-TfMzk_HUbrylOPMQJggh-7XScKY43qTiuuo5EnxKg9Il3YaAMmzsjNY5jr_XXehlMTf2miCEkJHNi0d3OVEKEqRgvzEgIq2g1iG8SBsoKU0jDZ2sutIxHmRg&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/chaipat.ncm/posts/pfbid0eTu88cTqthQGLV6hJkMjRCbf9NpNnisz1Wmcr86WDgMXFak2dKTGgV1CNz53ryiHl"
source_date: 2026-03-10
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: Medium-Low
related: ["[[Trading Risk Management]]", "[[Stochastic Volatility]]"]
---

# Dynamic Stop Loss และ Risk Management

> [!summary] TL;DR
> Stop-loss และ target price ควรสัมพันธ์กับ volatility, horizon และ payoff distribution มากกว่าระยะคงที่ แต่โมเดลเพียงอย่างเดียวไม่สร้าง positive EV หาก signal ต้นทางไม่มี edge

## Important Details

โพสต์กล่าวถึงการคำนวณโอกาสชน TP/SL ด้วย GBM เปรียบเทียบ finite-time กับ continuous-time/dynamic framework และใช้ volatility-based levels เพื่อหา risk–reward ratio ที่เปลี่ยนตามตลาด

## Verification & Reconciliation

คำกล่าวว่า dynamic stop สามารถ “ให้ EV บวก” ต้องมีเงื่อนไขของ drift, costs, slippage และ entry rule; การจัดการทางออกไม่สามารถเปลี่ยนกลยุทธ์ที่มี expected return ติดลบให้เป็นบวกได้เสมอ GBM และ stochastic volatility เป็นคนละระดับของแบบจำลอง และโพสต์ไม่ได้ให้รายละเอียดพอประเมิน implementation

## Sources

- [Original Facebook post](https://www.facebook.com/chaipat.ncm/posts/pfbid0eTu88cTqthQGLV6hJkMjRCbf9NpNnisz1Wmcr86WDgMXFak2dKTGgV1CNz53ryiHl?__cft__[0]=AZa2pTZsyldRgFsqbOymYHZ3JwIlUNlUXJhsYoz7MXQu89wsaO6zR-TfMzk_HUbrylOPMQJggh-7XScKY43qTiuuo5EnxKg9Il3YaAMmzsjNY5jr_XXehlMTf2miCEkJHNi0d3OVEKEqRgvzEgIq2g1iG8SBsoKU0jDZ2sutIxHmRg&__tn__=%2CO%2CP-R)
