---
title: Match Report Dashboard
summary: A coach-facing reporting system built on one rule — every metric reflects match performance, not load.
stats:
  - figure: "5"
    label: sections auto-drafted weekly — Game Time, Work Rate, Athlete Analysis, Possession, Situational Intensity
  - figure: "1"
    label: core intensity language across every page — work rate in metres per minute
stack: "R · Champion Data · Obsidian · Email"
---

## The distinction that shaped it

The load monitoring dashboard exists to protect athletes from overload. This one exists for a different audience with a different question: coaches want to know what happened on the field, not how tired a player is. Keeping those two concerns in separate systems, rather than one dashboard trying to serve both audiences, made both of them sharper.

## The weekly workflow

Each week, a "Significant Mentions" draft is auto-generated across five sections — Game Time, Work Rate, Athlete Analysis, Possession Analysis, and Situational Intensity — then personalised in Obsidian before going out as a coach-facing email. Work rate (metres per minute, using time on ground as the denominator) is the consistent language across every page, so a coach doesn't need to re-learn the metric each time they open a different view.

## Pages built

- **Skills Drill Position Profile** — Run Work Rate vs. VHS Work Rate scatter with position-group reference zones and drift arrows, plus a per-drill table benchmarked against historical mean ±1.5 SD
- **Rotation Analysis** — an on-ground/bench swimlane shaded by work rate, alongside an exposure-vs-work-rate scatter
- **Situational Intensity** — reactive work rate in the 5–8 second window after a Champion Data chain-start trigger (centre bounce, turnover, intercept mark), benchmarked against the team's season average for that situation type

## What's next

An AFL Match Momentum stat, modelled conceptually on Opta's approach, is in early design — a natural extension of the existing chain-outcome model and the Situational Intensity infrastructure already in place.
