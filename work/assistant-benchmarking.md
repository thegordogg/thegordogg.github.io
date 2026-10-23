---
title: "Benchmarking an in-car assistant: from bug frequency to bug cost"
description: "A ~1,000-driver survey, designed backward from the decisions, that changed how an engineering team prioritizes assistant bugs. Elastic Net, Shapley importance, penalty-reward asymmetry."
---

# Benchmarking an in-car assistant: from bug frequency to bug cost

<div class="meta" markdown="1">
**Where:** Google, Android Auto UX Research (contract), 2026 · **Role:** owned the study end to end (instrument, recruitment, analysis pipeline, report) while the area's lead researcher was on leave; she presented the final readout · **Methods:** survey design, multi-panel recruitment, factor analysis, Elastic Net, Shapley importance, penalty-reward analysis, open-end coding · **n:** about 1,000 drivers
</div>

## The decision at stake

The Gemini assistant had replaced its predecessor in the car, and nobody could say how it was doing with drivers. Engineering was prioritizing bugs by how often they were reported. Product had two asks: what drives satisfaction, and how do we compare with the leading competitor, journey by journey?

An engineer suggested mining Reddit for the competitive piece. Reddit over-represents extreme opinions, and it is say-only: it cannot tell you how common a problem is or what it does to satisfaction. I argued for one survey that answered both asks, because both needed the same thing: a measure of what drivers experience (specific failures) and perceive (quality) in each core journey, tied to satisfaction, for our assistant and for the competitor's. The items about what goes well and badly could be asked of both groups unchanged.

## What I did

**Designed backward from the output.** The result format the team needed, then the analysis plan (overall and per-journey satisfaction, 24 perception items, 53 issue items, open-ends), then the sample that plan required, then recruitment.

**Recruited across three panels with explicit tradeoffs.** One was free but slow for this hard-to-reach sample, one free with known data-quality concerns, one fast but paid. I got sign-off for a paid top-off and landed about 1,000 usable drivers on time and under budget. A third assistant's users turned out to be too rare to recruit; with stakeholders, we deferred that comparison rather than report on 19 people.

**Rewrote the open-ends mid-study.** The first cohort's qualitative items were hypothetical ("how would passengers change what you want?") and produced "nothing" and "no change." Later cohorts got incident recall ("tell me about a specific time the assistant's response was less than ideal because of your situation"), and I analyzed the cohorts separately to respect the change. Social and environmental constraints surfaced on their own.

**Chose the models for the decision, not the résumé.** Perceptions reduced to two factors, trust in the assistant's competence and ease of interaction, with an oblique rotation because the two correlate. Drivers of satisfaction via Elastic Net rather than LASSO because predictors were correlated, then Shapley decomposition for relative importance. Then, at the lead researcher's suggestion when she returned, a penalty-reward analysis: for each journey, does a failure cost more than a success earns?

It does, and differently by journey. In some journeys a failure costs a lot and a perfect answer earns nothing (hygiene). In others failures are forgiven and delight is rewarded. A single regression would have said that misinterpretation matters. It would not have said which failures are punished and which are forgiven.

## What changed

I built an impact × frequency table: each bug's satisfaction cost within its journey, scaled by the journey's penalty weight and by prevalence, with a competitive version that also weights where the competitor is ahead. Engineering adopted it as its bug-prioritization framework.

The re-rank that mattered: the most frequently reported issue would have drawn the most engineering attention. Action failures, where the assistant confirms and then does nothing or does the wrong thing, carry a larger per-incident penalty and are common enough that their total cost is higher. They moved to the top.

![Illustrative quadrant: frequency on the x-axis, per-incident satisfaction cost on the y-axis; the most frequent issue sits lower than two action failures that are rarer but costlier.](/assets/img/fig-frequency-vs-cost.svg)
*Illustrative positions, not study data. The point of the table is the axis most teams don't have: cost per incident.*
{: .caption}

The findings fed the following year's roadmap, and the open-ended answers surfaced, unprompted, that drivers will not dictate or listen to messages with passengers aboard. That became the next study.

## What I'd do differently

- Add behavioral and outcome items (usage frequency, churn intent) so drivers tie to behavior, not only to satisfaction.
- Set soft demographic quotas up front. The two cohorts differed in age and gender; adjusting for both did not change the headline or the journey ranking, but I would rather design that out than check it afterward.
- Add straight-lining checks to a 60-item instrument with one attention check.
- Incident recall is now my default for open-ends about situations.
