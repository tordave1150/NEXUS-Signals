---
title: Claude Trading Skills
note_type: source
primary_topic: Investment
secondary_topics: [Agent Skills, Screening, Portfolio Management]
concepts: [Market Regime, Stock Screening, Exposure, Human Decision Gate]
entities: [TraderMonty, Claude Code, FMP, Finviz, Alpaca]
tags: [agent-skills, equity-research, github]
source_type: Attached Screenshot, GitHub Repository and Documentation
source_title: Claude Trading Skills
source_author: TraderMonty
source_url: "https://github.com/tradermonty/claude-trading-skills"
canonical_url: "https://github.com/tradermonty/claude-trading-skills"
source_date:
captured_at: 2026-08-18
created: 2026-08-18
updated: 2026-08-18
status: verified
confidence: High
related: ["[[Trading Automation]]", "[[Investment Research Workflow]]"]
---

# Claude Trading Skills

## เลือกใช้แบบเร็ว

- **เริ่มง่าย:** Finviz Screener ใช้สร้าง/เปิด screener URL และ Market Breadth Analyzer ใช้ public CSV ได้
- **หุ้นปันผล:** Value Dividend Screener + Kanchi Dividend SOP
- **หุ้นเติบโต:** CANSLIM Stock Screener + VCP Screener
- **คุมจังหวะและขนาดพอร์ต:** Exposure Coach สรุป market posture และเพดาน net exposure จากสัญญาณต้นน้ำ
- **มีพอร์ต Alpaca:** Portfolio Manager วิเคราะห์ holdings, cash และความเสี่ยงพอร์ต

## API ที่ต้องใช้จริง

| Skill | Requirement |
|---|---|
| Finviz Screener | Finviz optional |
| Market Breadth Analyzer | public CSV; ไม่ต้องมี API ใน basic path |
| Value Dividend Screener | FMP required |
| Kanchi Dividend SOP | FMP recommended |
| CANSLIM / VCP Screener | FMP required |
| Exposure Coach | local calculation แต่ต้องมี regime/breadth inputs |
| Portfolio Manager | Alpaca required |

FMP Basic ยืนยัน 250 calls/วันและข้อมูล end-of-day บางชุด จึงพอสำหรับทดลองและงานเบา แต่ต้องเช็กว่า endpoint/ประวัติข้อมูลที่ skill ใช้อยู่ใน free tier จริง ส่วน FINVIZ Elite เป็นทางเลือกเมื่อ workflow ต้องการข้อมูลหรือความเร็วเพิ่ม ไม่ใช่เงื่อนไขของเส้นทางเริ่มต้นทั้งหมด

## 🔎 In-depth Details

ลำดับที่ลดความผิดพลาดได้ดีกว่าการ “เปิด screener แล้วซื้อ” คือ:

**Regime/Breadth → Exposure ceiling → Candidate screen → Fundamental/technical validation → Position sizing → Pre-trade checklist → Post-trade review**

Exposure Coach ไม่ควรถูกตีความว่าให้เปอร์เซ็นต์ลงทุนได้จากศูนย์ มันรวมสัญญาณ market regime, breadth และ growth-vs-value bias เพื่อสร้างกรอบว่าเปิดสถานะใหม่ได้หรือควรเน้นเงินสด ขณะที่การตัดสินใจและการส่งคำสั่งยังต้องเป็น human gate ตามเจตนาของ repository

โพสต์ “Finance Agent Skills” เดิมอ้างชุดราคา/ข่าว/options/งบ/TradingView แต่ไม่มี repository ให้ยืนยัน จึงไม่เก็บเป็นเครื่องมือแยก รายการดังกล่าวถูกรวมเป็นข้อกำหนดตรวจสอบ: ทุก skill ต้องแสดง provider, entitlement, timestamp/timezone, adjusted-vs-unadjusted price, error handling และ data freshness; คำว่า real-time ห้ามใช้โดยไม่มี latency/venue coverage ที่ระบุได้

## Sources

- Attached screenshot: [[Assets/Claude Trading Skills README.png]]
- [Official repository](https://github.com/tradermonty/claude-trading-skills)
- [Documentation](https://tradermonty.github.io/claude-trading-skills/)
- [FMP pricing](https://site.financialmodelingprep.com/pricing-plans)
- [Merged Facebook post — unverified Finance Agent Skills](https://www.facebook.com/popquants/posts/pfbid02z7cf3fcnmPKFqK7RGLFn9d3RocKUYVZUovhDgAibfANbRhNdam2xD2PxtQYXUPvPl)
