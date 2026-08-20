---
title: MCP Stack สำหรับ Web Research และ Automation
note_type: source
primary_topic: Data_Science
secondary_topics: [Software Engineering, Artificial Intelligence]
concepts: [Model Context Protocol, Browser Automation, Web Scraping, Developer Tools]
entities: [Perplexity, Playwright, Firecrawl, Glif, Chrome DevTools]
tags: [mcp, browser-automation, web-research]
source_type: Facebook Post
source_title: 5 MCP ที่ควรมีสำหรับ Claude Code
source_author: Thongchai Thampueak
source_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-070__"
canonical_url: "https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPlURL-070__"
source_date: 2026-05-11
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: High
related: ["[[Model Context Protocol]]", "[[Browser Automation]]"]
---

# MCP Stack สำหรับ Web Research และ Automation

> [!summary] TL;DR
> โพสต์เสนอ MCP servers ห้ากลุ่มสำหรับ live research, browser control, scraping, media generation และ web debugging ทำให้ agent เชื่อมข้อมูลและลงมือกับระบบภายนอกได้

## Capability Map

- Perplexity: web search/research
- Playwright: browser navigation และ UI automation
- Firecrawl: extraction/crawling เป็นข้อมูลโครงสร้าง
- Glif: media-generation workflows
- Chrome DevTools: DOM, network, console และ performance inspection

## Reconciliation

MCP เป็นมาตรฐานการเชื่อม tools/data ไม่ใช่การรับรองว่า server ทุกตัวปลอดภัยหรือจำเป็นต้องติดตั้งทั้งหมด ความสามารถจริงขึ้นกับ client, authentication, tool schema และ permission โพสต์เรียกว่า “ของต้องมี” แต่หลักที่ปลอดภัยกว่าคือเปิดเฉพาะ tools ที่งานต้องใช้ ตรวจ publisher และระวัง prompt injection, credential exposure และ destructive actions

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl?__cft__[0]=AZa3CMOIR24ySechTPTYRKMkCTJur37OHPqtvmZSJNoTxwKa-TRomccBPCRHAlWxQa0ozz1GAiTU-BIXH0Gp7mktjmMCzAM50vM7WVL60lt4zKKRDd9dEOiJhleFL9YOIJhqaWCZNaulEavmrsFgETPiVjHJ5lkbeyyEd7EVGLGaIg&__tn__=%2CO%2CP-RURL-070__)
- [Anthropic — Introducing Model Context Protocol](https://www.anthropic.com/news/model-context-protocol)
- [Anthropic — Security and privacy for custom connectors](https://support.anthropic.com/en/articles/11175166-about-custom-integrations-using-remote-mcp)


