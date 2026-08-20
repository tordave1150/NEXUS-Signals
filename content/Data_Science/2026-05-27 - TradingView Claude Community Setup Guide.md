---
title: TradingView Claude Community Setup Guide
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Developer Tools]
concepts: [Model Context Protocol, Chrome DevTools Protocol, TradingView Automation]
entities: [Claude Desktop, Claude Code, TradingView, PyPI]
tags: [tradingview, mcp, cdp, community-guide]
source_type: Google Doc
source_title: TradingView_Claude_Setup_Guide.md
source_author: Community Guide
source_url: "https://docs.google.com/document/d/1Ton1CjIM7-oO0JzcF9hNeHtFsPRlU24MYEYZCkq6BG8/edit?tab=t.0"
canonical_url: "https://docs.google.com/document/d/1Ton1CjIM7-oO0JzcF9hNeHtFsPRlU24MYEYZCkq6BG8/edit"
source_date: 2026-05-27
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: Medium
related: ["[[Model Context Protocol]]", "[[Chrome DevTools Protocol]]"]
---

# TradingView Claude Community Setup Guide

> [!summary] TL;DR
> คู่มือ Windows 11 แยกสองเส้นทาง: (1) `tradingview-mcp-server` สำหรับ market data, screening และ backtest และ (2) `tradesdontlie/tradingview-mcp` ผ่าน CDP เพื่อควบคุม chart, Pine Script, watchlist และ drawing ใน session TradingView จริง

## Workflow

- ติดตั้ง `uv`, Python tool และตั้ง Claude Desktop MCP config สำหรับเส้นทางข้อมูล
- ติดตั้ง Node/Git, clone repository, เพิ่ม MCP ให้ Claude Code และเปิด TradingView/Chrome ด้วย remote-debugging port สำหรับเส้นทาง CDP
- มีตัวอย่าง prompts และ troubleshooting เรื่อง PATH, config, restart และ connection status

## Critical Reconciliation

อ่าน Google Doc เต็ม 1 tab แล้ว PyPI ยืนยัน package/คำสั่งติดตั้งโดยหลัก และ GitHub ยืนยันว่า CDP project เป็น automation อิสระ ไม่ได้ได้รับรองโดย TradingView แต่คู่มือมีคำสั่งซ้ำและ paths/versions ที่อาจล้าสมัย ควรตรวจ README/release ปัจจุบัน, pin version, หลีกเลี่ยง expose port 9222, เก็บ secrets นอก config ที่แชร์ และทดสอบใน profile แยกก่อนใช้งานจริง

## Sources

- [Original Google Doc](https://docs.google.com/document/d/1Ton1CjIM7-oO0JzcF9hNeHtFsPRlU24MYEYZCkq6BG8/edit?tab=t.0)
- [tradingview-mcp-server on PyPI](https://pypi.org/project/tradingview-mcp-server/)
- [tradesdontlie/tradingview-mcp](https://github.com/tradesdontlie/tradingview-mcp)
