---
title: Algorithmic Trading, AI และผลกระทบต่อตลาด
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Artificial Intelligence]
concepts: [Algorithmic Trading, Market Microstructure, High-Frequency Trading]
entities: [SEC, CFTC, Knight Capital]
tags: [algorithmic-trading, market-microstructure, ai]
source_type: Facebook Post
source_title: Algorithmic Trading and AI - Strategies and Market Impact
source_author: Chaipat Nengcomma
source_url: "https://www.facebook.com/chaipat.ncm/posts/pfbid0yCecRMqA6bEEcytF3QhRbNMWFcJhvbLHyw2W1zbD74FS7hPEv4iziEWb5g3vKBUHl?__cft__[0]=AZa5gYVBtbdanq3Icn_ny7RIn7t4fuXkDbWJfF2Chn4tsAcFn2-pxn-sSwZxi_6M6cfgwggNWSefaCWgjg2XJmKw9e0oPz9AyV-7417VWRk9BXNVxUWprDbZ_2stcFvGsBN7nitrFFeL8IyEnzZpv2jOE5zG9bClmcDvfGt72uWhcQ&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/chaipat.ncm/posts/pfbid0yCecRMqA6bEEcytF3QhRbNMWFcJhvbLHyw2W1zbD74FS7hPEv4iziEWb5g3vKBUHl"
source_date: 2026-02-26
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Algorithmic Trading]]", "[[Market Microstructure]]"]
---

# Algorithmic Trading, AI และผลกระทบต่อตลาด

> [!summary] TL;DR
> Algorithmic trading ช่วยเพิ่มความเร็ว สภาพคล่อง และ price discovery ในภาวะปกติ แต่เมื่อผู้ให้สภาพคล่องถอนคำสั่งพร้อมกันหรือระบบผิดพลาด ก็สามารถขยายความผันผวนและความเสี่ยงเชิงระบบได้

## Important Details

โพสต์กล่าวถึง trend following, statistical arbitrage, market making และ HFT พร้อมตัวอย่าง Flash Crash วันที่ 6 พฤษภาคม 2010 และความเสียหายของ Knight Capital ในปี 2012 นอกจากนี้ยังมองว่า NLP/LLM จะเพิ่มบทบาทของข้อมูลไม่มีโครงสร้างในการวิเคราะห์ sentiment

## Verification & Reconciliation

รายงาน SEC ต่อสภาคองเกรสสรุปว่างานศึกษาส่วนใหญ่ไม่เห็นว่า HFT เป็นตัวก่อ Flash Crash โดยตรง แต่การถอนสภาพคล่องและปฏิกิริยาของอัลกอริทึมมีส่วนสร้างวงจรป้อนกลับเชิงลบ จึงควรใช้ถ้อยคำว่า “มีส่วนขยายเหตุการณ์” มากกว่า “เป็นสาเหตุเดียว”

## Things Worth Remembering

- แยก algorithmic trading ออกจาก HFT; HFT เป็นเพียงกลุ่มย่อย
- ประสิทธิภาพในภาวะปกติไม่รับประกัน resilience ในภาวะเครียด
- ระบบจริงต้องมี pre-trade controls, kill switch, monitoring และการทดสอบกรณีผิดปกติ

## Sources

- [Original Facebook post](https://www.facebook.com/chaipat.ncm/posts/pfbid0yCecRMqA6bEEcytF3QhRbNMWFcJhvbLHyw2W1zbD74FS7hPEv4iziEWb5g3vKBUHl?__cft__[0]=AZa5gYVBtbdanq3Icn_ny7RIn7t4fuXkDbWJfF2Chn4tsAcFn2-pxn-sSwZxi_6M6cfgwggNWSefaCWgjg2XJmKw9e0oPz9AyV-7417VWRk9BXNVxUWprDbZ_2stcFvGsBN7nitrFFeL8IyEnzZpv2jOE5zG9bClmcDvfGt72uWhcQ&__tn__=%2CO%2CP-R)
- [SEC Report to Congress on Algorithmic Trading](https://www.sec.gov/files/Algo_Trading_Report_2020.pdf)

