---
title: Portfolio Factor Attribution ด้วย Claude Code
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Artificial Intelligence]
concepts: [Factor Attribution, Alpha, Style Drift]
entities: [Kanis Saengchote, Kenneth French, Berkshire Hathaway]
tags: [factor-investing, portfolio-analysis, ai]
source_type: Facebook Post
source_title: รีวิวการทำ Portfolio Factor Attribution ด้วย Claude Code
source_author: Kanis Saengchote
source_url: "https://www.facebook.com/ksaengchote/posts/pfbid0jL6ds54NxbDbXLZEydRH4EGzp3ZXGEqFfj9ddissdpJB9EHHpWsMZ4CZVQzvE9EXl?__cft__[0]=AZZpP20SSq78cN67gFE4NJoULxLNWeG8waV2FVzwOhVRUx5K4gfyNKrGuTstw24ESke1o8JXkYuuF9TAQXqY3kpq8u8AYYNXhpdWhivnex5Y-nTV97moQ-H3Kf71Sy6eNAL7TIzwHWDbDDHJt2_C2bVi_LctESjhSAlolKhKAMfC2A&__tn__=%2CO%2CP-R"
alternate_source_urls: ["https://www.facebook.com/ksaengchote/posts/pfbid0j9wdZvne8yYAJWcGRxrNrJkzt9SDtHNP2sx9KK16u1tRUr4LxgkbaUiLoUjmYXdcl?__cft__[0]=AZbpjhckuNpvEaztN7W3b_dRhm-l1aJYM9i9c2FVDjYjlPpX3ZnrTHQz6_7O1ZNOeolasFpE1JzSmYFMLFUpdEmpt9vqApfnremlZHgqM1XIPj_r9ejTeyiXiHV2q1GXktbrbFo_C68yZ089b16FM6O9y-aIqniWtW6O1-a7vyWTDA&__tn__=%2CO%2CP-R"]
canonical_url: "https://www.facebook.com/ksaengchote/posts/pfbid0jL6ds54NxbDbXLZEydRH4EGzp3ZXGEqFfj9ddissdpJB9EHHpWsMZ4CZVQzvE9EXl"
source_date: 2026-04-04
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-18
status: reconciled
confidence: High
related: ["[[Factor Investing]]", "[[Performance Attribution]]"]
---

# Portfolio Factor Attribution ด้วย Claude Code

> [!summary] TL;DR
> Factor attribution ถามว่าผลตอบแทนมาจาก market/factor exposures หรือ residual alpha เท่าใด โดยใช้ AI สร้าง pipeline ได้ แต่การเลือกโมเดล ข้อมูล และการตีความยังต้องอาศัยผู้วิเคราะห์

## Important Details

Workflow ในโพสต์ประกอบด้วยการจัดวันที่ คำนวณ excess returns, full-sample OLS พร้อม Newey–West HAC, rolling 36-month regression, alpha significance และกราฟ cumulative return, model comparison, actual-vs-predicted, factor heatmap และ rolling betas เพื่อหา style drift

## Verification & Reconciliation

- Kenneth French Data Library มี factor returns และอธิบายวิธีสร้าง factor อย่างเป็นทางการ
- งาน *Buffett’s Alpha* สนับสนุนการอธิบายผลตอบแทน Berkshire ผ่าน quality/value/low-risk และ leverage แต่ “replicate ได้” ไม่ได้แปลว่าได้ผลเหมือนทุกช่วง
- Alpha บวกที่มีนัยสำคัญไม่ใช่ “secret sauce” โดยอัตโนมัติ อาจเกิดจาก omitted factors, nonlinear exposure, stale pricing หรือ specification error
- Newey–West ช่วย autocorrelation/heteroskedasticity แต่ lag choice และ small-sample uncertainty ยังสำคัญ

## 🔎 In-depth Details

Factor attribution เป็น **conditional explanation** ภายใต้โมเดลและ factor construction ที่เลือก ไม่ใช่การค้น “สาเหตุแท้จริง” ของผลตอบแทน ขั้นต่ำควรรันหลาย specification (เช่น market-only, 3-factor, 5-factor + momentum), ใช้ factor frequency ที่ตรงกับ portfolio returns และตรวจ overlapping holdings/benchmark ก่อนตีความ alpha

รายงานที่ใช้ตัดสินใจควรแยก: annualized alpha หลัง fees, confidence interval/HAC t-stat, adjusted R², rolling betas, residual drawdown และ contribution ของแต่ละ factor พร้อม sensitivity ต่อ start date และ rebalance rule หาก alpha หายเมื่อเพิ่ม factor ที่สมเหตุผล หรือ beta เปลี่ยนตามช่วง ให้สรุปว่าเป็น model/style uncertainty ก่อนเรียกว่า manager skill

Data Library ของ Kenneth French มีทั้ง current files และ historical archives; การเก็บ data vintage สำคัญต่อ reproducibility เพราะ upstream data และ factor series อาจถูกปรับย้อนหลัง

## Sources

- [Original Facebook post](https://www.facebook.com/ksaengchote/posts/pfbid0jL6ds54NxbDbXLZEydRH4EGzp3ZXGEqFfj9ddissdpJB9EHHpWsMZ4CZVQzvE9EXl?__cft__[0]=AZZpP20SSq78cN67gFE4NJoULxLNWeG8waV2FVzwOhVRUx5K4gfyNKrGuTstw24ESke1o8JXkYuuF9TAQXqY3kpq8u8AYYNXhpdWhivnex5Y-nTV97moQ-H3Kf71Sy6eNAL7TIzwHWDbDDHJt2_C2bVi_LctESjhSAlolKhKAMfC2A&__tn__=%2CO%2CP-R)
- [Identical repost](https://www.facebook.com/ksaengchote/posts/pfbid0j9wdZvne8yYAJWcGRxrNrJkzt9SDtHNP2sx9KK16u1tRUr4LxgkbaUiLoUjmYXdcl?__cft__[0]=AZbpjhckuNpvEaztN7W3b_dRhm-l1aJYM9i9c2FVDjYjlPpX3ZnrTHQz6_7O1ZNOeolasFpE1JzSmYFMLFUpdEmpt9vqApfnremlZHgqM1XIPj_r9ejTeyiXiHV2q1GXktbrbFo_C68yZ089b16FM6O9y-aIqniWtW6O1-a7vyWTDA&__tn__=%2CO%2CP-R)
- [Merged post — fund attribution and value-for-money](https://www.facebook.com/permalink.php?story_fbid=pfbid0AKeRc1UUAC6HNJ5K7svNYNbdf79o9VQrAxg6eZuFHfCL7d7n2EB8zQKQBFfTr3zjl&id=100049294731654)
- [Kenneth French Data Library](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/data_library.html)
- [Fama/French factor construction](https://mba.tuck.dartmouth.edu/pages/faculty/ken.french/Data_Library/f-f_factors.html)
- [AQR - Buffett's Alpha](https://www.aqr.com/insights/research/journal-article/buffetts-alpha)
