---
title: CME OI and Order Book Reversal Heuristics
note_type: source
primary_topic: Investment
secondary_topics: [Gold Trading, Market Microstructure]
concepts: [Open Interest, Pending Orders, Liquidity Reversal]
entities: [CME, FXSSI, XAUUSD]
tags: [gold, order-book, open-interest]
source_type: Facebook Post
source_title: CME OI System with Order Book for gold reversals
source_author: Tawat Chaisiri
source_url: "https://www.facebook.com/tawat.chaisiri.9/posts/pfbid0229EfEQ1KtbW6aE6YU6sXJXANnzzi3vvd68nytxpakcmkmezdrdECiS16KKDbCkjVl?__cft__[0]=AZZCG8SK_8rFSPx-IF3fPXUygftGm00SbBqAvQyazLte_4O26ilchvXZTUQFfSveKDPzLj1yPdEcjdDwHAQQoDOwiplVCPzBi2oY2o6SGaJ7vOf3RcM1h0nJh8Ua9Pn-EscObfJ6LRMV0APsbnSxBLUdkvIukTWXdRjJp713AsHzfw&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/tawat.chaisiri.9/posts/pfbid0229EfEQ1KtbW6aE6YU6sXJXANnzzi3vvd68nytxpakcmkmezdrdECiS16KKDbCkjVl"
source_date: 2026-06-14
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: summarized
confidence: Low
related: ["[[Open Interest]]", "[[Gold Trading]]"]
---

# CME OI and Order Book Reversal Heuristics

## Reported Setup

โพสต์ผสมข้อมูล pending orders/position status จาก FXSSI กับ OI heatmap, round numbers, supply/demand zones และ CHOCH เพื่อหา “liquidity grab” ขาขึ้น/ขาลงใน XAUUSD

## Key Heuristics

- ฝั่งซื้อ: sell stops ใต้ราคา, loss buyers เพิ่ม, demand zone และโครงสร้างกลับขึ้น
- ฝั่งขาย: buy stops เหนือราคา, profit buyers, supply zone และ round number
- ใช้ contrarian interpretation ว่าการสะสม stop อาจดึงราคาไปกวาด liquidity แล้วกลับตัว

## Verification & Caveat

โพสต์ไม่ให้ methodology, sample, execution log หรือแหล่งเชื่อม CME OI กับ OTC/CFD XAUUSD อย่างตรวจสอบได้ Retail positioning ของผู้ให้บริการหนึ่งไม่เท่ากับ consolidated order book และ CME open interest เป็นจำนวนสัญญาคงค้าง ไม่เผยเจตนาหรือทิศทาง “smart money” โดยตรง เกณฑ์เปอร์เซ็นต์และ pattern เป็น heuristic ที่ต้อง backtest ด้วย timestamp ถูกต้อง, no look-ahead, spread/slippage และ regime separation

## Sources

- [Original Facebook post](https://www.facebook.com/tawat.chaisiri.9/posts/pfbid0229EfEQ1KtbW6aE6YU6sXJXANnzzi3vvd68nytxpakcmkmezdrdECiS16KKDbCkjVl?__cft__[0]=AZZCG8SK_8rFSPx-IF3fPXUygftGm00SbBqAvQyazLte_4O26ilchvXZTUQFfSveKDPzLj1yPdEcjdDwHAQQoDOwiplVCPzBi2oY2o6SGaJ7vOf3RcM1h0nJh8Ua9Pn-EscObfJ6LRMV0APsbnSxBLUdkvIukTWXdRjJp713AsHzfw&__tn__=%2CO%2CP-R)


