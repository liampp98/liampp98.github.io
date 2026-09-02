---
title: AI Briefing System
summary: A structured R briefing object, piped through the Claude API, into a Quarto PDF ready for the HP meeting.
stats:
  - figure: "4"
    label: sections — Highlights, Risks, Key Questions, Suggested Investigations
stack: "R · Claude API · Quarto"
---

## The gap it fills

Every dashboard on this site answers a question once someone knows to ask it. Before an HP meeting, the more useful thing is often the reverse — what should we be asking about this week, based on what the data actually shows? That's a synthesis problem, not a display problem.

## How it works

A structured briefing object is assembled in R from the week's data across the monitoring and match-report systems, then passed through the Claude API. The output is rendered as a Quarto PDF with four sections: Highlights, Risks, Key Questions, and Suggested Investigations — written to be read in the five minutes before a meeting starts, not as a replacement for the dashboards themselves.

## Why it's structured this way

The brief doesn't try to hand HP staff conclusions. In line with the same principle behind every other system here — practitioner utility over the appearance of certainty — it's built to surface the right question, not assert a definitive answer that the underlying data doesn't actually support.
