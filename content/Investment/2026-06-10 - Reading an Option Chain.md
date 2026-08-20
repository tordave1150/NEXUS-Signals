---
title: Reading an Option Chain
note_type: source
primary_topic: Investment
secondary_topics: [Options, Education]
concepts: [Option Chain, Greeks, Implied Volatility]
entities: [Calls, Puts]
tags: [options, option-chain, greeks]
source_type: Facebook Post
source_title: วิธีอ่าน Option Chain
source_author: สำนักพิมพ์เอ็มพิริก้าบุ๊คส์
source_url: "https://www.facebook.com/mpirikabooks/posts/pfbid02aq88iiCrPMCJGDB9pHznmKLjh6C5zNhFfPxS7hiec4pxREqMXhAkmsZnLAebyZLjl?__tn__=%2CO*F"
canonical_url: "https://www.facebook.com/mpirikabooks/posts/pfbid02aq88iiCrPMCJGDB9pHznmKLjh6C5zNhFfPxS7hiec4pxREqMXhAkmsZnLAebyZLjl"
source_date: 2026-06-10
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: summarized
confidence: Medium
related: ["[[Options]]", "[[Greeks]]"]
---

# Reading an Option Chain

> [!summary] TL;DR
> Option chain จัดข้อมูลตาม underlying, expiration และ strike โดยทั่วไปวาง calls ทางซ้าย puts ทางขวา พร้อม bid/ask, size, volume, implied volatility และ Greeks สำหรับแต่ละสัญญา

## Reading Checklist

- ยืนยัน underlying และ expiration ก่อนเทียบ strike
- ดู bid/ask และ size ควบคู่ volume/open interest เพื่อประเมิน liquidity
- ตรวจ multiplier; สัญญาหุ้นสหรัฐจำนวนมากแทน 100 หุ้น แต่ไม่ใช่กฎสากล
- แยก ITM/ATM/OTM และดู IV ตาม strike/expiry ไม่ใช้ค่า ATM ค่าเดียวแทนทั้ง surface
- Delta วัด sensitivity ต่อ underlying, Gamma วัดการเปลี่ยนของ Delta และ Vega วัด sensitivity ต่อ IV

## Corrections and Caveats

Delta ของ call เช่น 0.606 ไม่ใช่ “โอกาส ITM 60.6%” แบบรับประกัน แม้ใช้เป็นค่าประมาณภายใต้โมเดลและสมมติฐานบางชุด Gamma มักสูงใกล้ ATM และเพิ่มเมื่อใกล้หมดอายุ ส่วน Vega โดยทั่วไปสูงกว่าเมื่อเวลาคงเหลือมาก แต่รูปทรงขึ้นกับโมเดล/ตลาด ต้องรวม theta, rates, dividends, early exercise, spread และ contract specification จริงก่อนตัดสินใจ

## Sources

- [Original Facebook post](https://www.facebook.com/mpirikabooks/posts/pfbid02aq88iiCrPMCJGDB9pHznmKLjh6C5zNhFfPxS7hiec4pxREqMXhAkmsZnLAebyZLjl?__tn__=%2CO*F)




