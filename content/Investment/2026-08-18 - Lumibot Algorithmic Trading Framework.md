---
title: Lumibot Algorithmic Trading Framework
note_type: source
primary_topic: Investment
secondary_topics: [Algorithmic Trading, AI Agents]
concepts: [Backtesting, Paper Trading, Hybrid Agents, Risk Gates]
entities: [Lumiwealth, Lumibot, Alpaca]
tags: [lumibot, algorithmic-trading, github]
source_type: GitHub Repository and Official Documentation
source_title: Lumibot
source_author: Lumiwealth
source_url: "https://github.com/Lumiwealth/lumibot"
canonical_url: "https://github.com/Lumiwealth/lumibot"
source_date:
captured_at: 2026-08-18
created: 2026-08-18
updated: 2026-08-18
status: verified
confidence: High
related: ["[[Trading Automation]]", "[[AI Trading Agent]]"]
---

# Lumibot Algorithmic Trading Framework

## Summary

Lumibot เป็น Python framework สำหรับสร้างกลยุทธ์ deterministic, AI-agent และ hybrid แล้วใช้ lifecycle เดียวกันกับ historical backtest, paper trading และ live broker เช่น Alpaca จุดแข็งคือไม่ต้องเขียนระบบใหม่เมื่อย้ายขั้น แต่ผลแต่ละขั้นยังไม่เทียบเท่ากันโดยอัตโนมัติ

เหมาะเมื่ออยากให้ Python รับผิดชอบ schedule, indicators, position sizing และ hard risk limits ขณะที่ agent ใช้อ่านข่าว, filings, macro, technicals และ account state เพื่อเสนอเหตุผลหรือคำสั่งภายใต้กรอบที่ตรวจสอบได้

## Recommended Architecture

1. **Research agents — read only:** เก็บหลักฐานและเสนอ thesis
2. **Deterministic gates:** ตรวจ universe, max position, max loss, stale data และ market hours
3. **Trader agent — permission แคบ:** มีเพียงตัวสุดท้ายที่เสนอ/ส่งคำสั่งได้
4. **Paper stage:** ทดสอบ event loop, credentials, order state และ failure recovery
5. **Small-live stage:** เริ่มทุนต่ำและมี kill switch ก่อนเพิ่มขนาด

## 🔎 In-depth Details

การ replay agent run ช่วยให้ debug และลดความแปรปรวนจาก LLM แต่ไม่ได้แก้ data leakage หรือ regime shift ควรเก็บ prompt/model/tool versions และ point-in-time inputs ไว้กับผล backtest

Alpaca ระบุว่า paper trading ไม่จำลอง market impact, information leakage, latency slippage, queue position, price improvement, regulatory fees และ dividends ครบ ดังนั้น paper pass หมายถึง “ระบบทำงานตามกลไก” ไม่ใช่ “ผลตอบแทน live ถูกพิสูจน์แล้ว”

## Sources

- [Official GitHub repository](https://github.com/Lumiwealth/lumibot)
- [Lumibot documentation](https://lumibot.lumiwealth.com/)
- [Lumibot getting started](https://lumibot.lumiwealth.com/getting_started.html)
- [Alpaca paper trading limitations](https://docs.alpaca.markets/docs/paper-trading)

