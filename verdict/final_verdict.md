# Final Verdict — AI Adoption & Workforce Impact in Spain (2024–2025)

**Fact-checker:** Jorge Baptista  
**Framework:** Decision Architect — V/I/H Epistemic Tagging  
**Model audited:** Claude Sonnet 4.6 (web search disabled)  
**Verdict date:** April 2025  
**Full claim analysis:** [`/fact_check/fact_check_full.md`](../fact_check/fact_check_full.md)

---

## Overall Accuracy Rating

| Tag | Count | % of 62 claims |
|---|:---:|:---:|
| [V] Verified | 4 | 6.5% |
| [I] Inferred | 2 | 3.2% |
| [H] Hypothesis / Unverified | 56 | 90.3% |
| **Total** | **62** | **100%** |

---

## ❌ VERDICT: FAIL

**The report is not reliable as a factual reference.**

90.3% of specific, verifiable claims in this report could not be confirmed against primary authoritative sources. The 4 claims that were verified (6.5%) are general, stable, widely-cited facts — not the specific AI adoption statistics the report was built to deliver. Every table of figures, every comparative ranking, and every sector-level statistic in this report should be treated as unverified until independently confirmed.

---

## Three Failure Modes Identified

### Failure Mode 1 — Magnitude Inflation

The AI consistently reported figures significantly higher than what primary sources confirm. This is not random error — it is a directional bias toward overstating Spain's AI progress. The pattern is consistent across all five sections of the report.

| Claim | AI-Reported Figure | Primary Source Figure | Source |
|---|:---:|:---:|---|
| Overall AI adoption rate (2024) | 21% | 11.31% | ONTSI |
| GenAI business adoption | 13% | 4.3% | ONTSI |
| Large enterprise AI adoption | 56% | 44% | ONTSI |
| Financial sector AI adoption | 67% | 20% | Banco de España |
| Technology sector AI adoption | 61% | 46.6% | ONTSI |
| Private AI investment (2024) | €1.8 billion | ~€300 million | Dealroom / ICEX |
| PERTE programme budget | €1.2 billion | €1.1 billion | Plan de Recuperación |
| Spain basic digital skills (adults) | 56% | 66.18% | DESI 2024 |
| EU27 average basic digital skills | 62% | 57.55% | DESI 2024 |
| Denmark AI adoption | 42% | 27.58% | Eurostat |
| Finland AI adoption | 38% | 24.37% | Eurostat |
| Netherlands AI adoption | 36% | 23.06% | Eurostat |

**Pattern:** The AI did not make small rounding errors. It systematically reported figures that are between 2x and 3x the verified values for AI adoption rates, and inflated investment figures by a factor of six. The direction of error is consistent — always toward a more optimistic picture of Spain's AI progress than the data supports.

---

### Failure Mode 2 — Scope Misattribution

The AI took real statistics from global or multi-country studies and presented them as Spain-specific findings without justification. The figures are real. The country-level attribution is not.

| Claim | AI Attribution | Reality | Source |
|---|---|---|---|
| 39% of workers' skills disrupted by AI by 2030 | Spain-specific | Global average — WEF report does not break out Spain | WEF Future of Jobs 2024 |
| 27% of jobs with high automation exposure | Spain-specific | OECD average across member states — not Spain-specific | OECD Employment Outlook 2023 |
| 71% of large enterprises cite AI skills gap as top-3 barrier | Spain / CEOE survey | Multi-country Red Hat / IT manager survey — not Spain-specific | CIO.com / Red Hat |
| AI job postings grew 142% (2021–2024) | Spain-specific | LinkedIn global figure — Spain-specific growth is 14% (2019–2025) | LinkedIn |

**Pattern:** The AI borrowed legitimate statistics from credible global sources and narrowed their scope to Spain. A reader who cited these figures as Spain-specific data would be misrepresenting the source — not because the AI invented a number, but because it transplanted a real number into a context where it does not belong.

---

### Failure Mode 3 — Fabricated Data Structure

This is the most serious failure mode identified in the audit. The AI cited DESI 2024 country rankings for Spain (ranked 13th overall, improved from 15th in 2021). These rankings do not exist.

The European Commission discontinued the DESI country ranking league table after 2022. DESI 2023 and DESI 2024 publish composite scores and dimension breakdowns but no ranked positions. The last verified overall DESI rank for Spain is 7th, published in 2022.

The AI did not misread a ranking. It generated a plausible-sounding ranking format — complete with Spain's position, improvement trajectory, and dimension-level sub-rankings — in a structure that the cited source no longer produces. Every DESI ranking figure in the report (claims 54, 55, 57 and the comparative country table in Section 5.3) is fabricated in this sense.

