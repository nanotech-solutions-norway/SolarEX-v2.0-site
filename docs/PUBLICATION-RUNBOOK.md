# SolarEX v2.0 Publication Runbook

## Objective
Publish the static SolarEX v2.0 site repository through GitHub Pages with the custom domain `www.solarex.no`.

## Repository
- Site repo: `nanotech-solutions-norway/SolarEX-v2.0-site`
- Content repo: `nanotech-solutions-norway/SolarEX-v2.0-content`

## What has already been prepared
- Static site pages uploaded on `main`
- `CNAME` file added for `www.solarex.no`
- GitHub Actions workflow added at `.github/workflows/deploy-pages.yml`
- `robots.txt` and `sitemap.xml` already present

## Manual GitHub steps still required
1. Open repository settings for `SolarEX-v2.0-site`.
2. Open **Pages**.
3. Set **Build and deployment** source to **GitHub Actions**.
4. Confirm Actions are allowed for the repository if prompted.
5. Trigger the workflow by pushing a new commit or using **Run workflow**.
6. After first successful deployment, confirm the Pages URL is live.

## DNS / domain checks
1. Ensure `www.solarex.no` is pointed to GitHub Pages according to current GitHub Pages DNS guidance.
2. If apex `solarex.no` should also resolve, configure redirect or ALIAS/ANAME strategy according to DNS provider capabilities.
3. In GitHub Pages settings, verify the custom domain reads `www.solarex.no`.
4. Enable HTTPS after DNS validation succeeds.

## Smoke test checklist
- Homepage loads
- Header logo renders
- Version chip `v2.0` visible
- Quartz and Titan pages load
- Contact link opens `mail@solarex.no`
- `robots.txt` and `sitemap.xml` return successfully
- Mobile menu works
- No missing asset errors in browser console

## Current connector limitation
The current ChatGPT GitHub connector can commit files and workflows, but it does not expose repository Pages settings toggles. Those settings still need to be completed in GitHub UI.
