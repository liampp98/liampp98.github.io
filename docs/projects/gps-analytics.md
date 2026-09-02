---
title: Match Movement & Chain-Outcome Modelling
summary: A 13-script pipeline across 15 matches of 10Hz GPS data, built to find out what actually predicts scoring.
stats:
  - figure: "0.956"
    label: AUC on the chain-outcome logistic regression model
  - figure: "2"
    label: movement types found via clustering, not the usual six positional groups
stack: "R · 10Hz GPS (Catapult) · Champion Data"
---

## The question

Positional groups are usually treated as a given — six groups, six sets of expectations. Before building demand profiles or benchmarks on top of that assumption, it was worth testing whether the movement data actually supported it.

## The pipeline

A 13-script R pipeline covering:

- **WCS processing** — worst-case-scenario load windows across the full match set
- **Positional demands** — movement profiles by role
- **Possession analysis** — how movement patterns shift with and without the ball
- **Chain outcome prediction** — a logistic regression model reaching 0.956 AUC
- **Spatial visualisation** — GPS coordinate normalisation across different venues, so movement patterns are comparable ground to ground
- **Rotation optimisation** — fatigue onset modelling to inform bench timing

## What it found

Clustering the movement data directly, rather than assuming positional groups, surfaced two movement types rather than six — a meaningfully simpler picture of how players actually move than the standard positional breakdown suggests. On the scoring side, chain metres gained was the dominant factor in the outcome model, ahead of other candidate predictors.

## Where it feeds

The chain-outcome model underpins the [Match Report Dashboard]({{ '/projects/match-reports/' | relative_url }})'s coach-facing pages, and the fatigue onset modelling informs rotation guidance in the same system.
