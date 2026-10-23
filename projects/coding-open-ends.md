---
title: "Coding 6,504 open-ended responses with an audit trail"
description: "A pre-launch study of privacy controls: 108 + 20 unmoderated think-alouds and an AI-assisted coding pipeline with dual independent coding, κ .75–.87, blind adjudication, and a 92% human check."
---

# Coding 6,504 open-ended responses with an audit trail

<div class="meta" markdown="1">
**Where:** Google, Android Auto UX Research (contract), 2026 · **My role:** I led fielding, analysis, and reporting; designed the screener and session script with the study lead, who wrote the research plan and presented the shareout; and designed and ran the coding pipeline · **Methods:** unmoderated think-alouds, inductive codebooks, LLM-assisted coding with dual independent coding and blind adjudication, human reliability check · **n:** 108 drivers plus a 20-person follow-up; 6,504 open-ended responses across 32 questions
</div>

## The decision at stake

A personalization feature was heading to launch with a set of privacy controls already designed. The question was whether those controls solved the problems drivers actually have. In a car, those problems include other people: passengers hear everything the assistant says, and family members borrow the car.

The requests arrived as a pile. Some were foundational (what do people think this is?), some evaluative (are the controls enough?), some generative (what would they use it for?). I turned them into 21 research questions in four themes, and I structured the session as a funnel, from broad reactions to onboarding to what "off" means to passengers and borrowers to the controls themselves, so we could watch mental models form instead of asking about them cold.

## What I did

I over-recruited on purpose. The plan said 12 to 15 participants. The marginal cost of an unmoderated session was near zero, the study was high-visibility, and the people with the most to lose, privacy-sensitive drivers and infrequent AI users, are rare, and the platform had no quotas. So I ran 108 sessions and subset afterward. After fielding I realized that one item, drafted by a stakeholder, didn't answer the question he actually had, so I ran a 20-person follow-up with a corrected item rather than report a number that meant something different from what he thought it meant.

Stakeholders drafted most of the items and I rewrote them for clarity, neutrality, and open-endedness. I also made the contrasts they cared about explicit: explicit requests versus implicit data use, car versus phone.

Then the pipeline. Thirty-two open-ended questions produced 6,504 responses, which is weeks of hand-coding we didn't have before launch. I never framed it as human versus machine. The question was whether the coding would be reliable and auditable, so I built the pipeline around the properties a qualitative researcher would demand.

![Schematic of the coding pipeline: codebooks per question with rules and anchor quotes, two independent coders, agreement statistics, blind adjudication of every disagreement with rationale saved, a human blind re-code, and findings with traceable quotes.](/assets/img/fig-coding-pipeline.svg)
*Schematic of the method; no study data shown.*
{: .caption}

I built the codebooks inductively, one per question, with inclusion and exclusion rules, and I made every merge, split, and drop decision myself. Every code had to carry an anchor quote traceable to the raw response; that requirement is how I caught the models ignoring negations ("I *wouldn't* want...") and attributing comments to the wrong journey. Two independent coders worked every cell, with 81% raw agreement and κ between .75 and .87 across questions. I blind-adjudicated all 1,232 disagreements and saved the rationale per cell. Then I blind re-coded a sample myself against the final codes: 92% agreement, and none of the disagreements touched a conclusion. For subgroups, I set reporting thresholds from the distribution of differences rather than from p-values, because a segment can be 15 people.

## What changed

The team learned which controls solved which problems. Most drivers' concerns were resolved or partly resolved by the planned controls, and the controls handled the borrowed-car problem well. Two misunderstandings about what a control turns off were education problems and fixable with copy; one was a scope boundary that belonged to another team, so I routed it there. The concern drivers raised most often, unprompted, was not the one the controls had been built for.

The onboarding copy changed before launch, and the report is now used with car-maker partners. Questions from the shareout became follow-up analyses within days, including a test of my own hypothesis about one finding. It wasn't supported, and I said so.

## What I'd do differently

Pilot the platform first. Technical issues on the unmoderated tool hurt the closed-ended items and may have excluded less tech-savvy drivers, which is exactly who we most wanted. Give forced-choice batteries a "don't know"; 41 of 109 people straight-lined the one that lacked it. And for high-stakes items I'd add a second human pass, because sarcasm, cultural nuance, and multi-clause answers are still where the pipeline is weakest.
