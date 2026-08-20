---
title: Markov Property and Market Regimes
note_type: source
primary_topic: Investment
secondary_topics: [Statistics, Quantitative Finance]
concepts: [Markov Property, Markov Chain, Regime Detection]
entities: [Investic Academy]
tags: [markov-chain, regime, quantitative-finance]
source_type: Facebook Post
source_title: Markov Property — Does the Market Remember?
source_author: Investic Academy
source_url: "https://www.facebook.com/investic.academy/posts/pfbid02g9KCze4rFDCe8iJcnyRkdtJiG6THD7MUhJ3YVqMehUUJ4oQzuRUMqdJPBfTsE4Y3l?__tn__=%2CO*F"
canonical_url: "https://www.facebook.com/investic.academy/posts/pfbid02g9KCze4rFDCe8iJcnyRkdtJiG6THD7MUhJ3YVqMehUUJ4oQzuRUMqdJPBfTsE4Y3l"
source_date: 2026-06-28
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: High
related: ["[[Market Regime]]", "[[Markov Chain]]"]
---

# Markov Property and Market Regimes

## Summary

Markov property หมายถึงการแจกแจงของสถานะถัดไปขึ้นกับสถานะปัจจุบัน ไม่จำเป็นต้องใช้เส้นทางทั้งหมดที่ผ่านมา โพสต์เสนอให้แบ่งตลาดเป็น Bull / Neutral / Bear และใช้ transition probabilities เพื่อปรับกลยุทธ์ตาม regime ปัจจุบัน

## Reconciliation

คำกล่าวว่า momentum หรือ mean reversion เป็นการ “ออกจาก Markov” ต้องระวัง เพราะคุณสมบัติ Markov ขึ้นกับการนิยาม state หาก state รวมตัวแปรที่เกี่ยวข้องเพียงพอ กระบวนการยังอาจเป็น Markov ได้ การใช้โมเดล regime-switching จึงไม่ได้พิสูจน์ว่าตลาดจำหรือไม่จำอดีต แต่เป็นการย่อข้อมูลให้เป็น state ที่ใช้พยากรณ์ได้

## From Markov Chain to Hidden Regimes

เมื่อนิยาม bull/neutral/bear จากข้อมูลที่เห็นได้โดยตรง เราได้ finite-state chain และ transition matrix; เมื่อ regime เป็น latent state และ returns/volatility เป็น observations เราได้ HMM หรือ Markov-switching model การใช้ในตลาดรวมถึง regime detection, credit migration และ state-conditioned risk แต่ไม่ได้รับประกัน win rate และไม่มีหลักฐานสาธารณะเพียงพอให้สรุปว่า Renaissance ใช้ HMM แบบใด

## 🔎 In-depth Details

ความท้าทายอยู่ที่ **state design และ real-time inference**: label ที่สร้างจากผลตอบแทนอนาคตทำให้เกิด lookahead ทันที และ smoothed probabilities ที่ใช้ข้อมูลทั้งชุดไม่เท่ากับ filtered probabilities ที่มี ณ วันตัดสินใจ Workflow ที่ถูกต้องต้อง estimate ด้วยข้อมูลถึงเวลา `t`, บันทึก filtered state probability, ตัดสินใจสำหรับ `t+1` แล้ว roll window ไปข้างหน้า

ก่อนใช้ position จริง ให้ตรวจ stability ของ transition matrix, state duration, posterior uncertainty และผลหลัง costs เทียบกับ no-regime baseline หาก state สลับถี่เกินต้นทุนหรือ mapping ของ state เปลี่ยนเมื่อขยับ sample เล็กน้อย โมเดลยังไม่เป็น signal ที่ใช้งานได้

โพสต์ PopQuants dashboard เดิมระบุเพียงว่าอ่าน regime แบบ real time จาก order book แต่ไม่มี methodology, venue, latency หรือ validation จึงไม่เก็บเป็นโน้ตเครื่องมือแยก และไม่ใช้เป็นหลักฐานว่าการจำแนก state มี predictive edge

## Sources

- [Original Facebook post](https://www.facebook.com/investic.academy/posts/pfbid02g9KCze4rFDCe8iJcnyRkdtJiG6THD7MUhJ3YVqMehUUJ4oQzuRUMqdJPBfTsE4Y3l?__tn__=%2CO*F)
- [Merged post — Markov market signals](https://www.facebook.com/permalink.php?story_fbid=pfbid0AKRkqbxvJV2RW2QNCBkyQfCHcfsafX4o97LrxHqj7seePdsU7zAFXdJ5xftjQsmcl&id=61569334229421)
- [Merged post — Markov chains in finance and AI](https://www.facebook.com/mpirikabooks/posts/pfbid02zU39dZkeNLgJjsxG2MjY24e6ZwtGbPopBmT9Wc12MyH8jmAKLTV2eTaALYMoqMmSl)
- [NIST definition of a Markov process](https://www.itl.nist.gov/div898/handbook/apr/section1/apr171.htm)
- [Hamilton — Markov switching framework (NBER reference and extensions)](https://www.nber.org/papers/w16657)
- [Merged product announcement — PopQuants regime dashboard](https://www.facebook.com/popquants/posts/pfbid03587cjzrQ4wXE8fRYbae2qoiXmm4f6Zucstv1ATejKtck5aXxLEH6Bc2xz923m3XEl)


