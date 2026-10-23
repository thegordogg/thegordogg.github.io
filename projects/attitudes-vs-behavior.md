---
title: "Where attitudes and behavior diverge: 300,000 posts and panel surveys"
description: "Doctoral research published in Psychological Science (2024): most people say they like political open-mindedness, but dismissive posts win online. Behavioral data and a segment-level survey explained the gap."
---

# Where attitudes and behavior diverge: 300,000 posts and panel surveys

<div class="meta" markdown="1">
**Where:** University of British Columbia, doctoral research with Kristin Laurin · **Published:** [Psychological Science, 2024](https://doi.org/10.1177/09567976241258149) and [Psychological Science, 2021](https://doi.org/10.1177/09567976211011969) · **Methods:** API data collection, human coding and NLP classification, regression with controls, sentiment analysis, survey experiment with behaviorally defined segments · **n:** hundreds of thousands of posts; 16 survey studies with about 4,200 participants; a 323-person segment study
</div>

## The question

In 2017, in my first meeting with my PhD advisor, I asked whether partisans would praise someone on their own side who tried to understand the other side. She predicted no. Sixteen studies and about 4,200 U.S. and Canadian participants later, the answer was a clear yes. Almost everyone, liberals and conservatives alike, liked members of their own side who heard out their opponents. Open-minded targets read as tolerant, closed-minded ones as loyal, and openness only lost when the ideas being entertained seemed immoral or stupid. That became my first paper (Psychological Science, 2021).

Social media looks like the opposite of that finding. So was the survey wrong, or was the feed?

## Behavioral data first

I went to the behavior first. Using Python and the platform API, I collected hundreds of thousands of U.S. Senators' posts. Senators are a good base: all 100 of them post about politics, which generalizes better than a handful of presidents or governors. My research assistants and I hand-coded more than 6,000 posts as engaging with opponents or dismissing them, then I trained a classifier to code the rest, and the results held both ways.

Dismissing posts earned two to four times the likes and shares of engaging ones, controlling for follower counts, party, and year. Sentiment analyses showed the dismissing posts were more impolite, negative, and moralized, but those differences did not statistically account for their popularity.

![Figure 2 from the paper: raw like and retweet counts for senators' engaging, dismissing, and neither tweets in Studies 1a and 1b. Dismissing tweets earned several times the engagement of engaging tweets.](/assets/img/attitudes-fig2-engagement.png)
*Figure 2 from the paper. Dismissing posts out-earned engaging ones on likes and retweets in both studies.*
{: .caption}

## Then the people

Two explanations fit. Either the people who engage with politicians' posts are not most people, or most people express different preferences online than they do in surveys.

First I checked that the survey preference wasn't an artifact of the medium. When people rated the same posts as if they had appeared offline or on Twitter, and as if they came from a senator or from an ordinary citizen, they still preferred the engaging posts in nearly every condition. They also rated engaging posts as more tolerant, cooperative, rational, legitimizing, and open to change. The preference was real; something else was producing the engagement.

![Figure 5 from the paper: warmth toward the senator for engaging versus dismissing tweets, by communicator role (senator or citizen) and medium (offline or Twitter), across Studies 2a and 2b.](/assets/img/attitudes-fig5-warmth.png)
*Figure 5. The preference for engaging posts held across medium and messenger.*
{: .caption}

![Figure 8 from the paper: attribute ratings for engaging versus dismissing tweets. Engaging tweets rated higher on tolerant, cooperative, rational, legitimizing, and open to changing.](/assets/img/attitudes-fig8-attributes.png)
*Figure 8. What people saw in each kind of post.*
{: .caption}

So I recruited 323 U.S. adults: 156 frequent reactors who regularly like and share politicians' posts (about 6% of adults) and 167 who rarely do. Everyone saw ten real senator posts, half engaging and half dismissing, and told me what they approved of, how they felt about the senator, and what they would like and share.

Both explanations were true. Frequent reactors preferred dismissing posts on every measure. Everyone else approved of the engaging posts, but their feelings toward the senator and their intent to like and share tilted slightly toward the dismissing ones anyway. And the frequent reactors were a different population: more partisan, more extreme, more interested in status for their party. A small group sets a divisive norm, and the majority follows it.

![Figure 6 from the paper: preference for engaging over dismissing tweets among frequent reactors versus everyone else, on approval, feelings toward the senator, and intent to like or retweet. Frequent reactors prefer dismissing on all three; everyone else approves of engaging but tilts toward dismissing on feelings and intent.](/assets/img/attitudes-fig6-preference.png)
*Figure 6. Frequent reactors prefer dismissing posts; everyone else approves of engaging posts and amplifies dismissing ones anyway.*
{: .caption}

![Figure 7 from the paper: standardized differences between frequent reactors and everyone else on theorized variables (preference for dismissing, partisan extremity, desire for party status, affective polarization, opposition to compromise) and extraneous variables.](/assets/img/attitudes-fig7-reactors.png)
*Figure 7. Who the frequent reactors are.*
{: .caption}

## What it means for products

Engagement is a funhouse mirror of public opinion when a small, unrepresentative group produces most of it. Since the paper came out, journalists and researchers at platforms have asked what I would change, and my answers are the same each time. Show view counts next to likes and shares, so engagement is read against reach. Make likes private, so people feel free to express a minority view. Rank constructive content by positive feedback relative to views rather than raw volume, and surface the people who post it. And bring the quiet majority into engagement deliberately, including when prioritizing sign-ups.

## Methods, for the quant reader

API collection in Python; a hand-coded training set with inter-rater checks; NLP classification validated against the human codes; regression with senator-level controls; sentiment analysis tested as a competing explanation; and a survey experiment whose segments were defined by behavior (self-reported engagement frequency) rather than demographics. Figures are from Heltzel & Laurin (2024), *Psychological Science*.
