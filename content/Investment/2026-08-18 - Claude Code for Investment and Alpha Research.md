---
title: Claude Code for Investment and Alpha Research
note_type: source
primary_topic: Investment
secondary_topics: [Claude Code, Quantitative Research]
concepts: [Alpha Research, Context Engineering, Backtesting, Research Automation, Reverse DCF, Agent Teams]
entities: [นัทเล่าเรื่อง, คณิสร์ แสงโชติ, สิทธิ์ อยู่โปร่ง, โกเมธ จันทวิมล, WorldQuant BRAIN]
tags: [claude-code, alpha-research, youtube]
source_type: YouTube Playlist
source_title: Claude Code for Investment & Portfolio Management
source_author: นัทเล่าเรื่อง
source_url: "https://www.youtube.com/playlist?list=PLWYjdCridVWKG2q152C-J24lIAm7SngcC"
canonical_url: "https://www.youtube.com/playlist?list=PLWYjdCridVWKG2q152C-J24lIAm7SngcC"
source_date:
captured_at: 2026-08-18
created: 2026-08-18
updated: 2026-08-18
status: reconciled
confidence: Medium-High
related: ["[[Systematic Research Workflow]]", "[[AI Trading Agent]]"]
---

# Claude Code for Investment and Alpha Research

## Playlist Map

