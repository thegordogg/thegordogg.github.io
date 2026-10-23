---
title: "Benchmarking an in-car assistant: from bug frequency to bug cost"
description: "A ~1,000-driver survey, designed backward from the decisions, that changed how an engineering team prioritizes assistant bugs. Elastic Net, Shapley importance, penalty-reward asymmetry."
---

# Benchmarking an in-car assistant: from bug frequency to bug cost

<div class="meta" markdown="1">
**Where:** Google, Android Auto UX Research (contract), 2026 · **My role:** I owned the study end to end (instrument, recruitment, analysis pipeline, report) while the area's lead researcher was on leave; she presented the final readout · **Methods:** survey design, multi-panel recruitment, factor analysis, Elastic Net, Shapley importance, penalty-reward analysis, open-end coding · **n:** about 1,000 drivers
</div>

## The decision at stake

When I picked this up, the Gemini assistant had replaced its predecessor in the car and nobody could say how it was doing with drivers. Engineering was prioritizing bugs by how often they were reported, which is what you do when you don't know what else to do. Product had two asks: what drives satisfaction, and how do we compare with the leading competitor, journey by journey? Our lead researcher for the assistant was about to be out for three weeks, so she handed me the asks at a high level and I owned the study from there.

An engineer suggested mining Reddit for the competitive piece. I pushed back with reasons rather than preference: Reddit over-represents extreme opinions, and it's say-only, so you can't tell how common a problem is or what it does to satisfaction. I offered to look anyway, but I argued that one survey could answer both asks, because both needed the same thing: a measure of what drivers experience (specific failures) and perceive (quality) in each core journey, tied to satisfaction, for our assistant and for the competitor's. The items about what goes well and badly could be asked of both groups unchanged, and that merge saved weeks.

## What I did

I designed backward from the output. First the result format the team needed, then the analysis plan (overall and per-journey satisfaction, 24 perception items, 53 issue items, open-ends), then the sample that plan required, and only then recruitment.

Recruitment was a chain of tradeoffs. One panel was free but slow for this hard-to-reach sample, one was free with known data-quality concerns, and one was fast but paid. I got sign-off for a paid top-off and landed about 1,000 usable drivers on time and under budget. A third assistant's users turned out to be too rare to recruit, so with stakeholders we deferred that comparison rather than report on 19 people.

Halfway through, I rewrote the open-ended items. The first cohort's questions were hypothetical ("how would passengers change what you want?") and produced "nothing" and "no change." Later cohorts got incident recall instead ("tell me about a specific time the assistant's response was less than ideal because of your situation"), and the social and environmental constraints surfaced on their own. I analyzed the cohorts separately to respect the change.

For the modeling, I chose for the decision rather than for the résumé. The perception items reduced to two factors, trust in the assistant's competence and ease of interaction, with an oblique rotation because the two correlate. I estimated drivers of satisfaction with Elastic Net rather than LASSO because the predictors were correlated, then used Shapley decomposition for relative importance. When the lead researcher came back she suggested testing whether failures and successes move satisfaction asymmetrically, so I ran a penalty-reward analysis: for each journey, does a failure cost more than a success earns?

It does, and differently by journey. In some journeys a failure costs a lot and a perfect answer earns nothing; those are hygiene. In others, failures are forgiven and delight is rewarded. A single regression would have told us that misinterpretation matters. It would not have told us which failures are punished and which are forgiven, and that asymmetry is what changed the weights.

## What changed

Before this study, Engineering fixed the most-reported bugs. After it, they had an impact × frequency table I built: each bug's satisfaction cost within its journey, scaled by the journey's penalty weight and by prevalence, with a competitive version that also weights where the competitor is ahead. They adopted it as their bug-prioritization framework.

The re-rank that mattered: the most frequently reported issue would have drawn the most engineering attention. Action failures, where the assistant confirms and then does nothing or does the wrong thing, carry a larger per-incident penalty and are common enough that their total cost is higher. They moved to the top.

![Illustrative quadrant: frequency on the x-axis, per-incident satisfaction cost on the y-axis; the most frequent issue sits lower than two action failures that are rarer but costlier.](/assets/img/fig-frequency-vs-cost.svg)
*Illustrative positions, not study data. The point of the table is the axis most teams don't have: cost per incident.*
{: .caption}

The findings fed the following year's roadmap. And the open-ended answers surfaced something nobody had asked about: drivers won't dictate or listen to messages with passengers aboard. That became the next study.

## What I'd do differently

I'd add behavioral and outcome items, like usage frequency and churn intent, so the drivers tie to behavior and not only to satisfaction. I'd set soft demographic quotas up front; the two cohorts differed in age and gender, and while adjusting for both didn't change the headline or the journey ranking, I'd rather design that out than check it afterward. I'd add straight-lining checks to a 60-item instrument that had one attention check. And incident recall is now my default for any open-end about a situation.
