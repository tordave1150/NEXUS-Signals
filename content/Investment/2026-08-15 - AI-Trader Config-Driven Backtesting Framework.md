---
title: AI-Trader Config-Driven Backtesting Framework
note_type: source
primary_topic: Investment
secondary_topics: [Backtesting, Research Automation]
concepts: [Config-Driven Workflow, YAML, Backtrader, MCP Server]
entities: [AI-Trader, Backtrader, whchien]
tags: [backtesting, yaml, mcp]
source_type: Facebook Post and GitHub Repository
source_title: AI-Trader
source_author: Thongchai and whchien
source_url: "https://www.facebook.com/chaivsai/posts/pfbid021RjfmPCy7Jzp9uae4XpkTsQR38vpgMFyFqhBaHNNEHjAuCPZPM6JQaWFFULcHsRWl?__tn__=%2CO*F"
canonical_url: "https://www.facebook.com/chaivsai/posts/pfbid021RjfmPCy7Jzp9uae4XpkTsQR38vpgMFyFqhBaHNNEHjAuCPZPM6JQaWFFULcHsRWl"
source_date: 2026-08-15
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: verified
confidence: High
related: ["[[Reproducible Backtesting]]", "[[Agentic Trading Research]]"]
---

# AI-Trader Config-Driven Backtesting Framework

## Verified Features

AI-Trader เป็น framework บน Backtrader ที่กำหนด backtest ด้วย YAML ซึ่งเก็บ version control ได้ มี CLI สำหรับรัน test และดึงข้อมูล รองรับหุ้นสหรัฐ/ไต้หวัน คริปโต และ forex มี strategy มากกว่า 20 แบบ รวมถึง MCP server ให้ผู้ช่วย AI เรียก backtest, fetch data และวิเคราะห์ผล

## Caveats

ความทำซ้ำได้ของ config ไม่ได้ทำให้ผลถูกต้องโดยอัตโนมัติ ยังต้องตรวจ data version, corporate actions, timestamp, commission, spread, slippage, market impact และ parameter search การเชื่อม LLM ควรมี approval boundary และ audit log; repository เป็น GPL-3.0 จึงต้องตรวจเงื่อนไขเมื่อดัดแปลงหรือเผยแพร่ต่อ

## Sources

- [Original Facebook post](https://www.facebook.com/chaivsai/posts/pfbid021RjfmPCy7Jzp9uae4XpkTsQR38vpgMFyFqhBaHNNEHjAuCPZPM6JQaWFFULcHsRWl?__tn__=%2CO*F)
- [AI-Trader repository](https://github.com/whchien/ai-trader)




