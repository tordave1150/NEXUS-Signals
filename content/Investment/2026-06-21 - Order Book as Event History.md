---
title: Order Book as Event History
note_type: source
primary_topic: Investment
secondary_topics: [Market Microstructure, Algorithmic Trading]
concepts: [Limit Order Book, Order Flow, Markov State]
entities: [PopQuants]
tags: [order-book, order-flow, scalping]
source_type: Facebook Post
source_title: Order book is a short clip, not only a snapshot
source_author: PopQuants
source_url: "https://www.facebook.com/popquants/posts/pfbid02cNTVrVaVnzp3hWoncsRtnpZnay8mUd82D8csEnttAwUneBXbKAz7cBQomXz67t4yl?__cft__[0]=AZY34y62OI1LLxbLyZ3IZEwIYxuH_gb8mOsqKKxgKYZpuvbKpDFesTITVRBJ-fkROOp9xo160-YHr7Y01FHapBZYgGQbshUuLQHHAmU0PhcOqiRf2rL7cwDnvN_fFsh154T5E4qh8igmUuOSnObHoyzXUbDnqZl1IMxvFg05RQqJ1Q&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02cNTVrVaVnzp3hWoncsRtnpZnay8mUd82D8csEnttAwUneBXbKAz7cBQomXz67t4yl"
source_date: 2026-06-21
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: summarized
confidence: Medium
related: ["[[Limit Order Book]]", "[[Order Flow]]"]
---

# Order Book as Event History

## Central Idea

Bid size 300 และ ask size 300 ที่ snapshot เดียวกันอาจมีความหมายต่างกัน เพราะเส้นทางก่อนมาถึงสถานะนั้นอาจประกอบด้วยการเติมคำสั่ง การยกเลิก และการถูก execute คนละแบบ จึงควรมอง order book เป็นลำดับเหตุการณ์สั้น ๆ ไม่ใช่ภาพนิ่งเพียงเฟรมเดียว

## Implications

- เพิ่ม features จาก order arrivals, cancellations, fills, queue depletion และ replenishment
- แยก state variables ออกจาก transition/event intensities
- ทดสอบว่าประวัติเพิ่ม predictive information เหนือ top-of-book/depth snapshot หรือไม่
- Markov model มีประโยชน์เมื่อ state definition เก็บข้อมูลที่จำเป็นพอ แต่สมมติฐาน memoryless ต้องตรวจจากข้อมูล

## Verification Limitation

โพสต์กล่าวถึง paper แต่ไม่ให้ชื่อ DOI หรือลิงก์ และระบุว่าจะอธิบายในคอร์ส จึงตรวจงานต้นฉบับและข้อกำหนดของโมเดลไม่ได้ แนวคิดทั่วไปสอดคล้องกับ market microstructure แต่ยังไม่ใช่หลักฐานว่าทำ scalping ได้กำไรหลัง latency, queue priority, fees และ adverse selection

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02cNTVrVaVnzp3hWoncsRtnpZnay8mUd82D8csEnttAwUneBXbKAz7cBQomXz67t4yl?__cft__[0]=AZY34y62OI1LLxbLyZ3IZEwIYxuH_gb8mOsqKKxgKYZpuvbKpDFesTITVRBJ-fkROOp9xo160-YHr7Y01FHapBZYgGQbshUuLQHHAmU0PhcOqiRf2rL7cwDnvN_fFsh154T5E4qh8igmUuOSnObHoyzXUbDnqZl1IMxvFg05RQqJ1Q&__tn__=%2CO%2CP-R)


