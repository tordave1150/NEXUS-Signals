---
title: Dumb Display Smart Server ESP32 Calendar
note_type: source
primary_topic: Data_Science
secondary_topics: [Embedded Systems, AI Coding]
concepts: [Thin Client, Server-Side Rendering, E-Paper]
entities: [ESP32, Waveshare, Claude Code, Google Calendar]
tags: [esp32, e-paper, thin-client]
source_type: Facebook Post
source_title: ESP32 desk calendar built with Claude Code
source_author: Teepagorn Champ Wuttipitayamongkol
source_url: "https://www.facebook.com/teepagorn/posts/pfbid02o7wNHXMqrQkqcTWqdkpQ74GesXLBYP5AKp9jfsaAuvZRwUwARisr8yddjNbKUmyJl?__tn__=%2CO*F"
canonical_url: "https://www.facebook.com/teepagorn/posts/pfbid02o7wNHXMqrQkqcTWqdkpQ74GesXLBYP5AKp9jfsaAuvZRwUwARisr8yddjNbKUmyJl"
source_date: 2026-06-26
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: summarized
confidence: Medium
related: ["[[Thin Client]]", "[[Embedded Systems]]"]
---

# Dumb Display Smart Server ESP32 Calendar

## Architecture

โปรเจกต์ใช้หลัก “จอโง่ เซิร์ฟเวอร์ฉลาด”: Mac ดึง Google Calendars หลายบัญชี จัด layout และ render เป็นภาพขาวดำ 400×300 จากนั้น ESP32/Waveshare display เพียงดาวน์โหลดภาพและแสดงผล พร้อมปุ่มสลับหน้า

## Useful Engineering Lessons

- ย้าย OAuth, JSON parsing และ layout ออกจาก microcontroller ไปยังเครื่องที่จัดการง่ายกว่า
- แก้ shaping ภาษาไทยด้วย headless Chrome แทน image renderer ที่จัดวรรณยุกต์ผิด
- ใช้ Python ฝั่ง server และ C++ firmware ฝั่งบอร์ด โดย AI ช่วยเขียนและ debug แบบสนทนา
- เลือก font/readability ตามข้อจำกัดจอจริง ไม่ยึด aesthetic ใน mockup

## Caveat

AI ช่วยลดกำแพงทักษะแต่ยังต้องมีผู้ใช้กำหนด architecture, อ่าน logs และทดสอบ hardware ควรป้องกัน calendar tokens, จำกัด endpoint รูปภาพ, ใช้ TLS/authentication และออกแบบ offline/error state ก่อนใช้กับข้อมูลส่วนตัว

## Sources

- [Original Facebook post](https://www.facebook.com/teepagorn/posts/pfbid02o7wNHXMqrQkqcTWqdkpQ74GesXLBYP5AKp9jfsaAuvZRwUwARisr8yddjNbKUmyJl?__tn__=%2CO*F)


