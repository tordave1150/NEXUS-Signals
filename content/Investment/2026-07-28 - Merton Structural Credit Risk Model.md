---
title: Merton Structural Credit Risk Model
note_type: source
primary_topic: Investment
secondary_topics: [Credit Risk, Options]
concepts: [Structural Model, Equity as Call Option, Distance to Default]
entities: [Robert C. Merton, Moody's KMV]
tags: [merton-model, credit-risk, corporate-debt]
source_type: Facebook Post and Original Paper
source_title: On the Pricing of Corporate Debt
source_author: เจ้าม่วง and Robert C. Merton
source_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid036i514eLdkjMuehwLET7vPPWEcoCNrgBh7CmsqHLQ6C4nXCXRhyV7sT34MQbhYRGkl&id=61585718400443&__cft__[0]=AZatt7Ee2_fJcbYOn8105rdI_j8dZAx6k4NE1DnjMii4UM-gaOpmIGsBBrOCJJHSRn25F1CyfUdgRduRl9l8o1iuDJTzXrnyO_BMzhG1mN2m-Wj8IzcOmsyYjABpAWDbgSTTO_IAYPxAi3-4BD9lzRwMUrW_ZK0toKq475drKf_ALw&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid036i514eLdkjMuehwLET7vPPWEcoCNrgBh7CmsqHLQ6C4nXCXRhyV7sT34MQbhYRGkl&id=61585718400443"
source_date: 2026-07-28
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: verified
confidence: High
related: ["[[Credit Risk Model]]", "[[Black Scholes]]"]
---

# Merton Structural Credit Risk Model

## Core Structure

Merton (1974) มอง equity ณ วันครบกำหนดเป็น call option บนมูลค่าสินทรัพย์บริษัท: หากสินทรัพย์ V สูงกว่าหนี้ B ผู้ถือหุ้นได้ `V-B`; หากต่ำกว่าหนี้ ผู้ถือหุ้นปล่อย default และ payoff เป็นศูนย์ ทำให้ราคาหนี้และ credit spread เชื่อมกับ leverage, asset volatility และ maturity

## Correction and Limits

คำว่า paper นี้ “ได้รับรางวัลโนเบล” ไม่ตรงนัก: Merton และ Myron Scholes ได้รางวัลปี 1997 สำหรับวิธีประเมิน derivatives โดยรวม ไม่ใช่รางวัลเฉพาะบทความนี้ โมเดลดั้งเดิมสมมติ capital structure เรียบง่าย, continuous trading, flat known rate และ default ที่ maturity; งานจริงจึงต้องปรับ coupon debt, early default, jumps และ asset-value estimation

## Sources

- [Original Facebook post](https://www.facebook.com/permalink.php?story_fbid=pfbid036i514eLdkjMuehwLET7vPPWEcoCNrgBh7CmsqHLQ6C4nXCXRhyV7sT34MQbhYRGkl&id=61585718400443&__cft__[0]=AZatt7Ee2_fJcbYOn8105rdI_j8dZAx6k4NE1DnjMii4UM-gaOpmIGsBBrOCJJHSRn25F1CyfUdgRduRl9l8o1iuDJTzXrnyO_BMzhG1mN2m-Wj8IzcOmsyYjABpAWDbgSTTO_IAYPxAi3-4BD9lzRwMUrW_ZK0toKq475drKf_ALw&__tn__=%2CO%2CP-R)
- [Merton's 1974 paper](https://onlinelibrary.wiley.com/doi/10.1111/j.1540-6261.1974.tb03058.x)


