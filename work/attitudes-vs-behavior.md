---
title: "Where attitudes and behavior diverge: 300,000 posts and panel surveys"
description: "Doctoral research published in Psychological Science (2024): most people say they like political open-mindedness, but closed-minded posts win online. Behavioral data and a segment-level survey explained the gap."
---

# Where attitudes and behavior diverge: 300,000 posts and panel surveys

<div class="meta" markdown="1">
**Where:** University of British Columbia, doctoral research with Kristin Laurin · **Published:** [Psychological Science, 2024](https://doi.org/10.1177/09567976241258149) and [Psychological Science, 2021](https://doi.org/10.1177/09567976211011969) · **Methods:** API data collection, human coding and NLP classification, regression with controls, sentiment analysis, survey experiment with behaviorally defined segments · **n:** hundreds of thousands of posts; 16 survey studies with about 4,200 participants; a 323-person segment study
</div>

## The question

In 16 studies with about 4,200 U.S. and Canadian participants, almost everyone, liberals and conservatives alike, said they liked members of their own side who heard out the other side. Open-minded targets read as tolerant; closed-minded ones read as loyal. Openness only lost when the ideas being entertained seemed immoral or stupid. That became my first paper (Psychological Science, 2021).

Social media looks like the opposite. Was the survey wrong, or the feed?

## Behavioral data first

Using Python and the platform API, I collected hundreds of thousands of U.S. Senators' posts. Senators are a good base: all 100 post about politics, which generalizes better than presidents or governors. Research assistants and I hand-coded more than 6,000 posts as open or closed to engaging with opponents, then trained a classifier to code the rest; the results held both ways.

Closed-minded posts earned two to four times the likes and shares of open-minded ones, controlling for follower counts, party, and year. Sentiment analyses showed closed posts were more impolite, negative, and moralized, but those differences did not statistically account for their popularity.

## Then the people

Two explanations fit: the people who engage with politicians' posts are not most people, or most people express different preferences online than they do in surveys.

I recruited 323 U.S. adults: 156 "activists" who frequently interact with politicians' posts (about 6% of adults, with more extreme views) and 167 lurkers who rarely do. Everyone saw ten real senator posts, half open and half closed, and reported what they preferred and what they would like and share.

Both explanations were true. Activists preferred closed posts and would amplify them. Lurkers preferred open posts but said they would share closed ones, betraying their own preference to fit the norm. A small group sets a divisive norm, and the majority follows it.

<!-- Optional: add a figure from the 2024 paper here, e.g. ![caption](/assets/img/attitudes-fig.png). You hold author rights to the accepted-manuscript figures; check SAGE's reuse terms for the typeset version. -->

## What it means for products

Engagement is a funhouse mirror of public opinion when a small, unrepresentative group produces most of it. Recommendations I have made to journalists and to researchers at platforms since the paper came out:

- Show view counts next to likes and shares, so engagement is read against reach.
- Make likes private, so people feel free to express a minority view.
- Rank constructive content by positive feedback relative to views, not raw volume, and surface the people who post it.
- Bring lurkers into engagement deliberately, including when prioritizing sign-ups.

## Methods, for the quant reader

API collection in Python; a hand-coded training set with inter-rater checks; NLP classification validated against human codes; regression with senator-level controls; sentiment analysis as a competing explanation; and a survey experiment whose segments were defined by behavior (self-reported engagement frequency), not demographics.