1. [Claude Code Automate for Investing](https://www.youtube.com/watch?v=5sPkuV4aTSU) — ผศ.ดร.คณิสร์ แสงโชติ: financial modeling, DCF และ workflow สำหรับวิเคราะห์หุ้น
2. [Claude Code for Alpha Research](https://www.youtube.com/watch?v=AJDpQMGgKok) — สิทธิ์ อยู่โปร่ง: สร้างและทดสอบสมมติฐาน alpha บน WorldQuant BRAIN
3. [Cloude code 1o1](https://www.youtube.com/watch?v=h9s5KFEGbcs) — ดร.โกเมธ จันทวิมล: จาก assistant ไปสู่ workflow และระบบหลาย agent

ตอน Alpha Research มี transcript ที่เข้าถึงได้โดยตรง ส่วนรายละเอียดของตอน 1 และ 3 ด้านล่างมาจากสรุป transcript ที่ผู้ใช้สร้างผ่าน NotebookLM จึงเก็บ timestamp และลดระดับความมั่นใจของคำกล่าวอ้างที่ยังทำซ้ำไม่ได้

## Reconciled Summary

- coding agent มีคุณค่าสูงสุดเมื่อทำหน้าที่ **orchestrator** ของงานที่มีไฟล์ ข้อมูล กฎ และจุดตรวจสอบชัดเจน ไม่ใช่ผู้ตัดสินใจลงทุนอัตโนมัติ
- งาน valuation ควรให้ agent สร้างและตรวจโมเดล แต่ให้มนุษย์รับผิดชอบสมมติฐานสำคัญ เช่น growth, margin, WACC และ terminal value
- งาน alpha research ควรแยก **idea generation** ออกจาก **backtest validation** และเก็บทุก trial เพื่อวัด data-mining risk
- งานหลาย agent จะคุ้มเมื่อแบ่งงานเป็นอิสระได้และมีหัวหน้ารวมผล พร้อม shared state, audit trail และเกณฑ์รับงานเดียวกัน
- Markdown/CSV เหมาะกับ workflow ที่ต้อง diff, parse และตรวจย้อนกลับ แต่ไม่ได้แปลว่าแม่นยำกว่า PDF/Excel ในทุกกรณี โดยเฉพาะตารางหรือสูตรที่สูญเสียโครงสร้างระหว่างแปลงไฟล์

## Transcript Reconciliation

### Video 1 — Automate for Investing

- **[00:08:20–00:10:45]** skill ใช้ `SKILL.md` และไฟล์อ้างอิงเพื่อบรรจุวิธีทำงาน แต่การเปิดใช้สิ่งที่ไม่เกี่ยวข้องมากเกินไปเพิ่มภาระ context
- **[00:28:15]** Plan Mode ถูกใช้ให้ระบบสำรวจและเสนอแผนก่อนแก้ไฟล์ ซึ่งสอดคล้องกับเอกสาร Claude Code ทางการ
- **[00:33:15–00:37:15]** ตัวอย่าง PLTR ดึง 10-K มาเป็น Markdown สร้าง/ตรวจโมเดลการเงิน และ trace สูตรจำนวนมาก ก่อนให้มนุษย์ตรวจ assumptions
- **[00:39:10]** reverse DCF มีประโยชน์กว่าการเชื่อ target price เดี่ยว เพราะเปลี่ยนคำถามเป็น “ราคาปัจจุบันกำลังสมมติ growth เท่าไร และสมเหตุสมผลหรือไม่”
- **[01:05:00]** ผลสาธิตมูลค่า PLTR ราว **$18 เทียบราคาตลาด $143** เป็น output ของกรณีศึกษา ไม่ใช่หลักฐานว่ามูลค่า $18 ถูกต้องหรือว่า AI ประเมินราคาแม่นยำ
- **[00:52:10]** ผู้พูดเสนอให้ใช้โมเดลเร็ว/ประหยัดกับงาน routine และโมเดล reasoning สูงกับ valuation ที่ซับซ้อน; นี่เป็นแนวทาง routing งาน ไม่ใช่กฎตายตัวของชื่อโมเดลใดรุ่นหนึ่ง

### Video 2 — Alpha Research

- **[00:14:15–00:18:30]** ตัวอย่างเริ่มจาก financial items 120 รายการ สร้างคู่ได้ `120C2 = 7,140` ratios แล้วใช้เกณฑ์เชิงเศรษฐศาสตร์คัดให้เหลือประมาณ 3,000 รายการ
- **[00:26:40–00:31:10]** Claude Code ออกแบบ workflow แล้วเรียกโมเดลภายนอกผ่าน script เพื่อสร้างไอเดีย ก่อนส่ง expression ไป backtest บน WorldQuant BRAIN
- **[00:30:15]** ค่าใช้จ่ายประมาณ **$3.95 สำหรับ 20 ideas** เป็นตัวเลขจากการสาธิตครั้งนั้นเท่านั้น; ทำซ้ำได้ก็ต่อเมื่อรู้ model version, pricing date, prompt และ token usage
- **[00:22:15–00:23:45]** การค้นหา ratios จำนวนมากเพิ่ม multiple-testing/data-mining risk และวิดีโอไม่ได้ให้รายละเอียด transaction costs หรือ slippage เพียงพอสำหรับสรุปว่าพร้อมใช้เงินจริง

### Video 3 — Claude Code 1o1

- **[00:03:50]** กรอบพัฒนาการคือ **Assist → Workflow → System**: จากตอบคำถาม ไปลงมือทำตามขั้นตอน และสุดท้ายประสานหลายบทบาท
- **[00:18:45]** ประวัติการทำงานสามารถสกัดเป็น skill ได้เมื่อแปลง tacit process ให้เป็น instruction, examples และ acceptance criteria ที่ตรวจสอบได้
- **[00:30:10–00:33:45]** ตัวอย่างแบ่งงานให้ 3–5 agents ทำคู่ขนาน มี agent หัวหน้ากระจายงาน และใช้ shared state รวมผล
- วิดีโอเรียกเครื่องมือ monitor ว่า **TMAX** แต่ยังระบุตัวโครงการ/URL ที่แน่ชัดจากหลักฐานที่มีไม่ได้ จึงไม่บันทึกความสามารถเฉพาะของเครื่องมือนี้เป็นข้อเท็จจริง

## Key Ideas for Alpha Research

- **Alpha** คือ excess return หลังแยกผลตอบแทนจาก market/factor exposures ไม่ใช่กำไรดิบของพอร์ต
- วงจรวิจัยคือ **idea → data → expression/model → portfolio → backtest → review**
- ก่อนให้ agent ทำงาน ต้องมีเอกสาร simulator, operators, data fields และข้อจำกัดของ output
- ทุก loop คือการทดลองเพิ่มหนึ่งครั้ง จึงต้องบันทึกทั้งผู้ชนะและผู้แพ้ รวมจำนวน trials ที่ค้นหา
- backtest ต้องแยกเวลาแบบ walk-forward และรวม turnover, fees, spread, slippage และ market impact ที่เหมาะกับกลยุทธ์
- คะแนนหรือการแข่งขันบน simulation platform ไม่ใช่หลักฐานว่ากลยุทธ์พร้อมใช้กับเงินจริง

## 🔎 In-depth Details

โครงที่นำไปใช้ซ้ำได้ควรมี:

1. `research_spec.md` — universe, horizon, hypothesis, benchmark และ forbidden leakage
2. `operators.md` + `data_catalog.md` — ภาษา ข้อมูล lag และ point-in-time availability ที่ agent ใช้ได้
3. constrained generator — สร้างเฉพาะ expression ที่ valid และมี economic rationale
4. experiment registry — เก็บ prompt/model version, parameters และผลของทุก trial
5. walk-forward + cost-aware backtest — แยก train/validation/test ตามเวลาและจำลองต้นทุน
6. independent review — ให้ reviewer ตรวจสูตร data lineage และ assumptions โดยไม่เห็นเฉพาะผลที่ดีที่สุด
7. risk gate — จำกัด exposure และห้าม auto-live จากคะแนน backtest เพียงอย่างเดียว

### Decision-Relevant Insights

- **Reverse DCF เป็นเครื่องมือทดสอบ premise:** ใช้ AI คำนวณ implied growth หลาย scenario แล้วเทียบกับฐานข้อมูลอุตสาหกรรมและข้อจำกัดเชิงเศรษฐศาสตร์ แทนการถามหาราคาเหมาะสมเพียงตัวเดียว
- **Scale ต้องมาพร้อม statistical budget:** การสร้าง 7,140 ratios ไม่ได้สร้างข้อมูลใหม่ แต่เพิ่มจำนวนสมมติฐานที่ทดลอง จึงควรกำหนด holdout, false-discovery control และหยุดค้นก่อนดูผล test set
- **Agent team ไม่ได้ลดความเสี่ยงโดยอัตโนมัติ:** agent หลายตัวอาจทำผิดแบบเดียวกันหากใช้ข้อมูลหรือ prompt ร่วมกัน ต้องแยกหน้าที่ producer/reviewer และใช้ acceptance tests ที่ deterministic เมื่อทำได้
- **ต้นทุนโมเดลเป็นตัวแปรของระบบ:** routing งานไปโมเดลราคาถูกช่วยลดค่าใช้จ่ายได้ แต่ควรวัด cost per accepted output ไม่ใช่ cost per generated idea

### Evidence Boundaries

- การสาธิต terminal, spreadsheet หรือ dashboard แสดงว่า workflow รันได้ในกรณีหนึ่ง แต่ยังไม่เท่ากับ reproducibility หากไม่มี code, data snapshot, prompt และ environment
- ยังไม่มีหลักฐานเพียงพอเรื่อง live execution, slippage, position sizing, secret management และ operational failure recovery
- ชื่อคำสั่ง ปลั๊กอิน ราคาโมเดล และความสามารถของผลิตภัณฑ์เปลี่ยนได้ จึงอ้างอิงเอกสารปัจจุบันก่อนนำไปติดตั้งจริง

### Evidence from earlier prototypes

โพสต์ทดลองที่รวมเข้ามายืนยันประโยชน์ด้าน workflow แต่ไม่ยืนยันผลตอบแทน: ตัวอย่าง factor research รายงาน short-term reversal Sharpe ราว 1.5+ พร้อม turnover สูงและ diversity ต่ำ ส่วนโพสต์ automation อธิบายการป้อน syntax/data rules ให้ LLM สร้าง WorldQuant expressions ทั้งสองไม่มี code, sample, costs และ untouched holdout ให้ทำซ้ำ จึงเก็บเฉพาะบทเรียนเรื่อง experiment design และไม่เก็บค่าผลลัพธ์เป็น benchmark

## Sources

- [Original playlist](https://www.youtube.com/playlist?list=PLWYjdCridVWKG2q152C-J24lIAm7SngcC)
- [Claude Code Automate for Investing](https://www.youtube.com/watch?v=5sPkuV4aTSU)
- [Claude Code for Alpha Research](https://www.youtube.com/watch?v=AJDpQMGgKok)
- [Cloude code 1o1](https://www.youtube.com/watch?v=h9s5KFEGbcs)
- NotebookLM-derived transcript analysis supplied by the user on 2026-08-18
- [Claude Code Plan Mode — official documentation](https://code.claude.com/docs/en/permission-modes#analyze-before-you-edit-with-plan-mode)
- [Claude Code custom subagents — official documentation](https://code.claude.com/docs/en/subagents)
- [Anthropic Financial Services Plugins — official repository](https://github.com/anthropics/financial-services-plugins)
- [WorldQuant BRAIN IQC](https://www.worldquant.com/brain/iqc/)
- [The Probability of Backtest Overfitting](https://escholarship.org/uc/item/4w1110bb)
- [Merged post — automating alpha research](https://www.facebook.com/permalink.php?story_fbid=pfbid02sD9DjieLGgnUJNsf6p9j7qM7geUAD72QoPbXDH5Na38yTQzoAg287aazDZsU5R8vl&id=100049294731654)
- [Merged post — factor research prototype](https://www.facebook.com/quantcornerthailand/posts/pfbid0rz38Q9hLczZJTsAvc76KdBF7222FoCFzt34HteWapsVJt7butJhVDYtTNu3ApXvul)
- [Merged repost — factor research prototype](https://www.facebook.com/quantcornerthailand/posts/pfbid02vMXK2B3xehAVoqgzchkigLAfBjSmm8Mh42JPdrRXYUZDg2Rs6QhLsC7313APxwGol)
