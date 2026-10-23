---
title: "Rebuilding an annual satisfaction benchmark so partner rankings could be trusted"
description: "About 1,800 drivers across seven car brands. Post-stratification weighting to fleet share, design-based inference, LASSO key-driver analysis, per-partner readouts. Partner strategy shifted from new features to reliability."
---

# Rebuilding an annual satisfaction benchmark so partner rankings could be trusted

<div class="meta" markdown="1">
**Where:** Google, Android Auto UX Research (contract), 2025 · **Role:** inherited the annual program; owned the weighting, analysis, and per-partner readouts · **Methods:** post-stratification weighting, design-based inference, LASSO key-driver analysis, qualitative pairing · **n:** about 1,800 drivers across seven car brands, international
</div>

## The decision at stake

An annual international survey tells car-maker partners how their in-car experience compares with each other and with competitors, and where to invest. The audience is partner directors and internal product managers, and what they react to is rankings.

The program I inherited reported raw means. The sample did not match reality at two levels, models within a brand and brands within the fleet, so unweighted comparisons rewarded whoever we happened to over-recruit.

## What I did

- **Post-stratification weights** to real fleet shares at both levels, applied at the level each analysis required, with a survey-design object so standard errors reflected the weights.
- **Statistical comparisons** instead of eyeballed means.
- **Key-driver analysis with LASSO**, because of the number of candidate predictors.
- **Readouts that paired numbers with drivers' own words**, so each partner's "what to focus on" came with evidence a product director could repeat in their own meetings.

![Toy example: two bar charts of three brands, raw and weighted to fleet share, in which the ranking of the top two brands swaps.](/assets/img/fig-weighting.svg)
*Toy example with invented values.*
{: .caption}

## What changed

Weighting did not change the headline: the top drivers of satisfaction were system performance, latency and reliability, not missing features. It did reorder the brands and the order of the drivers, which is exactly what partners act on; unweighted results would have flattered whoever we over-sampled.

Product strategy shifted from building new features toward fixing performance and reliability. Partner readouts focused on weaknesses tied to things partners can change (hardware and software updates) and on premium versus mass-market comparisons, so partners could adjust strategy by vehicle class. One brand led its peers on technical performance but trailed on usability, so its recommendations were interface changes rather than performance work.

## What I'd do differently

- Calibrate on more dimensions and add a nonresponse adjustment.
- Align on deliverable format and preferences before producing a single chart. I rebuilt graphs more times than I should have on this program, and it changed how I start every project now.
