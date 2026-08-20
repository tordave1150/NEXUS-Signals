---
title: Claude Code สำหรับ Financial Modeling และ Valuation
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Artificial Intelligence]
concepts: [Financial Modeling, Valuation, AI Workflow]
entities: [Kanis Saengchote, Anthropic]
tags: [financial-modeling, valuation, ai]
source_type: Facebook Post
source_title: Claude Code for Investment
source_author: Seminar knowledge by Amorn
source_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid0WXMuiS2SdtokAbkd3f7qZTsyZWbjvqNVCFdkTjs4wthoCr7iQisWnYJMGLfpwPGhl&id=100049294731654&__cft__[0]=AZa86vNw0SyroPQ0Ad74Uglt0wEj4a3aiPB5PiI4qgcQdi8nVuelw7D2NEnkL01J3Krkl_ByEHJ4I0UB_cpaQ0UD6j7uu5WlHGvzJfwFeuZPe0IpTqtvTUz71L2nOkw9Brq2qnYnrQf_SbKlc9a9PStyK5Q1VM2NtLlSbDV4elKWAw&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/permalink.php?story_fbid=pfbid0WXMuiS2SdtokAbkd3f7qZTsyZWbjvqNVCFdkTjs4wthoCr7iQisWnYJMGLfpwPGhl&id=100049294731654"
source_date: 2026-03-28
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: Medium
related: ["[[Financial Modeling]]", "[[AI Workflow]]"]
---

# Claude Code สำหรับ Financial Modeling และ Valuation

> [!summary] TL;DR
> AI ควรทำหน้าที่ประกอบ pipeline, model และเอกสารภายใต้ assumptions ที่มนุษย์กำหนด พร้อม plan/review/checks—not เป็นแหล่งสมมติฐานลงทุนอัตโนมัติ

## Key Takeaways

- เตรียมข้อมูลเป็น Markdown/CSV พร้อม provenance ก่อนประมวลผล
- ใช้ plan ก่อนรันงานยาวและเปิดเฉพาะ skills/plugins ที่จำเป็น
- 3-statement/DCF models ต้องมี balance checks และ trace-back
- แบ่ง agents เป็น data, analysis, report และ QA ได้ แต่ต้องกำหนด interfaces

## Verification & Reconciliation

ข้อเสนอเรื่องให้มนุษย์รับผิดชอบ assumptions สอดคล้องกับ model governance ที่ดี แต่คำกล่าวว่าภาษาไทยใช้ token “มากกว่าอย่างมีนัยสำคัญ” และการเปิด plugins แย่ง context ขึ้นกับ tokenizer/product/version ควรตรวจเอกสารปัจจุบันก่อนเหมารวม

## Sources

- [Original Facebook post](https://www.facebook.com/permalink.php?story_fbid=pfbid0WXMuiS2SdtokAbkd3f7qZTsyZWbjvqNVCFdkTjs4wthoCr7iQisWnYJMGLfpwPGhl&id=100049294731654&__cft__[0]=AZa86vNw0SyroPQ0Ad74Uglt0wEj4a3aiPB5PiI4qgcQdi8nVuelw7D2NEnkL01J3Krkl_ByEHJ4I0UB_cpaQ0UD6j7uu5WlHGvzJfwFeuZPe0IpTqtvTUz71L2nOkw9Brq2qnYnrQf_SbKlc9a9PStyK5Q1VM2NtLlSbDV4elKWAw&__tn__=%2CO%2CP-R)
