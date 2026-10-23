---
title: How I work
description: "Three principles, the methods and tools I use, and what you will not find on this site."
---

# How I work

## Three principles

**I design backward from the decision.** I start from the choice the team has to make and what it would take to make it well, then work back to the result format, the analysis, the sample, and only then the instrument. It keeps me from running "a study about users" instead of a study that answers a question, and it is how two separate asks became [one survey](/projects/assistant-benchmarking/) that changed how an engineering team prioritizes bugs.

**I bring quantitative rigor to qualitative data, and the user's voice to quantitative data.** Open-ended answers get codebooks with rules, two coders, adjudication, and a quote behind every number ([example](/projects/coding-open-ends/)). Survey numbers get paired with verbatims so a product director can repeat the finding in their own words ([example](/projects/satisfaction-benchmark/)). Logs get joined to surveys, because behavior tells you what and how often, and attitudes tell you why and how widely ([example](/projects/attitudes-vs-behavior/)).

**I say what the evidence can and cannot support.** Weighted inference instead of raw means when the sample doesn't match the population. Penalties instead of averages when the decision is about failures. Thresholds set from the data when a subgroup is 15 people. And the limits stated in the readout before anyone asks.

## Methods and tools

| Area | What I use |
|---|---|
| Surveys and measurement | Instrument design, cognitive interviews, psychometrics (IRT, EFA/CFA, SEM), post-stratification and calibration weighting, design-based inference, longitudinal panels |
| Modeling | Regression (mixed-effects, logistic), regularized regression (LASSO, Elastic Net), Shapley importance, penalty-reward analysis, latent profile analysis, matched comparisons, A/B tests |
| Qualitative | Unmoderated and moderated think-alouds, semi-structured interviews, diary studies, affinity mapping, inductive codebooks with inter-rater reliability |
| Behavioral data | API collection, NLP classification validated against human coding, experiment telemetry (Detection Response Task), logs joined to surveys |
| AI-assisted pipelines | LLM-assisted coding with dual independent coding, blind adjudication, and human reliability checks; taxonomies and rubrics with traceable quotes |
| Tools | R first (tidyverse, survey/srvyr, lme4, glmnet, lavaan, Shiny), Python, SQL, Qualtrics, UserTesting, Suzy |

## What you won't find here

The industry case studies describe decisions, methods, and sample sizes. They leave out metric values, partner and competitor names, unreleased features, and internal tools, and their figures are illustrative and labeled as such. If you're evaluating me for a role, I'm glad to go deeper in conversation within the same limits.
