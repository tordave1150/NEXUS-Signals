---
title: Time and Regime Filters for Crypto Momentum
note_type: source
primary_topic: Investment
secondary_topics: [Algorithmic Trading, Crypto]
concepts: [Donchian Breakout, ADX, Time Filter]
entities: [Investic Academy, BTC, ETH, SOL, XRP]
tags: [momentum, regime-filter, backtesting]
source_type: Facebook Post
source_title: เทรดน้อยลงเกือบครึ่ง แต่พอร์ตพลิกจากลบเป็นบวก
source_author: Investic Academy
source_url: "https://www.facebook.com/investic.academy/posts/pfbid02F7usXBe4DRbtztBaxkgFexUWhpo3CgY1M8W8dMjuwSTMss5BBGATV7GbxLtcs6mMl?__tn__=%2CO*F"
canonical_url: "https://www.facebook.com/investic.academy/posts/pfbid02F7usXBe4DRbtztBaxkgFexUWhpo3CgY1M8W8dMjuwSTMss5BBGATV7GbxLtcs6mMl"
source_date: 2026-06-12
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: summarized
confidence: Medium
related: ["[[Momentum Strategy]]", "[[Regime Filter]]"]
---

# Time and Regime Filters for Crypto Momentum

## What This Content Is About

โพสต์ทดลอง Donchian breakout บนข้อมูลรายชั่วโมงของคริปโตย้อนหลังสองปี แล้วเพิ่มตัวกรองชั่วโมง/วันและ ADX เพื่อให้ระบบ momentum เทรดเฉพาะสภาพแวดล้อมที่มีแนวโน้มชัด

## Reported Results

- กติกาพื้นฐาน: ทะลุ high 24 ชั่วโมงเข้า Long และหลุด low 24 ชั่วโมงออก
- ตัวอย่าง ETH: ไม่กรองรายงาน -19%, drawdown -57%, 167 เทรด; เพิ่มเวลา/วันเป็น +59%, DD -35%, 108 เทรด; เพิ่ม ADX > 25 เป็น +82%, DD -30%, 83 เทรด
- ตารางหลายสินทรัพย์รายงาน BTC -12% → +20%, ETH -29% → +65%, SOL -15% → +32% และ XRP +285% → +166% โดย XRP ลดกำไรแต่ drawdown ดีขึ้น
- โพสต์เสนอให้ใช้ ADX > 25 ยืนยัน momentum แต่กลับด้านเป็น ADX < 25 kill switch สำหรับ mean reversion

## Verification & Reconciliation

ผลลัพธ์ยังตรวจซ้ำไม่ได้เพราะไม่มี code/data ที่เปิดให้ตรวจ และตัวเลข ETH ในโพสต์ขัดกันเอง (-19%/+82% ในตัวอย่างหนึ่ง เทียบ -29%/+65% ในตารางหลายเหรียญ) นอกจากนี้ “Golden Hours” และ weekday filters อาจถูกเลือกจากข้อมูลชุดเดียวกับ backtest จึงเสี่ยง data snooping จำนวน 83–84 เทรดไม่เพียงพอจะยืนยันความทนทานเอง ต้องทำ walk-forward, nested selection, costs/slippage และทดสอบช่วงตลาดหลาย regime

## Sources

- [Original Facebook post](https://www.facebook.com/investic.academy/posts/pfbid02F7usXBe4DRbtztBaxkgFexUWhpo3CgY1M8W8dMjuwSTMss5BBGATV7GbxLtcs6mMl?__tn__=%2CO*F)


