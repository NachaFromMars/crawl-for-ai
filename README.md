# crawl-for-ai — Full-page web scraping with JavaScript rendering

> Scrapes any web page — including JavaScript-heavy SPAs — via a local Crawl4AI instance. Faster and more accurate than cloud scrapers for complex pages, with unlimited local usage.

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blueviolet)](https://github.com/NachaFromMars)

## Overview
crawl-for-ai connects to a local Crawl4AI instance to extract full page content with JavaScript rendering. It exposes two endpoints — a clean proxy output and a full-data direct output — and a Node.js script wrapper for quick use. Because it runs locally, there are no rate limits and no per-request costs. It outperforms simpler fetch-based scrapers on JS-rendered dashboards, SPAs, and dynamic content.

## Features
- **Proxy endpoint** (port 11234) — clean `[{page_content, metadata}]` output
- **Direct endpoint** (port 11235) — full `{results:[{markdown, html, links, media, ...}]}` output
- **Script** — `node scripts/crawl4ai.js "url"` + `--json` for raw response
- **JS rendering** — handles React, Vue, Angular SPAs
- **Unlimited** — local instance, no API quotas

## Usage / Quick Start
```bash
# Set required env var
export CRAWL4AI_URL="http://localhost:11235"

# Scrape a page
node scripts/crawl4ai.js "https://example.com"
node scripts/crawl4ai.js "https://example.com" --json
```

## Trigger Keywords (OpenClaw)
crawl page, scrape website, fetch full page content, extract with JS rendering

## Related Skills
- [ddg-web-search](https://github.com/NachaFromMars/ddg-web-search) — lightweight search without a local instance
- [playwright-scraper-skill](https://github.com/NachaFromMars/playwright-scraper-skill) — browser-based scraping alternative

---
Part of the [NachaFromMars](https://github.com/NachaFromMars) OpenClaw skill ecosystem.
