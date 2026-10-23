---
title: "Coding 6,504 open-ended responses with an audit trail"
description: "A pre-launch study of privacy controls: 108 + 20 unmoderated think-alouds and an AI-assisted coding pipeline with dual independent coding, κ .75–.87, blind adjudication, and a 92% human check."
---

# Coding 6,504 open-ended responses with an audit trail

<div class="meta" markdown="1">
**Where:** Google, Android Auto UX Research (contract), 2026 · **Role:** led fielding, analysis, and reporting; designed the screener and session script with the study lead, who wrote the research plan and presented the shareout; designed and ran the coding pipeline · **Methods:** unmoderated think-alouds, inductive codebooks, LLM-assisted coding with dual independent coding and blind adjudication, human reliability check · **n:** 108 drivers plus a 20-person follow-up; 6,504 open-ended responses across 32 questions
</div>

## The decision at stake

A personalization feature was heading to launch with a set of privacy controls already designed. The question was whether those controls solved the problems drivers actually have. In a car, those problems include other people: passengers hear everything the assistant says, and family members borrow the car.

The requests arrived as a pile: foundational (what do people think this is?), evaluative (are the controls enough?), generative (what would they use it for?). I turned them into 21 research questions in four themes and structured the session as a funnel, from broad reactions to onboarding to what "off" means to passengers and borrowers to the controls themselves, so we could watch mental models form rather than ask about them cold.

## What I did

**Over-recruited on purpose.** The plan said 12 to 15 participants. The marginal cost of an unmoderated session was near zero, the study was high-visibility, and the people with the most to lose, privacy-sensitive drivers and infrequent AI users, are rare and the platform had no quotas. So 108 sessions, then subset. A 20-person follow-up fixed one item that, I realized after fielding, did not answer the question its author meant to ask; I would rather re-field than report a number that means something different from what the reader thinks.

**Rewrote stakeholder items** for clarity, neutrality, and open-endedness, and made implied contrasts explicit: explicit requests versus implicit data use, car versus phone.

**Built the pipeline a qualitative researcher would demand.** Thirty-two open-ended questions produced 6,504 responses, which is weeks of hand-coding we did not have before launch. The question was never human versus machine; it was whether the coding was reliable and auditable.

![Schematic of the coding pipeline: codebooks per question with rules and anchor quotes, two independent coders, agreement statistics, blind adjudication of every disagreement with rationale saved, a human blind re-code, and findings with traceable quotes.](/assets/img/fig-coding-pipeline.svg)
*Schematic of the method; no study data shown.*
{: .caption}

- Codebooks built inductively per question, with inclusion and exclusion rules. I made every merge, split, and drop decision.
- Every code carried an anchor quote traceable to the raw response. That requirement is how I caught the models ignoring negations ("I *wouldn't* want...") and attributing comments to the wrong journey.
- Two independent coders on every cell: 81% raw agreement, κ .75 to .87 across questions.
- Blind adjudication of all 1,232 disagreements, 100% resolved, with the rationale saved per cell.
- A blind re-code of a sample by me against the final codes: 92% agreement, and no disagreement touched a conclusion.
- Subgroup differences reported against thresholds set from the distribution of differences, not p-values, because a segment can be 15 people.

## What changed

The team learned which controls solved which problems. Most drivers' concerns were resolved or partly resolved by the planned controls, and the controls solved the borrowed-car problem well. Two misunderstandings about what a control turns off were education problems, fixable with copy; one was a scope boundary that belonged to another team and was routed there. The concern drivers raised most often, unprompted, was not the one the controls were built for.

Onboarding copy changed before launch. The report is used with car-maker partners. Shareout questions became follow-up analyses within days, including a test of my own hypothesis about one finding, which was not supported, and I said so.

## What I'd do differently

- Pilot the platform first. Technical issues on the unmoderated tool hurt the closed-ended items and may have excluded less tech-savvy drivers, exactly who we most wanted.
- Give forced-choice batteries a "don't know." Forty-one of 109 straight-lined one battery that lacked it.
- For high-stakes items, add a second human pass. Sarcasm, cultural nuance, and multi-clause answers remain the pipeline's weak spots.
