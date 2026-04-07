# AI Fact-Check

**Can an AI model accurately report specific statistics about AI adoption in Spain?**

This project answers that question by generating a research report using an AI model with web search disabled, then verifying every specific, verifiable claim against primary authoritative sources using a structured epistemic tagging framework.

**Result: 90.3% of claims were unverified.**

---

## The Finding in One Table

| Tag | Count | % of 62 claims |
|---|:---:|:---:|
| ✅ [V] Verified | 4 | 6.5% |
| ⚠️ [I] Inferred | 2 | 3.2% |
| ❌ [H] Hypothesis / Unverified | 56 | 90.3% |

The 4 verified claims are general, stable facts (Spain's SME share, tourism figures, MareNostrum 5 investment, connectivity ranking). Every specific AI adoption statistic — the figures a business decision-maker would actually use — failed verification.

---

## Why This Project Exists

AI systems produce text that looks authoritative regardless of whether the underlying data is accurate. A hallucinated statistic and a verified statistic look identical on the page. Both have the same formatting, the same confident tone, the same institutional citations.

This creates a practical problem: **how do you know which claims to trust?**

This project builds and applies a structured answer to that question — a methodology called V/I/H epistemic tagging that evaluates every claim individually and attaches an explicit reliability label.

---

## The V/I/H Methodology

Every claim in the AI-generated report was evaluated against primary sources and tagged with one of three labels:

**[V] Verified** — The exact figure is confirmed by a primary authoritative source with a direct link. No interpretation required.

**[I] Inferred** — A primary source supports the direction of the claim but not the specific figure. The claim is directionally true but not precisely confirmed.

**[H] Hypothesis** — No primary source found, or the source cited by the AI does not contain the claim. The figure should not be used as a basis for any decision until independently confirmed.

Three distinct failure modes were identified in this audit:

1. **Magnitude inflation** — The AI consistently reported figures 2–6x higher than primary sources confirm, always in the direction of overstating Spain's AI progress
2. **Scope misattribution** — Real global statistics were presented as Spain-specific findings without justification
3. **Fabricated data structure** — The AI cited DESI 2024 country rankings that do not exist; DESI discontinued ranked league tables after 2022

Full methodology explanation: [`/methodology/VIH_framework.md`](methodology/VIH_framework.md)

---

## Repository Structure

```
ai-fact-check/
│
├── README.md                        ← This file
│
├── methodology/
│   └── VIH_framework.md             ← Full explanation of V/I/H tagging system
│
├── prompt/
│   └── generation_prompt.md         ← Exact prompt used to generate the AI report
│
├── reports/
│   └── ai_generated_report.md       ← Unedited AI output (Claude Sonnet 4.6, web search off)
│
├── fact_check/
│   └── fact_check_full.md           ← 62 claims evaluated one by one with tags and notes
│
├── sources/
│   └── sources_cited.md             ← Every primary source consulted during verification
│
└── verdict/
    └── final_verdict.md             ← Summary findings, failure modes, confidence level
```

---

## The Most Important Finding

The headline figure of the AI report — **"21% of Spanish companies adopted at least one AI technology in 2024"** — is the first statistic cited in the executive summary and the foundation for every comparative analysis that follows.

The verified figure from ONTSI (Spain's official telecommunications observatory) is **11.31%**.

The AI reported a figure nearly double the actual value for the most prominent claim in the document. Every comparative table, every EU peer ranking, and every strategic conclusion built on that baseline is therefore built on an unverified foundation.

This is not an edge case. It is the headline.

---

## Experimental Design

The report was generated with **web search disabled** deliberately. When an AI model cannot access live data, it must rely entirely on its training data to produce specific statistics. This is the condition under which hallucination risk is highest — and therefore the condition under which fact-checking is most meaningful.

A report generated with web search enabled would largely retrieve and cite accurate sources, removing the analytical value of the audit. The goal of this project is not to evaluate what AI can do with internet access. It is to measure what AI produces from memory alone when asked for specific, recent, country-level data.

| Parameter | Value |
|---|---|
| Model | Claude Sonnet 4.6 |
| Web search | Disabled |
| Report topic | AI adoption and workforce impact in Spain, 2024–2025 |
| Claims extracted | 62 |
| Primary sources consulted | 18 |

---

## What This Project Demonstrates

**For AI evaluation work:** A structured, reproducible methodology for auditing AI-generated factual claims — with explicit confidence levels, documented sources, and falsification conditions on every finding.

**For data analytics work:** End-to-end application of the Decision Architect framework — anchor question defined before data collection, hypotheses written before verification, claims tagged by evidence strength, verdict delivered with explicit confidence level and falsification conditions.

**For anyone using AI-generated research:** A concrete, documented example of the gap between what an AI report looks like and what it can be verified to contain.

---

## How to Reproduce This Audit

1. Use the prompt in [`/prompt/generation_prompt.md`](prompt/generation_prompt.md) with any capable language model and web search disabled
2. Extract every verifiable claim (specific numbers, rankings, institutional attributions)
3. Consult primary sources listed in [`/sources/sources_cited.md`](sources/sources_cited.md)
4. Apply V/I/H tags following the criteria in [`/methodology/VIH_framework.md`](methodology/VIH_framework.md)
5. Compare your findings to [`/fact_check/fact_check_full.md`](fact_check/fact_check_full.md)

The methodology is fully transparent and independently reproducible.

---

## Author

**Jorge Baptista**  
Data Analyst · Decision Architect methodology  
Madrid, Spain

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Jorge_Baptista-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/jorge-baptista-1a1322143/)

---

*Built with the Decision Architect framework — BADIR analytical structure + Feynman first-principles falsification*
