---
title: Kelly Criterion for Position Sizing
note_type: source
primary_topic: Investment
secondary_topics: [Risk Management, Information Theory]
concepts: [Kelly Criterion, Log Growth, Fractional Kelly]
entities: [John L. Kelly Jr., Bell Labs]
tags: [kelly-criterion, position-sizing, risk]
source_type: Facebook Post and Original Paper
source_title: The Kelly Criterion
source_author: FIRE เกษียณก่อนกำหนด and John L. Kelly Jr.
source_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid02n41tEcRdU73uBErvGaohJ6BZpYCPB6m5ikcD6pacWWTXTqN9VjZr47KEsJkQrCv4l&id=61574928686427&__tn__=%2CO*F"
canonical_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid02n41tEcRdU73uBErvGaohJ6BZpYCPB6m5ikcD6pacWWTXTqN9VjZr47KEsJkQrCv4l&id=61574928686427"
source_date: 2026-07-13
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: High
related: ["[[Position Sizing]]", "[[Log Utility]]"]
---

# Kelly Criterion for Position Sizing

## Core Rule

สำหรับเดิมพัน binary ที่ชนะด้วยความน่าจะเป็น p, แพ้ q และได้กำไรสุทธิ b ต่อหนึ่งหน่วย สูตร `f* = (bp-q)/b` ให้สัดส่วนที่ maximize long-run expected log wealth ตัวอย่าง p=0.6, b=1 ให้ Full Kelly 20%

## Practical Limits

Kelly ตอบ “ลงเท่าไรเมื่อ edge ถูกต้อง” ไม่ได้บอกว่าควรซื้ออะไร และไวมากต่อ estimation error, nonstationarity, fat tails และความสัมพันธ์ระหว่าง positions การลงเกิน Kelly ลด growth และเพิ่ม drawdown จึงนิยม fractional Kelly เช่น half-Kelly แต่สัดส่วนที่เหมาะต้องคำนวณจาก distribution และ constraints จริง ไม่ใช่กฎครึ่งหนึ่งตายตัว

## 🔎 In-depth Details

Kelly เป็น **objective เรื่องอัตราเติบโตระยะยาว** ไม่ใช่ drawdown control: ต่อให้ประมาณ edge ถูก Full Kelly ก็ยังรับเส้นทางความมั่งคั่งที่ผันผวนมากได้ และเมื่อ `p` หรือ payoff ถูกประเมินสูงเกินจริง ขนาดที่คำนวณจะสูงเกินอย่างเป็นระบบ การใช้ fractional Kelly จึงควรมองเป็น shrinkage ต่อความไม่แน่นอน ไม่ใช่สูตร `0.5×` ที่ใช้ได้ทุกกรณี

กรอบใช้งานที่ปลอดภัยกว่าคือคำนวณ Kelly จากผลตอบแทนสุทธิหลัง fees/slippage แล้วจำกัดด้วย volatility target, concentration limit, gap/liquidation stress และ portfolio correlation จากนั้นทดสอบหลายค่าของ edge แทนการใช้ point estimate เดียว หากขนาดเปลี่ยนมากเมื่อขยับสมมติฐานเพียงเล็กน้อย แปลว่า **ข้อมูลยังไม่รองรับ leverage นั้น**

> [!important] Decision rule
> ใช้ Kelly เป็นเพดานเชิงทฤษฎี แล้วให้ risk budget และ stress loss เป็นเพดานปฏิบัติ; เลือกค่าที่ต่ำที่สุดในสามกรอบ

## Sources

- [Original Facebook post](https://www.facebook.com/permalink.php?story_fbid=pfbid02n41tEcRdU73uBErvGaohJ6BZpYCPB6m5ikcD6pacWWTXTqN9VjZr47KEsJkQrCv4l&id=61574928686427&__tn__=%2CO*F)
- [Merged Facebook post — extreme sizing risks](https://www.facebook.com/cwayinvestment/posts/pfbid0288R3AgJsB9vhrtPNUAZUThvcXoNxXJK4jgqzmuyF7cE7At3xaBamc64jLijFm4VFl)
- [Kelly's 1956 paper](https://onlinelibrary.wiley.com/doi/abs/10.1002/j.1538-7305.1956.tb03809.x)
- [Leverage and Uncertainty — fractional Kelly under drawdown aversion](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2925462)


