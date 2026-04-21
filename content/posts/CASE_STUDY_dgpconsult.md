---
title: "2 to a 100"
date: 2026-04-16
draft: false
author: "Daniel Peña"
description: "Case Study: AI for BPO Quality Assurance."
tags: ["IA", "BPO", "Cortex-QA"]
---

**Published by:** Data Guardian & Performance Consulting (DGPC)  
**Category:** AI Implementation | BPO Operations | Quality Assurance

---

## The Problem: 

BPOs are facing monumental changes to their way of being, as automated tools become the norm, operations everywhere are embracing AI automations in order to augment the capabilities of their team.

In a BPO only agents generate revenue, everything else is a cost center, this is the reason that QA teams are usually understaffed, and overworked. Usually **your QA team can only review a fraction of what your agents produce.**

In a contact center handling **10,000** interactions per month, a typical QA team samples **2–5% of tickets.** 

*That means **9800** of agent conversations go unreviewed.*

![The QA Blind Spot — 2% Manual QA vs 100% Cortex-QA](/images/posts/cortexqa-coverage.png)

---

## The Solution: 

**Cortex-QA** is an automated audit engine that evaluates 100% of agent interactions using a Large Language Model (LLM) pipeline.

Rather than replacing human judgment, **Cortex-QA scales it**. The system applies the same evaluation criteria a senior QA analyst would use — empathy, technical resolution, protocol compliance — to every single ticket, automatically, with no marginal cost per review.

In the **Cortex-QA** framework, the Analyst is promoted from a "Ticket Grader" to a **Quality Strategist.**

Instead of spending 40 hours a week manually reading individual transcripts to find a single coaching moment, analysts now oversee the entire operation's health. They transition from the tedious "review" phase to **high-value activities:**

- **Trend Orchestration:** Identifying systemic failures across entire shifts or regions.

- **Targeted Coaching:** Spending time only with agents who show statistically significant gaps.

- **Protocol Refinement:** Using AI-generated insights to update training manuals and business logic.

**Cortex-QA** handles the audit volume, so the human team can focus on the human resolution.

---

## Architecture: 

The core innovation behind **Cortex-QA** is what we call the **Double-Pulse agentic loop** — a two-step AI reasoning process that separates qualitative analysis from quantitative scoring.

**Why two steps?** A single prompt asking for both a narrative review and a structured score produces worse output on both dimensions. By separating reasoning from scoring, we give the model space to "think first, then grade" — the same cognitive pattern a skilled human reviewer follows.

### Pulse 1 — Qualitative Reasoning
The engine reads the full conversation thread and generates a concise analytical narrative (≤40 words):

> *"The agent acknowledged the customer's frustration and offered concrete diagnostic steps. Clear resolution path and professional tone throughout the interaction."*

### Pulse 2 — Structured Scoring
Using its own prior analysis as context, the model outputs a structured JSON score:

```json
{
  "empatia":      4,
  "resolucion":   1,
  "cumplimiento": 1
}
```
These two pulses run sequentially for each ticket, and the results are written to a persistent audit journal and a machine-readable results file — ready for dashboard integration in Looker Studio or Power BI.

![Double-Pulse Architecture — How Cortex-QA reasons and scores](/images/posts/cortexqa-doublepulse.svg)

---

## Data Engineering: 
### Corpus Quality as a First-Class Concern

Before an AI can audit an agent, the system must audit the data. In any real-world BPO environment—whether using Zendesk, Salesforce, Genesys, or other tools —raw logs are messy, incomplete, or lack context.

**Cortex-QA** treats Data Quality as foundational. We implement a 7-stage "Integrity Gate" that ensures the LLM only evaluates interactions with enough signal to be meaningful. This prevents "hallucinated" failures and ensures the resulting KPIs are defensible to stakeholders.

The pipeline also reconstructs **multi-turn conversation threads** directly from the raw CSV, capturing up to 6 exchange turns per ticket rather than just the first customer–agent pair. This produces richer context for the LLM and more accurate empathy and resolution scores.

**The result: high-quality tickets** — a corpus where every entry has a specific, contextualized complaint, a substantive agent response, and enough conversational signal for meaningful AI evaluation.

This data engineering discipline is not an implementation detail — it is the core of the system. A QA auditor that scores garbage data produces garbage KPIs. 

**Cortex-QA** treats corpus quality as a first-class engineering concern. 

---

## Results & ROI

| Metric | Before (Manual QA) | After (Cortex-QA) |
|---|---|---|
| Tickets reviewed per month | ~200 (2% of 10,000) | 10,000 (100%) |
| Avg. time per review | 8–12 minutes | ~8 seconds |
| Reviewer cost (per ticket) | ~$1.50–$2.50 | ~$0.002 (API cost) |
| Coverage blind spot | 98% | 0% |
| Feedback latency | Days to weeks | Real-time |
| Compliance gap detection | Reactive | Proactive |

**At 10,000 tickets per month, the cost delta is significant:**

- Manual QA at 2% coverage: ~$300–500/month for 200 reviews
- Cortex-QA at 100% coverage: ~$20/month in API costs

That is **50x the coverage at a fraction of the cost** — with no reviewer fatigue, no scheduling overhead, and no inconsistency between reviewers.

![Cost vs Coverage — Manual QA vs Cortex-QA](/images/posts/cortexqa-cost.svg)

---

## Beyond Cost: Strategic Value

The real ROI of Cortex-QA is not just cost reduction — it is the intelligence that 100% coverage unlocks:

**Agent coaching at scale.** When every interaction is scored, managers can identify an agent's specific pattern weaknesses rather than acting on anecdote.

**Compliance without anxiety.** Industries with strict communication regulations (financial services, healthcare) can demonstrate documented, systematic review of every customer interaction.

**Trend detection.** Aggregated scores across thousands of tickets reveal product issues, policy gaps, and seasonal complaint spikes before they surface in CSAT surveys.

**Performance benchmarking.** Objective, consistent scores across all agents and all shifts create a defensible basis for performance reviews and incentive structures.

---

## What's Next

DGPC is extending Cortex-QA with:

- **Beyond individual audits**, we are moving toward Context-Aware QA. By integrating RAG, Cortex-QA doesn't just judge a ticket based on a general LLM 'vibe'—it judges it against your company’s specific, proprietary internal knowledge base.
- **Async batch processing** to reduce 1,000-ticket audit time from ~2 hours to under 15 minutes
- **Dashboard integration** for real-time QA scorecards in Looker Studio
- **Agent-level roll-up reports** to feed directly into performance management workflows

---

## Work With Us

If your operation is still auditing 2% of interactions and hoping the other 98% are fine — **they probably aren't.**

DGPC specializes in building AI infrastructure that makes BPO quality assurance scalable, defensible, and actionable. We work with operations teams to design, implement, and operationalize systems like Cortex-QA within your existing workflow.

We turn your Quality Assurance department from a bleeding cost center into a **Strategic Intelligence unit.**

**Ready to close the coverage gap?**

[Contact DGPC →](https://www.linkedin.com/in/daniel-gustavo-pe%C3%B1a-chaves-dgpc/)

---

*Data Guardian & Performance Consulting | dgpconsult.com*
