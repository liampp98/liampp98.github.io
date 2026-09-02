---
title: Load Monitoring Dashboard
summary: From a passive trend display into an active, target-based tracker for training load.
stats:
  - figure: "3"
    label: flag types — clawback in progress, persistent drift, undertrain risk
  - figure: "1"
    label: adaptive clawback formula, applied per athlete
stack: "R · Plumber API · React/Vite · SQLite"
---

## The problem

The original Weekly Loads page showed trend lines — useful for a retrospective look, but it didn't tell HP staff who needed attention *this week*, or what to do about it. Every read required someone to manually compare a player's load against their plan and make a judgement call.

## What changed

The page now works as an active tracker rather than a passive display:

- **A squad watchlist**, sorted by attention needed rather than alphabetically or by position — the players furthest off plan surface first.
- **An adaptive clawback formula**, individualised per athlete, that recalculates how a player's remaining sessions should be adjusted after a missed or reduced load, rather than leaving that judgement to manual review.
- **Three flag types** — clawback in progress, persistent drift, and undertrain risk — replacing a single generic "at risk" flag with something that tells a practitioner *what kind* of problem they're looking at before they open the page.

Season plan targets are read directly by the R pipeline rather than entered through the UI, so the numbers driving the dashboard stay in sync with the actual season plan rather than a separately maintained copy.

## What it's built on

The page sits on the same R Plumber API and SQLite backend as the rest of the dashboard suite — see [Dashboard Infrastructure]({{ '/projects/infrastructure/' | relative_url }}) for how the pipeline and hosting fit together.

## Where it's going

The next iteration folds in return-to-performance tracking: a home view showing squad availability status (available for selection vs. rehab), individual rehab plans with protocols and planned session dates, and tighter integration with testing and ACWR data — work that currently lives in a separate spreadsheet the rehab team maintains by hand.
