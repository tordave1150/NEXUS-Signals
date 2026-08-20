---
title: Two-Factor Scenario Heatmaps
note_type: source
primary_topic: Investment
secondary_topics: [Quantitative Research, Feature Engineering]
concepts: [Conditional Returns, Quantile Binning, Interaction Effects]
entities: [Investic Academy]
tags: [scenario-analysis, heatmap, forward-returns]
source_type: Facebook Post
source_title: Scenario Heatmap
source_author: Investic Academy
source_url: "https://www.facebook.com/investic.academy/posts/pfbid02WAAzYf4uGAQT2osRwmohT5djZwzfo86FHaGrnPrGttiuoceFRTk55pRNLzY5tvQxl?__cft__[0]=AZYox6ps1Ptnc75MgpH31AyjieLa2ThUtMrIPcrw8xoldiKKFNHb7hed4kfeK7vegn_70YwobeJgLlaLdfyfaoOs-0_kTDLtz2caQSoDA5YOXOQqanoqudJLrOTCuN9NwKTDk84plmH6A9U-g7CCoWl4Ln8h0zRffAi1NWDbusM-kg&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/investic.academy/posts/pfbid02WAAzYf4uGAQT2osRwmohT5djZwzfo86FHaGrnPrGttiuoceFRTk55pRNLzY5tvQxl"
source_date: 2026-08-05
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: summarized
confidence: Medium
related: ["[[Conditional Return Analysis]]", "[[Feature Interaction]]"]
---

# Two-Factor Scenario Heatmaps

## Method

Scenario Heatmap แบ่งตัวแปรสองตัว เช่น momentum, funding หรือ real yield เป็น quantile แล้วคำนวณค่าเฉลี่ยหรือมัธยฐานของ forward return ในแต่ละช่องหลาย horizon เช่น 1, 4, 8 และ 24 ชั่วโมง วิธีนี้ช่วยเห็นปฏิสัมพันธ์แบบไม่เชิงเส้นซึ่ง correlation หรือ regression ตัวแปรเดียวอาจซ่อนไว้

## Caveats

แต่ละช่องต้องรายงานจำนวนตัวอย่างและความไม่แน่นอนด้วย เพราะการแบ่งหลาย bin และหลาย horizon เพิ่ม multiple testing ขณะที่ forward window ที่ทับซ้อนกันทำให้ observation ไม่เป็นอิสระ รูปแบบที่เห็นควรยืนยันด้วยช่วงเวลา out-of-sample และทดสอบความเสถียรข้าม regime ก่อนใช้เป็น signal

## Sources

- [Original Facebook post](https://www.facebook.com/investic.academy/posts/pfbid02WAAzYf4uGAQT2osRwmohT5djZwzfo86FHaGrnPrGttiuoceFRTk55pRNLzY5tvQxl?__cft__[0]=AZYox6ps1Ptnc75MgpH31AyjieLa2ThUtMrIPcrw8xoldiKKFNHb7hed4kfeK7vegn_70YwobeJgLlaLdfyfaoOs-0_kTDLtz2caQSoDA5YOXOQqanoqudJLrOTCuN9NwKTDk84plmH6A9U-g7CCoWl4Ln8h0zRffAi1NWDbusM-kg&__tn__=%2CO%2CP-R)




