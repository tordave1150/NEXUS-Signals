---
title: Financial Market Stylized Facts - เมื่อข้อมูลจริงต่างจากโมเดลเรียบง่าย
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Statistics]
concepts: [Fat Tails, Volatility Clustering, Dynamic Correlation]
entities: [QuantCorner]
tags: [statistics, market-risk, quantitative-finance]
source_type: Facebook Post
source_title: Market Stylized Facts 2
source_author: QuantCorner
source_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid0aLBaskpY7uAT8xRZFUgvJV1K6bMbC9msD9zdZTav2RprRtwqQ7asyNvpSemYQNgel?__cft__[0]=AZbWdm6juR8h7r5GD2dwYyjrxUbN6hH9u3_Uwiyp4oMdwF0tMMA9rEwlAKxrku7eW63uOOolNV7Lk_FEBOsbwRlYYdesXFx1Wz4mrKGATu8XURZytlGNkIB2YqtP805yofKZ9BAap26c_KbRMoYlz0TswF7vB9n7FmgNseV1i5X9WA&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/quantcornerthailand/posts/pfbid0aLBaskpY7uAT8xRZFUgvJV1K6bMbC9msD9zdZTav2RprRtwqQ7asyNvpSemYQNgel"
source_date: 2026-03-21
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: High
related: ["[[Fat Tails]]", "[[Volatility Clustering]]"]
---

# Financial Market Stylized Facts

> [!summary] TL;DR
> ผลตอบแทนจริงมักมี fat tails และ skewness, volatility มี persistence และ correlation เปลี่ยนตามเวลา โดยเฉพาะช่วงวิกฤต จึงไม่ควรใช้ Gaussian/static-correlation assumptions แบบไม่ทดสอบ

## Key Takeaways

- Normal distribution มักประเมิน tail risk ต่ำไป
- Random walk ในระดับผลตอบแทนเฉลี่ยไม่ขัดกับ volatility clustering; ต้องแยก predictability ของ mean กับ variance
- Correlation ที่สูงขึ้นในช่วง stress ทำให้ diversification อ่อนแรง
- ควรเสริม simulation, scenario analysis และ dynamic risk models

## Verification & Reconciliation

ข้อสรุปสอดคล้องกับวรรณกรรม econometrics และ market risk โดยทั่วไป แต่การกล่าวว่า CAPM หรือ Mean–Variance “สมมติ normality” โดยตรงอาจกว้างเกินไป: ผลลัพธ์บางส่วนต้องการสมมติฐานที่อ่อนกว่านั้น ข้อจำกัดจริงอยู่ที่การประมาณ moments และความไม่เสถียรของ distribution

## 🔎 In-depth Details

“ไม่เป็น Normal” ไม่ได้บอกโดยตรงว่าควรใช้ distribution ใด ความเสี่ยงจริงมาจากหลายกลไกร่วมกัน: unconditional returns อาจมี fat tails เพราะ volatility เปลี่ยนตามเวลา, residuals หลังปรับ volatility แล้วยังมี conditional heavy tails, และ dependence ระหว่างสินทรัพย์สูงขึ้นในช่วง stress ดังนั้นการเปลี่ยน Gaussian เป็น Student-t อย่างเดียวอาจยังพลาด regime shift, jumps และ liquidity feedback

สำหรับงาน risk management ให้แยกเครื่องมือเป็นสามชั้น: (1) forecast ความผันผวน/ความสัมพันธ์แบบ time-varying (2) tail model หรือ historical simulation และ (3) scenario stress ที่ไม่ผูกกับความถี่ในอดีต ตรวจ exceedance ของ VaR/ES ตามเวลาและบันทึกว่าความผิดพลาดมาจาก mean, volatility, correlation หรือ liquidity assumption เพื่อแก้ model risk ตรงจุด

> [!important] Model choice
> ใช้ Gaussian เป็น baseline เพื่อเทียบ calibration ได้ แต่ห้ามให้ baseline เป็นกรอบความเสี่ยงเพียงชั้นเดียว

## Sources

- [Original Facebook post](https://www.facebook.com/quantcornerthailand/posts/pfbid0aLBaskpY7uAT8xRZFUgvJV1K6bMbC9msD9zdZTav2RprRtwqQ7asyNvpSemYQNgel?__cft__[0]=AZbWdm6juR8h7r5GD2dwYyjrxUbN6hH9u3_Uwiyp4oMdwF0tMMA9rEwlAKxrku7eW63uOOolNV7Lk_FEBOsbwRlYYdesXFx1Wz4mrKGATu8XURZytlGNkIB2YqtP805yofKZ9BAap26c_KbRMoYlz0TswF7vB9n7FmgNseV1i5X9WA&__tn__=%2CO%2CP-R)
- [Merged post — normal distribution and option-model caveats](https://www.facebook.com/permalink.php?story_fbid=pfbid0wuBfU5fnknJJ5VpXtCBp4sPwWKdHXrEzkLgRsosHeDDRP53iQAq8JtL4bC5uSGxcl&id=100076198440403)
- [Merged post — fat tails and Black Monday](https://www.facebook.com/investic.academy/posts/pfbid02veLmyPHFcxRdRABafESEdVmTw6WPhsUjXfYPX9G2TEr77xRnoGY5N2PDHBL4ApYLl)
- [Cont — Empirical Properties of Asset Returns](https://doi.org/10.1080/713665670)
