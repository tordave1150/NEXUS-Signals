---
title: Quantum-Assisted Portfolio Rebalancing
note_type: source
primary_topic: Data_Science
secondary_topics: [Investment, Quantum Computing]
concepts: [Portfolio Rebalancing, QUBO, QAOA]
entities: [PopQuants]
tags: [portfolio-optimization, quantum-computing, rebalancing]
source_type: Facebook Post
source_title: Quantum-Assisted Optimal Rebalancing
source_author: PopQuants
source_url: "https://www.facebook.com/popquants/posts/pfbid0akD76LrxMzkU1fkrbtwHadH4uvDPo2hVYwFtXD8DgrA96YbinmyX7i7VdYYYgiF2l?__cft__[0]=AZbDQ134YyJlZO2irkehjo7Iz1z6uGYWxfr7gQneX0RLFMPDoQh2K-DuxsDj8hoBztnsTXgQYV0Set5dIY8ANaCxYlnRat2KRMmtwUGdG8A137FWLCTrNH1bA-Xn6zh3bYJzdPXbcMngGREI7wv5qWBkCO3iAt4loSugivqmNQg01w&__tn__=%2CO%2CP-R"
alternate_source_urls: ["https://www.facebook.com/popquants/posts/pfbid0b41dMrARNBASZfcyyFp21xxTYC2nvMRT5zoh7w1TFf2m92i7jHDzkGaUNDPtdRnkl?__cft__[0]=AZaTenpidIUbFjJBzsMo7WpKEjovBkfjL5QMREvYiEKfNQU3n5ditzvTfYYO9rJcVCJrsk0UmetT3jdA41s2EXYHHmfc-uv9BNxmoVVbUfzqpyz5-R8mcrNQR-dZJqFw4ClHU8RTdofIXfF7MQArPZql-dzeFMDoiblxErFyaMFR2A&__tn__=%2CO%2CP-R"]
canonical_url: "https://www.facebook.com/popquants/posts/pfbid0akD76LrxMzkU1fkrbtwHadH4uvDPo2hVYwFtXD8DgrA96YbinmyX7i7VdYYYgiF2l"
source_date: 2026-04-02
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: reconciled
confidence: Medium
related: ["[[Portfolio Rebalancing]]", "[[Transaction Costs]]"]
---

# Quantum-Assisted Portfolio Rebalancing

> [!summary] TL;DR
> งานทดลองแปลง “วันใดควร rebalance” เป็น QUBO และใช้ QAOA เลือก schedule โดยคำนึงถึง drift กับ transaction cost ผลทดสอบปี 2025 ดีขึ้นเล็กน้อยพร้อมจำนวน rebalances ลดลงมาก

## Important Details

หุ้น 10 ตัวถูกเลือกด้วย Ledoit–Wolf covariance และ hierarchical clustering จาก S&P 500 ก่อนใช้ Genetic Algorithm หา target weights ผลที่โพสต์รายงาน: GA+QAOA return 10.10%, Sharpe 0.588, 8 rebalances และ cost 6.1 bp เทียบ GA/10-day return 9.77%, Sharpe 0.575, 24 rebalances และ cost 11.0 bp

## Verification & Reconciliation

ยืนยันว่ามี preprint arXiv ชื่อเดียวกัน แต่ผลต่าง Sharpe 0.013 เล็กและยังไม่แสดง statistical/economic significance งานเป็น preprint ใหม่ ช่วง OOS สั้น และไม่พิสูจน์ quantum advantage เหนือ classical optimizer ที่เทียบอย่างเข้มงวด ผลอาจไวต่อ universe, cost model และ hyperparameters

## Sources

- [Original Facebook post](https://www.facebook.com/popquants/posts/pfbid0akD76LrxMzkU1fkrbtwHadH4uvDPo2hVYwFtXD8DgrA96YbinmyX7i7VdYYYgiF2l?__cft__[0]=AZbDQ134YyJlZO2irkehjo7Iz1z6uGYWxfr7gQneX0RLFMPDoQh2K-DuxsDj8hoBztnsTXgQYV0Set5dIY8ANaCxYlnRat2KRMmtwUGdG8A137FWLCTrNH1bA-Xn6zh3bYJzdPXbcMngGREI7wv5qWBkCO3iAt4loSugivqmNQg01w&__tn__=%2CO%2CP-R)
- [Identical repost](https://www.facebook.com/popquants/posts/pfbid0b41dMrARNBASZfcyyFp21xxTYC2nvMRT5zoh7w1TFf2m92i7jHDzkGaUNDPtdRnkl?__cft__[0]=AZaTenpidIUbFjJBzsMo7WpKEjovBkfjL5QMREvYiEKfNQU3n5ditzvTfYYO9rJcVCJrsk0UmetT3jdA41s2EXYHHmfc-uv9BNxmoVVbUfzqpyz5-R8mcrNQR-dZJqFw4ClHU8RTdofIXfF7MQArPZql-dzeFMDoiblxErFyaMFR2A&__tn__=%2CO%2CP-R)
- [arXiv paper](https://arxiv.org/abs/2603.16904)

