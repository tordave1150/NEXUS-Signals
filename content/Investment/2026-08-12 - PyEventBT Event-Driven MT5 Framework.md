---
title: PyEventBT Event-Driven MT5 Framework
note_type: source
primary_topic: Investment
secondary_topics: [Backtesting, Trading Systems]
concepts: [Event-Driven Architecture, MetaTrader 5, Simulated Execution, Live Trading]
entities: [PyEventBT, Martí Castany, MetaTrader 5]
tags: [backtesting, event-driven, mt5]
source_type: Facebook Post and GitHub Repository
source_title: PyEventBT
source_author: Chaipat and Martí Castany
source_url: "https://www.facebook.com/chaipat.ncm/posts/pfbid02nS5PZYt6ztqHRkWLrkfUhfLV73B8Prozu6NwdkGFsmVgQ6YQDE9c6pcWMqViEWPpl?__cft__[0]=AZYh9igzl9A18P_l9yL4Krf8aUTHKLAYk0oDed7oA4amTy3xQ8f_wA4REmr7Ka_P_CA_ibStDFRcyjKA9iksRrCzViJUu2Uwe9gG85n9a-JPn27s7GQiRJIf-2ioQvKrd9z_kHJvcdt_He2WgzPiC8WNEp7AqHitOm88ttrcZ-_0aA&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/chaipat.ncm/posts/pfbid02nS5PZYt6ztqHRkWLrkfUhfLV73B8Prozu6NwdkGFsmVgQ6YQDE9c6pcWMqViEWPpl"
source_date: 2026-08-12
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: verified
confidence: High
related: ["[[Event-Driven Backtesting]]", "[[MetaTrader 5]]"]
---

# PyEventBT Event-Driven MT5 Framework

## Verified Features

PyEventBT เป็น Python framework แบบ event-driven สำหรับ backtest และ live trading บน MetaTrader 5 โดยแยกเส้นทาง Bar → Signal → Sizing → Risk → Order → Fill → Portfolio รองรับข้อมูลย้อนหลังจาก CSV, feed แบบ real-time และ execution ทั้งจำลองกับจริง

## Engineering Caveat

สถาปัตยกรรม event-driven ช่วยทำให้ timing convention และการจำลองคำสั่งชัดเจน แต่ไม่ได้ป้องกัน look-ahead bias โดยอัตโนมัติ ผู้ใช้ยังต้องตรวจ timestamp, bar availability, execution delay, spread, slippage, market impact และความแตกต่างระหว่าง simulated กับ broker fills

## Sources

- [Original Facebook post](https://www.facebook.com/chaipat.ncm/posts/pfbid02nS5PZYt6ztqHRkWLrkfUhfLV73B8Prozu6NwdkGFsmVgQ6YQDE9c6pcWMqViEWPpl?__cft__[0]=AZYh9igzl9A18P_l9yL4Krf8aUTHKLAYk0oDed7oA4amTy3xQ8f_wA4REmr7Ka_P_CA_ibStDFRcyjKA9iksRrCzViJUu2Uwe9gG85n9a-JPn27s7GQiRJIf-2ioQvKrd9z_kHJvcdt_He2WgzPiC8WNEp7AqHitOm88ttrcZ-_0aA&__tn__=%2CO%2CP-R)
- [PyEventBT repository](https://github.com/marticastany/pyeventbt)




