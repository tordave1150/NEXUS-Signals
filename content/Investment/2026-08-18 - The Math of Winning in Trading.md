---
title: The Math of Winning in Trading
note_type: source
primary_topic: Investment
secondary_topics: [Risk Management, Trading Systems]
concepts: [Expectancy, Win Rate, Payoff Ratio, Drawdown]
entities: [Mulham Trading]
tags: [trading-math, expectancy, youtube]
source_type: YouTube Video
source_title: The Math of Winning in Trading
source_author: Mulham Trading
source_url: "https://www.youtube.com/watch?v=BAfRVpKIxZ4"
canonical_url: "https://www.youtube.com/watch?v=BAfRVpKIxZ4"
source_date:
captured_at: 2026-08-18
created: 2026-08-18
updated: 2026-08-18
status: verified
confidence: Medium
related: ["[[Risk Management]]", "[[Position Sizing]]"]
---

# The Math of Winning in Trading

## Core Model

ระบบเทรดตัดสินด้วยผลรวมของ win rate, average win, average loss และต้นทุน ไม่ใช่ตัวเลขใดตัวเลขหนึ่ง:

`Expectancy (R/trade) = p × W − (1 − p) × L − C`

- `p` = win rate
- `W` = average win หน่วย R
- `L` = average loss หน่วย R
- `C` = commissions + spread + slippage หน่วย R

จุดคุ้มทุนคือ `p_BE = (L + C) / (W + L)` ระบบ win rate ต่ำยังมีกำไรได้ถ้า payoff สูงพอ และระบบ win rate สูงก็ขาดทุนได้ถ้าขาดทุนเฉลี่ย/ต้นทุนใหญ่เกินไป

## Risk and Survival

Positive expectancy ไม่มีความหมายถ้าขนาดสถานะทำให้พอร์ตอยู่ไม่ถึง sample ระยะยาว หากเสี่ยงสัดส่วน `f` ของ equity ต่อครั้ง การขาดทุนติดกัน `n` ครั้งทำให้ drawdown โดยประมาณเป็น:

`Drawdown = 1 − (1 − f)^n`

ดังนั้น position sizing ต้องออกแบบจาก losing streak ที่รับได้ ไม่ใช่จากกำไรที่อยากได้

## 🔎 In-depth Details

ใช้ rolling expectancy แยกตาม regime และรายงานทั้ง distribution ไม่ใช่ค่าเฉลี่ยเดียว เพิ่ม confidence interval, max drawdown, time under water และผลหลังหักต้นทุน จากนั้น validate ด้วยข้อมูลเดินหน้าและ paper/small-live stage

การลองหลายพารามิเตอร์แล้วเลือกเส้น equity ที่สวยที่สุดทำให้ expectancy บนกระดาษสูงเกินจริง งานเรื่อง Probability of Backtest Overfitting เสนอให้วัดความเสี่ยงจาก model selection โดยตรง แทนการเชื่อ hold-out ชุดเดียว

## Sources

- [Original YouTube video](https://www.youtube.com/watch?v=BAfRVpKIxZ4)
- [The Probability of Backtest Overfitting](https://escholarship.org/uc/item/4w1110bb)
- [Alpaca paper trading limitations](https://docs.alpaca.markets/docs/paper-trading)

