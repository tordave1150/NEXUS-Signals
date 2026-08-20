---
title: Hidden Markov Models Algorithms Guide
note_type: source
primary_topic: Data Science
secondary_topics: [Probabilistic Models, NLP]
concepts: [Hidden Markov Model, Forward Algorithm, Viterbi, Forward-Backward]
entities: [Daniel Jurafsky, James H. Martin, Stanford University]
tags: [hmm, dynamic-programming, probabilistic-models]
source_type: Facebook Post and Stanford PDF
source_title: Hidden Markov Models
source_author: Thongchai Thampueak, Daniel Jurafsky and James H. Martin
source_url: "https://www.facebook.com/chaivsai/posts/pfbid0VffrYDczECpTPAcdJLNzupDJZubTpLji4gsm2bGSETehTzPgZ7Md6HriFwEFWBc1l?__cft__[0]=AZYz-1P-b6mxa9UHvSZpoqI0GvZQAHxNR-XeFqahtO5dvo_p6Hfj949Gm6RBdWUv3_JKnhmpo6WBqtZOXMG4--CZx-MDmTtbhb9ycpRgE_RLLyzWi4k_m_ZDorHOVP0GbGh80BmU3peUSYFUB3AOOaMnxj24V0yR1phjP5RNVJFFIg&__tn__=%2CO%2CP-R"
canonical_url: "https://www.facebook.com/chaivsai/posts/pfbid0VffrYDczECpTPAcdJLNzupDJZubTpLji4gsm2bGSETehTzPgZ7Md6HriFwEFWBc1l"
additional_source_url: "https://web.stanford.edu/~jurafsky/slp3/A.pdf?utm_id=97758_v0_s00_e0_tv1_a1demonyfxk4wn&fbclid=IwY2xjawTuxJBwZG9mAWV4dG4DYWVtAjEwAGJyaWQRMU9kTGJLWFFxZFF2MTVxb2xzcnRjBmFwcF9pZBAyMjIwMzkxNzg4MjAwODkyAAEeMR4JPDtAB2F1IQyWgQ7bKIUvngdjPf827oLdoyZSQ9frB2KZvpOHkM7AHHU_aem_jZjSZ2YmdC48Q18NdgLEYQ"
additional_canonical_url: "https://web.stanford.edu/~jurafsky/slp3/A.pdf"
source_date: 2026-07-13
captured_at: 2026-08-17
created: 2026-08-17
updated: 2026-08-17
status: verified
confidence: High
related: ["[[Markov Chain]]", "[[Sequence Models]]"]
---

# Hidden Markov Models Algorithms Guide

## Core Model

Appendix A ของ *Speech and Language Processing* อธิบาย HMM ด้วย hidden states, transition matrix, emission probabilities และ initial distribution ภายใต้ first-order Markov และ output-independence assumptions

## Three Problems

- Likelihood: Forward algorithm รวมความน่าจะเป็นของทุก hidden path อย่างมีประสิทธิภาพ
- Decoding: Viterbi หา state sequence ที่มีความน่าจะเป็นสูงสุด
- Learning: Forward-Backward/Baum-Welch ประมาณพารามิเตอร์เมื่อไม่มี state labels

เอกสาร 17 หน้าใช้ตัวอย่างอากาศกับจำนวนไอศกรีมเพื่อแสดง trellis และ dynamic programming ชัดเจน เหมาะเป็น reference พื้นฐานก่อนต่อยอดสู่ regime models หรือ sequence labeling

## Duplicate Reconciliation

URL-186 เป็นโพสต์แนะนำ และ URL-187 เป็น PDF ต้นฉบับ จึงรวมเป็น Source Note เดียว

## Sources

- [Original Facebook post](https://www.facebook.com/chaivsai/posts/pfbid0VffrYDczECpTPAcdJLNzupDJZubTpLji4gsm2bGSETehTzPgZ7Md6HriFwEFWBc1l?__cft__[0]=AZYz-1P-b6mxa9UHvSZpoqI0GvZQAHxNR-XeFqahtO5dvo_p6Hfj949Gm6RBdWUv3_JKnhmpo6WBqtZOXMG4--CZx-MDmTtbhb9ycpRgE_RLLyzWi4k_m_ZDorHOVP0GbGh80BmU3peUSYFUB3AOOaMnxj24V0yR1phjP5RNVJFFIg&__tn__=%2CO%2CP-R)
- [Stanford PDF](https://web.stanford.edu/~jurafsky/slp3/A.pdf?utm_id=97758_v0_s00_e0_tv1_a1demonyfxk4wn&fbclid=IwY2xjawTuxJBwZG9mAWV4dG4DYWVtAjEwAGJyaWQRMU9kTGJLWFFxZFF2MTVxb2xzcnRjBmFwcF9pZBAyMjIwMzkxNzg4MjAwODkyAAEeMR4JPDtAB2F1IQyWgQ7bKIUvngdjPf827oLdoyZSQ9frB2KZvpOHkM7AHHU_aem_jZjSZ2YmdC48Q18NdgLEYQ)