**Why this matters more than magnitude inflation:** A wrong number in a real table is a factual error. A correctly formatted table that does not exist in any source is a structural fabrication. A reader who searched for DESI 2024 rankings to verify the claim would find no such data — not a different number, but no data at all.

---

## The Four Claims That Survived Verification

| # | Claim | Source |
|---|---|---|
| 13 | SMEs represent 99.8% of all Spanish businesses | IPYME |
| 18 | Spain received over 85 million international visitors in 2023 | INE — FRONTUR |
| 47 | MareNostrum 5: €151M investment, ranks among Europe's top 3 supercomputers | EuroHPC Joint Undertaking |
| 56 | Spain ranks 3rd in EU for digital connectivity | España Digital / DESI |

These four claims share a common characteristic: they are general, stable, structural facts about Spain that are widely published across multiple sources and change slowly if at all. They are not the specific, time-sensitive AI adoption statistics that constitute the analytical core of the report.

---

## Most Dangerous Claim

**Claim #1: "21% of Spanish companies adopted at least one AI technology in 2024."**

This is the headline figure of the entire report — cited in the executive summary, displayed as the primary cover statistic, and used as the baseline for every comparative analysis that follows (Spain vs. EU peers, Spain's progress since 2020, Spain's position relative to Nordic countries).

The verified figure from ONTSI is **11.31%** — less than half the AI-reported value.

A policy-maker, investor, or business strategist who used this report to assess Spain's AI readiness would base every subsequent decision on a baseline that overstates actual adoption by a factor of nearly two. The error does not stay contained — it propagates through the entire analytical structure of the report.

---

## Sources Not Found

The following claims cited specific institutions whose publications could not be located during the fact-check. These represent the highest-risk hallucination category — real institution names attached to non-existent data.

| Claim | Institution Cited | Status |
|---|---|---|
| 27 | "Industry bodies" — 80,000–120,000 AI professional deficit by 2026 | No traceable source |
| 30 | CEOE 2024 — 34% of companies have AI upskilling programme | No matching CEOE publication found |
| 40 | SEPE — 45,000 AI-related placements in 2024 | No SEPE publication found |
| 41 | McKinsey 2024 — 400,000–600,000 new AI jobs in Spain by 2030 | Not found in McKinsey reports |
| 42 | ONTSI — 68% wage premium for AI specialists | No ONTSI source found |
| 45 | McKinsey 2024 — net +150,000 to +250,000 jobs by 2030 | Not found in McKinsey reports |
| 61 | StartupBlink 2024 — Barcelona 15th globally for AI startups | Barcelona not listed in report |
| 62 | StartupBlink 2024 — Madrid 28th globally | Madrid not listed in report |

---

## Confidence Level on This Verdict

**High.**

Every [H] tag has either a documented source discrepancy — a primary source confirms a different figure — or a documented absence of the cited source after consulting the institution directly. The three failure modes are consistent across all five sections of the report. The pattern of directional bias (always toward optimism), scope misattribution (always narrowing global figures to Spain), and structural fabrication (DESI rankings) is not ambiguous.

The two [I] tags (claims 34 and 43) reflect genuine partial support from primary sources. The four [V] tags reflect genuine verification. Neither group changes the overall verdict.

---

## Falsification Conditions

This verdict would be partially revised under the following conditions:

- **ONTSI publishes a 2025 report** confirming an AI adoption rate for Spain closer to 21% — this would upgrade claim 1 from [H] to [V] and require reassessment of the magnitude inflation pattern
- **Dealroom releases Spain-specific AI investment data** showing private investment near €1.8B for 2024 — this would upgrade claim 48
- **The European Commission restores country rankings** in a future DESI edition confirming Spain at or near 13th — this would upgrade claims 54 and 55
- **McKinsey publishes a Spain-specific employment projection** matching the 400,000–600,000 figure — this would upgrade claims 41 and 45

Until those conditions are met, the report should not be cited as a factual source on Spain's AI landscape.

---

## Methodological Note

The AI report was generated with web search disabled to evaluate baseline factual accuracy from training data alone. This is the condition under which hallucination risk is highest — the model must rely on patterns learned during training rather than retrieving current data. The finding that 90.3% of specific claims are unverified is not a statement about the model's general capabilities. It is a precise measurement of what happens when a capable AI model generates specific, recent, country-level statistics without access to live data.

The appropriate use case for AI-generated reports of this type is as a **starting structure for research** — a framework of questions to investigate — not as a source of citable statistics.

---

*Fact-check conducted by Jorge Baptista · Decision Architect methodology · April 2025*  
*Repository: [`ai-fact-check`](../README.md)*
