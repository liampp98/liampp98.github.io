# Portfolio

Sport science / performance systems portfolio — AFLW high performance dashboards, GPS analytics, and infrastructure. Built to show the work, not just describe it.

**Live site:** add your GitHub Pages URL here once published (`https://<username>.github.io/<repo>/`)

## What's in this repo

- `docs/` — the portfolio site itself (Jekyll, served by GitHub Pages)
- `code-samples/` — standalone, rewritten code samples with synthetic data, each linked from the corresponding project page. These are illustrative extracts, not the working club codebases.

## Publishing this site

1. Push this repo to GitHub.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch," branch `main`, folder `/docs`.
4. Save. GitHub will build and publish the site — it takes a minute or two, and the URL appears at the top of the Pages settings once it's live.
5. Every push to `main` republishes automatically. No build step to run locally unless you want to preview changes first (see below).

## Previewing locally (optional)

Requires Ruby and Bundler.

```
cd docs
bundle init
bundle add jekyll
bundle exec jekyll serve
```

Then open `http://localhost:4000`.

## Adding a custom domain (optional)

1. Buy a domain from any registrar (Namecheap, Cloudflare, etc.) — roughly $15–20/year.
2. Add a file `docs/CNAME` containing just your domain, e.g. `liamsomething.com`.
3. At your registrar, point the domain's DNS at GitHub Pages (an `A` record set to GitHub's IPs, or a `CNAME` record to `<username>.github.io` for a subdomain).
4. Add the same domain in **Settings → Pages → Custom domain**. GitHub provisions HTTPS automatically once DNS resolves.

## Before publishing

- Replace every screenshot/GIF placeholder in `docs/assets/` with real (or genericised) visuals.
- Check with MFC on what's appropriate to show publicly — this site is written to describe systems and approach without exposing real player data, but it's worth a quick confirmation before it goes live.
- Fill in the `code-samples/` placeholders with real, rewritten scripts using synthetic data only — see each folder's README for what's needed.
- Update the GitHub link in `docs/_layouts/default.html` nav to point at this repo once it's public.
