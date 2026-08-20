---
title: Kronos Financial Market Foundation Model
note_type: source
primary_topic: Investment
secondary_topics: [Machine Learning, Time Series]
concepts: [Financial Tokenization, OHLCVA, Autoregressive Forecasting, Foundation Model]
entities: [Kronos, Yu Shi]
tags: [foundation-model, forecasting, ohlcv]
source_type: Facebook Post, Research Paper and GitHub Repository
source_title: Kronos A Foundation Model for the Language of Financial Markets
source_author: Investic Academy and Kronos authors
source_url: "https://www.facebook.com/investic.academy/posts/pfbid0Q4YyvsmvUT42PixatvXAU85ocUjHPu26FKgUxPGoGGmJ92nYAMGoNPaHtq282pgJl?__cft__[0]=AZaGQonoZTfE1qKAp157BSiuZ88i-ZY4kr8x-JGC1SdSSm-g8Jn-byLHzW7AY_GGIjIy2CM-DBXo4Xz_BcDs8ch5EEhu-b9NoQ1r0DMd7-fwha2znzOtySlkt3yDsAl9kZkKBI-8wYT565KZPDzQyQUO1T7xBOuozDsWqW79793p1A&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/investic.academy/posts/pfbid0Q4YyvsmvUT42PixatvXAU85ocUjHPu26FKgUxPGoGGmJ92nYAMGoNPaHtq282pgJl"
source_date: 2026-08-13
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: verified
confidence: High
related: ["[[Financial Time-Series Models]]", "[[Feature Generation]]"]
---

# Kronos Financial Market Foundation Model

## Finding

Kronos แปลงข้อมูล OHLCVA ต่อเนื่องเป็น token สองระดับ—coarse สำหรับโครงสร้างหลักและ fine สำหรับรายละเอียดคงเหลือ—แล้วใช้ decoder-only Transformer พยากรณ์ลำดับสถานะตลาด repository มีโมเดลและตัวอย่าง fine-tuning/backtest บน Qlib พร้อมระบุว่า demo ไม่ใช่ระบบ production

## Practical Use

เหมาะประเมินเป็น feature generator หรือ scenario model มากกว่าตีความเป็นเครื่องทำนายทิศทางสำเร็จรูป ต้องทดสอบหลัง cutoff ของ pretraining, ใช้ normalization แบบ causal, แยก train/validation/test ตามเวลา และรวมต้นทุน slippage/impact; issue สาธารณะของโครงการยังมีข้อสังเกตเรื่อง leakage และผล cross-sectional หลังต้นทุน จึงควรตรวจ code/version ที่ใช้งานจริง

## Sources

- [Original Facebook post](https://www.facebook.com/investic.academy/posts/pfbid0Q4YyvsmvUT42PixatvXAU85ocUjHPu26FKgUxPGoGGmJ92nYAMGoNPaHtq282pgJl?__cft__[0]=AZaGQonoZTfE1qKAp157BSiuZ88i-ZY4kr8x-JGC1SdSSm-g8Jn-byLHzW7AY_GGIjIy2CM-DBXo4Xz_BcDs8ch5EEhu-b9NoQ1r0DMd7-fwha2znzOtySlkt3yDsAl9kZkKBI-8wYT565KZPDzQyQUO1T7xBOuozDsWqW79793p1A&__tn__=%2CO%2CP-R)
- [Kronos paper](https://arxiv.org/abs/2508.02739)
- [Kronos repository](https://github.com/shiyu-coder/Kronos)




