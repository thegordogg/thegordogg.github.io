---
title: "Rebuilding an annual satisfaction benchmark so partner rankings could be trusted"
description: "About 1,800 drivers across seven car brands. Post-stratification weighting to fleet share, design-based inference, LASSO key-driver analysis, per-partner readouts. Partner strategy shifted from new features to reliability."
---

# Rebuilding an annual satisfaction benchmark so partner rankings could be trusted

<div class="meta" markdown="1">
**Where:** Google, Android Auto UX Research (contract), 2025 · **My role:** I inherited the annual program and owned the weighting, the analysis, and the per-partner readouts · **Methods:** post-stratification weighting, design-based inference, LASSO key-driver analysis, pairing quantitative results with verbatims · **n:** about 1,800 drivers across seven car brands, international
</div>

## The decision at stake

Once a year, an international survey tells car-maker partners how their in-car experience compares with each other and with competitors, and where to invest. The audience is partner directors and internal product managers, and what they react to is rankings.

The program I inherited reported raw means. The sample didn't match reality at two levels, models within a brand and brands within the fleet, which meant unweighted comparisons rewarded whoever we happened to over-recruit. Nobody had asked me to fix that. It just wasn't a ranking I could put my name on.

## What I did

I built post-stratification weights to real fleet shares at both levels and applied them at the level each analysis required, with a survey-design object so the standard errors reflected the weights. I replaced eyeballed means with statistical comparisons, and because there were many candidate predictors, I ran the key-driver analysis with LASSO. Then I paired each partner's numbers with their own drivers' words, so "what to focus on" came with evidence a product director could repeat in their own meetings.

![Toy example: two bar charts of three brands, raw and weighted to fleet share, in which the ranking of the top two brands swaps.](/assets/img/fig-weighting.svg)
*Toy example with invented values.*
{: .caption}

## What changed

Weighting didn't change the headline. The top drivers of satisfaction were system performance, latency and reliability, not missing features, either way. It did reorder the brands and the order of the drivers, which is exactly what partners act on, and unweighted results would have flattered whoever we over-sampled.

Product strategy shifted from building new features toward fixing performance and reliability. The partner readouts focused on weaknesses tied to things partners can actually change, like hardware and software updates, and on premium versus mass-market comparisons so partners could adjust strategy by vehicle class. One brand led its peers on technical performance but trailed on usability, so its recommendations were interface changes rather than performance work.

## What I'd do differently

I'd calibrate on more dimensions and add a nonresponse adjustment. And I'd agree on the deliverable format before producing a single chart. I rebuilt graphs more times than I should have on this program, and it changed how I start every project now.
