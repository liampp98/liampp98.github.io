---
title: Home
---
<section class="hero">
  <h1>Building the systems high performance teams actually use.</h1>
  <p class="lede">I'm Liam, a sport scientist working across AFLW high performance — athlete monitoring, GPS analytics, and the dashboard infrastructure that turns raw training data into decisions coaches and HP staff can act on.</p>

  <div class="hero-stats">
    <div class="stat">
      <span class="stat-figure">13</span>
      <span class="stat-label">script GPS pipeline, 15 matches of 10Hz data</span>
    </div>
    <div class="stat">
      <span class="stat-figure">0.956</span>
      <span class="stat-label">AUC on the chain-outcome prediction model</span>
    </div>
    <div class="stat">
      <span class="stat-figure">3</span>
      <span class="stat-label">dashboards in live use by HP and coaching staff</span>
    </div>
  </div>
</section>

<section class="work" id="work">
  <h2>Selected work</h2>

  <div class="work-item">
    <div>
      <span class="tag">Athlete monitoring</span>
      <h3><a href="{{ '/projects/load-dashboard/' | relative_url }}">Load Monitoring Dashboard</a></h3>
    </div>
    <p>Redesigned the Weekly Loads page from a passive trend display into an active, target-based tracker — with an adaptive clawback formula, a squad watchlist, and a three-state flag system for athletes drifting off plan.</p>
  </div>

  <div class="work-item">
    <div>
      <span class="tag">Infrastructure</span>
      <h3><a href="{{ '/projects/infrastructure/' | relative_url }}">Dashboard Infrastructure</a></h3>
    </div>
    <p>The full-stack system behind every dashboard on this site — React/Vite, an R Plumber API, SQLite, and Docker on a self-managed VM, migrated from an earlier Shiny Server setup as needs outgrew it.</p>
  </div>

  <div class="work-item">
    <div>
      <span class="tag">GPS analytics</span>
      <h3><a href="{{ '/projects/gps-analytics/' | relative_url }}">Match Movement & Chain-Outcome Modelling</a></h3>
    </div>
    <p>A 13-script analysis pipeline across 15 matches of 10Hz GPS data — positional demands, possession analysis, and a chain-outcome model reaching 0.956 AUC.</p>
  </div>

  <div class="work-item">
    <div>
      <span class="tag">Coach-facing</span>
      <h3><a href="{{ '/projects/match-reports/' | relative_url }}">Match Report Dashboard</a></h3>
    </div>
    <p>A coach-facing reporting system built on one rule: every metric reflects effect on match performance, not load or fatigue. Weekly auto-generated report drafts, rotation analysis, and skills-drill position profiling.</p>
  </div>

  <div class="work-item">
    <div>
      <span class="tag">Automated reporting</span>
      <h3><a href="{{ '/projects/ai-briefing/' | relative_url }}">AI Briefing System</a></h3>
    </div>
    <p>A structured R briefing object passed through the Claude API, generating a Quarto PDF covering highlights, risks, key questions, and suggested investigations ahead of each HP meeting.</p>
  </div>
</section>

<section class="about" id="about">
  <h2>About</h2>
  <p>My work runs on one principle: athlete outcomes first, practitioner utility second, technical rigour third. A dashboard that raises the right question for a coach is worth more than one that claims a definitive answer nobody asked for. Everything on this site was built with that in mind.</p>
</section>
