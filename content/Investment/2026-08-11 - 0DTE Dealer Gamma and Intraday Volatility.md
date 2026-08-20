---
title: 0DTE Dealer Gamma and Intraday Volatility
note_type: source
primary_topic: Investment
secondary_topics: [Options, Market Microstructure]
concepts: [0DTE, Dealer Gamma, Delta Hedging, Intraday Volatility]
entities: [Chukwuma Dim, Bjorn Eraker, Grigory Vilkov]
tags: [options, gamma, volatility]
source_type: Facebook Post and Research Paper
source_title: 0DTEs Trading Gamma Risk and Volatility Propagation
source_author: Investic Academy and paper authors
source_url: "https://www.facebook.com/investic.academy/posts/pfbid02pTFyK1iH93JYaBisGtU1boFoAem171rDLx9s86w2DtPN9pgsTBU9SzR6yWx1HDjql?__cft__[0]=AZaBfiAgOiQMSWWdWhVKV6r6Op87IQ2IICpb1Sn9wJGHsKjOOlWHuf6zS_q34vs85rpJw3TbkkCc5t4aJ3mh3qqSHLMkKnyKreqZyld89skEP44k3BmhXJhO2fQC0g2CRowInTkzsXFEyYpjxHKh9HnagPLUTealjjjlYuUg5v6gow&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/investic.academy/posts/pfbid02pTFyK1iH93JYaBisGtU1boFoAem171rDLx9s86w2DtPN9pgsTBU9SzR6yWx1HDjql"
source_date: 2026-08-11
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: High
related: ["[[Dealer Gamma]]", "[[Intraday Market Structure]]"]
---

# 0DTE Dealer Gamma and Intraday Volatility

## Finding

งานศึกษาข้อมูล S&P 500 options พบว่า inventory gamma ของ market maker ในตัวอย่างเป็นบวกโดยเฉลี่ยและสัมพันธ์เชิงลบกับความผันผวน intraday ในอนาคต กลไกสอดคล้องกับ delta hedging: long gamma มักซื้อเมื่อราคาลงและขายเมื่อราคาขึ้น จึงส่งเสริม reversal ส่วน negative gamma สอดคล้องกับ momentum และการขยายความผันผวน

## Interpretation

ปริมาณ 0DTE สูงเพียงอย่างเดียวจึงไม่ระบุทิศทางผลกระทบ ต้องดู sign และขนาดของ dealer gamma ด้วย หลักฐานเป็นความสัมพันธ์เชิงประจักษ์ในช่วงตัวอย่างและใช้การประมาณสถานะ market maker; ไม่ควรสรุปว่า 0DTE ลดความผันผวนเสมอหรือใช้ gamma estimate จากผู้ให้บริการต่างรายแทนกันโดยไม่ตรวจวิธีคำนวณ

## Open Interest, Strikes, and Gold Examples

โน้ตเดิมเรื่องทองและ gamma levels ถูกรวมที่นี่: OI บอกจำนวนสัญญาคงค้าง แต่ไม่บอก opening/closing, trade sign หรือว่า dealer ถือด้านใด ระดับ strike ที่กระจุกจึงเป็นเพียง heuristic; อาจเกิด pinning/dampening เมื่อ dealer long gamma หรือเร่งราคาเมื่อ short gamma ทั้งนี้ expiry, intraday flow, futures basis และ liquidity เปลี่ยนผลได้ ตัวอย่างทำกำไรหนึ่งครั้งและหนังสือเชิงโฆษณาไม่ใช่หลักฐาน edge

## 🔎 In-depth Details

การอนุมาน market impact ต้องแยก `volume → inventory → gamma sign → hedge flow`: volume สูงไม่จำเป็นต้องสร้าง inventory สุทธิ หาก customer buys/sells สมดุลกัน Cboe อธิบายว่าตลาด maker ที่ long gamma มีแนวโน้ม hedge สวนการเคลื่อนไหว (ขายเมื่อขึ้น/ซื้อเมื่อลง) ขณะที่ short gamma hedgeตามทิศและอาจขยาย move แต่เป็น “potential mechanism” ไม่ใช่กฎทำนายราคาทุกวัน

ก่อนใช้ GEX/OI heatmap ให้บันทึกวิธีประมาณ dealer side, contract multiplier, spot/forward, implied volatility, time-to-expiry และ timestamp แล้วทำ event study แยก long/short-gamma regimes หลัง costs หาก provider สองรายให้ gamma sign ต่างกัน ให้ถือว่า model uncertainty สูงและลด/งด position แทนเลือกค่าที่เข้ากับ thesis

## Sources

- [Original Facebook post](https://www.facebook.com/investic.academy/posts/pfbid02pTFyK1iH93JYaBisGtU1boFoAem171rDLx9s86w2DtPN9pgsTBU9SzR6yWx1HDjql?__cft__[0]=AZaBfiAgOiQMSWWdWhVKV6r6Op87IQ2IICpb1Sn9wJGHsKjOOlWHuf6zS_q34vs85rpJw3TbkkCc5t4aJ3mh3qqSHLMkKnyKreqZyld89skEP44k3BmhXJhO2fQC0g2CRowInTkzsXFEyYpjxHKh9HnagPLUTealjjjlYuUg5v6gow&__tn__=%2CO%2CP-R)
- [SSRN paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4692190)
- [Merged post — gold options open interest](https://www.facebook.com/investic.academy/posts/pfbid05RGCnG9LggbXzX6pZaS9DVqCY2zE4bY6ojA92epHJKFypX5jWYvFzrijRE8qLoAfl)
- [Merged post — gamma hedging in both directions](https://www.facebook.com/investic.academy/posts/pfbid02i2Jj2uHvkt8AcG78VtMD3pYiM8qXfSdasLJudqhK6vEWnXccS4TR5w7oGiW1UPGul)
- [Merged post — call flow does not imply direction](https://www.facebook.com/investic.academy/posts/pfbid036WiFFZr5CmiRdNs9Yk3W1gMZgZmE3i9Aqz8bJ2oeDwikw6DagVJ5beh2jmAx6m9El)
- [Merged post — conditional gamma levels](https://www.facebook.com/investic.academy/posts/pfbid03VkzwLZSpbsSdnfdBuPHDz7VmPEsuGMDk9m8UUL1rh5M5seTtBSxc1ZMzwroF1WYl)
- [Merged promotional source — The Invisible Money](https://www.facebook.com/investic.academy/posts/pfbid02TiXaV2pK1DSVji4aZt1sQAEieRVadHxN2djYcYuYBWKCfa6XNppGRWdoytDYzv6Bl)
- [Cboe — Evaluating the Market Impact of SPX 0DTE Options](https://www.cboe.com/insights/posts/volatility-insights-evaluating-the-market-impact-of-spx-0-dte-options/)




