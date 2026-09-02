---
title: Dashboard Infrastructure
summary: The full-stack system behind every dashboard on this site, self-managed end to end.
stats:
  - figure: "4"
    label: layers — React frontend, R API, SQLite, Nginx
  - figure: "2nd"
    label: generation architecture, migrated from an earlier Shiny Server setup
stack: "React · Vite · R Plumber · SQLite · Nginx · Docker Compose · DigitalOcean"
---

## Why it exists

Dashboards for HP and coaching staff are only useful if they're fast, reliable, and easy to extend as new questions come up mid-season. That meant treating this as real infrastructure rather than a one-off analysis script — a proper pipeline, a real API layer, and a deployment that doesn't need a laptop running to stay online.

## How it's built

- **Frontend** — React and Vite, with a locked colour system applied consistently across every chart type, so a metric means the same thing visually wherever it appears.
- **API layer** — an R Plumber API sitting between the frontend and the database, so the same analytical code that runs the underlying models also serves the dashboards.
- **Data** — Catapult GPS data and Champion Data (chain and possession data) synced via cron into a shared SQLite database.
- **Hosting** — Docker Compose and an Nginx reverse proxy on a self-managed DigitalOcean VM.

## Why it changed

The system started as R Shiny apps self-hosted on a droplet with basic auth — good for getting early tools like a live GPS training dashboard and an ACWR planner in front of staff quickly. As the number of dashboards and the complexity of the interactions grew, the Shiny architecture became a bottleneck, so the frontend and backend were split apart: React handles the interface, Plumber handles the analysis and data access. That separation is what makes it possible to add a new dashboard — like the [Match Report Dashboard]({{ '/projects/match-reports/' | relative_url }}) — without touching the others.

## Documentation

The project vault is set up with MCP integration and a master context file, plus a per-page context template for each dashboard — so picking a project back up after a break doesn't mean re-deriving the design decisions from scratch.
