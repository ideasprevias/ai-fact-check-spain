# The V/I/H Epistemic Tagging Framework

**Author:** Jorge Baptista  
**Framework:** Decision Architect — V/I/H Epistemic Tagging  
**Purpose:** A structured method for evaluating the factual reliability of AI-generated claims

---

## The Problem This Framework Solves

When an AI system generates a report, it produces text that looks confident and well-structured regardless of whether the underlying information is accurate. A hallucinated statistic and a verified statistic look identical on the page. Both have the same font, the same sentence structure, the same tone of authority.

This is the core problem with using AI-generated content for research or decision-making: **the output gives you no signal about its own reliability.**

The V/I/H framework solves this by forcing every claim through an explicit verification process and attaching a label that tells the reader exactly how much to trust it.

---

## The Three Tags

### [V] — Verified

A claim is Verified when it meets all three of these conditions:

1. A primary authoritative source confirms the specific figure or statement
2. That source can be linked directly — not paraphrased, not summarized, but linked
3. No interpretation is required to connect the source to the claim

**What counts as a primary source:** Government statistical agencies (INE, Eurostat, ONTSI), official institutional reports (OECD, World Economic Forum, European Commission), peer-reviewed research, or official programme documentation from the organization responsible for the data.

**What does not count as a primary source:** News articles, blog posts, secondary summaries, or reports that themselves cite another source without linking to it.

**In plain language:** You found the exact number in the exact document. You can show anyone exactly where it is. There is no room for doubt.

---

### [I] — Inferred

A claim is Inferred when a primary source exists and supports the general direction of the claim, but does not confirm the specific figure stated.

This happens in two common situations:

**Situation 1 — The direction is right, the number is not.**  
Example: A primary source shows that AI adoption in Spain is growing year over year. The AI report states a specific growth rate of 26% CAGR. The trend is confirmed. The exact percentage is not. Tag: [I].

**Situation 2 — The source exists but the scope is wrong.**  
Example: The World Economic Forum's Future of Jobs Report 2024 states that 39% of workers' core skills will be disrupted by AI by 2030. This is a real figure in a real report. But the AI attributed it specifically to Spain. The report is global. The figure is real but the country-level attribution is not confirmed. Tag: [I].

**In plain language:** Something real is there, but the AI stretched it — either the number is approximate or the attribution is too specific. The claim is directionally true but not precisely true.

---

### [H] — Hypothesis

A claim is tagged Hypothesis when no primary source can be found to support it, or when the source cited by the AI either does not contain the claim or does not exist.

This covers four distinct failure modes:

**Failure mode 1 — Magnitude inflation.**  
The AI reports a figure that is directionally plausible but significantly higher or lower than what primary sources show. Example: AI adoption reported as 21%, primary source shows 11.31%. The AI did not make a small rounding error — it nearly doubled the real figure.

**Failure mode 2 — Source fabrication.**  
The AI cites a real institution (CEOE, McKinsey, SEPE) but the specific report or figure cannot be found in any publication from that institution. The institution exists. The data does not.

**Failure mode 3 — Scope misattribution.**  
A real statistic from a global or multi-country study is presented as Spain-specific without justification. The AI borrows a legitimate number from one context and transplants it into a different, narrower context where it does not belong.

**Failure mode 4 — Fabricated data structure.**  
The AI cites a source in a format that source no longer uses. In this project, the AI cited DESI 2024 country rankings (Spain ranked 13th). DESI discontinued country rankings after 2022. The AI did not misread a ranking — it invented a ranking format that does not exist in the cited source and populated it with invented positions.

**In plain language:** The claim is unverified. It may be plausible. It may even be approximately true. But until a primary source confirms it, it should not be used as a basis for any decision.

---

## How the Tags Are Applied in Practice

The verification process follows a strict sequence. The sequence matters because doing it in the wrong order introduces bias.

**Step 1 — Extract claims before searching.**  
Every verifiable claim in the AI report is extracted and listed before any source is checked. This prevents reverse-engineering — the temptation to find a source that approximately matches the claim and call it verified.

**Step 2 — Search primary sources first.**  
For each claim, the fact-checker consults primary sources only. Secondary sources (news articles, aggregator sites) are used only if primary sources do not cover the claim, and they never produce a [V] tag — only [I] at best.

**Step 3 — Apply the tag based on what was found, not what was expected.**  
The tag reflects the evidence, not the prior plausibility of the claim. A claim that sounds reasonable and comes from a reputable AI model still gets tagged [H] if no primary source confirms it.

**Step 4 — Document the absence of evidence explicitly.**  
If a source cannot be found, that is documented — not left blank. "Source not found after search of [institutions consulted]" is a finding, not a gap. This is what separates a rigorous fact-check from an incomplete one.

---

## Why Three Tags and Not Two

A simpler system might use just True and False. The V/I/H system uses three tags because the middle category — Inferred — captures something important that True/False misses.

Many AI hallucinations are not outright fabrications. They are real statistics applied in the wrong context, or correct directions stated with false precision. Collapsing these into "False" would be inaccurate. Collapsing them into "True" would be dangerous. [I] is the honest label for claims that are partially right in a way that matters.

---

## What the Tags Tell a Decision-Maker

| Tag | What it means for a decision | What to do |
|---|---|---|
| [V] Verified | Safe to cite. The figure is confirmed by a primary source you can link. | Use it |
| [I] Inferred | Use with caution. The direction is right but the specific figure is not confirmed. | Acknowledge the uncertainty or find the primary source yourself |
| [H] Hypothesis | Do not cite. The claim is unverified and may be significantly wrong. | Discard or research independently before using |

---

## The Connection to Decision Architect Methodology

The V/I/H framework is one component of the broader Decision Architect methodology, which applies the BADIR analytical framework and Feynman first-principles falsification to research and strategic analysis problems.

The core principle connecting them is the same: **a claim that cannot be proven wrong is an assumption, not a finding.** The V/I/H system operationalizes this principle at the level of individual factual claims. Every tag is a falsification result — either the claim survived verification ([V]), partially survived ([I]), or failed ([H]).

This is why the framework is applied before any conclusions are drawn from the AI report. The analysis cannot be more reliable than the facts it is built on.

---

## A Concrete Example From This Project

The AI-generated report stated:

> *"21% of Spanish companies adopted at least one AI technology in 2024."*

This is the headline figure of the entire report — cited in the executive summary, the cover statistics, and the comparative analysis section.

Verification process:
1. Claim extracted and listed before any source was consulted
2. Primary source consulted: ONTSI — Informe Anual sobre el Sector TIC 2024
3. ONTSI figure for the same metric, same year, same population: **11.31%**
4. Discrepancy: the AI reported a figure nearly double the primary source
5. Tag applied: **[H]**

The consequence: every comparative analysis in the report that uses the 21% figure as a baseline — Spain vs EU peers, Spain's progress since 2020, Spain's position relative to Nordic countries — is built on an unverified foundation. A business decision-maker who used this report to assess Spain's AI readiness would have a systematically distorted picture from the first sentence.

This is what the V/I/H framework is designed to catch — and document.

---

*Framework developed by Jorge Baptista · Decision Architect methodology · April 2025*
