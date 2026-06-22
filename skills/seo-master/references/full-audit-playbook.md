# Full Website Audit Playbook

Orchestrates the other modules into one prioritized report with a 0-100 health score. Use for "audit my site", "full SEO check", "website health check".

## Process

1. **Fetch the homepage** and detect business type (see SKILL.md signals).
2. **Crawl** internal links, respecting robots.txt. Cap at ~500 pages. Follow redirects (max 3 hops), 30s timeout per page, ~5 concurrent, 1s delay. If you lack a crawler, analyze the pages the user provides and the homepage, and state the coverage limit.
3. **Run each category** using its module:
   - Technical → `technical-audit.md` (robots, sitemaps, canonicals, CWV/INP, security headers, JS rendering, redirects)
   - Content quality → `content-quality-eeat.md` (E-E-A-T, thin content, readability, AI-citation readiness)
   - On-page → `on-page-and-meta.md` (titles, meta, headings, internal links, images)
   - Schema → `schema.md` (detection, validation, opportunities)
   - AI search readiness → `geo-citation-methods.md` (citability, llms.txt, AI-crawler access, answer-first structure)
   - Off-page (if data available) → `backlinks-and-entities.md`
   - Strategy signals (blog/clusters) → `keyword-clusters-serp.md`
4. **Score** each category, weight, and aggregate into a 0-100 health score.
5. **Report** with a prioritized action plan.

## Scoring weights

| Category | Weight |
|---|---|
| Content Quality | 23% |
| Technical SEO | 22% |
| On-Page SEO | 20% |
| Schema / Structured Data | 10% |
| Performance (CWV) | 10% |
| AI Search Readiness | 10% |
| Images | 5% |

Score each category 0-100, multiply by weight, sum. State the inputs behind each category score so the number is defensible. If a category could not be measured (e.g. no field CWV data), say so and note it lowers confidence rather than guessing.

## Report structure

```
# SEO Health Audit: [domain]
## Executive Summary
- Overall health score (0-100) and what it means
- Business type detected
- Top 5 critical issues
- Top 5 quick wins
## Technical SEO
## Content Quality (E-E-A-T)
## On-Page SEO
## Schema & Structured Data
## Performance (LCP / INP / CLS)
## Images
## AI Search Readiness (GEO)
## Prioritized Action Plan
```

## Priority definitions

- **Critical**: blocks indexing or risks a penalty. Fix immediately.
- **High**: significant ranking impact. Fix within a week.
- **Medium**: optimization opportunity. Fix within a month.
- **Low**: nice to have. Backlog.

Each action item: what, why it matters, expected impact, rough effort (S/M/L).

## Handoffs

- Audit surfaces a content gap → hand into `keyword-clusters-serp.md` and `competitor-and-gaps.md` to plan what to write.
- Audit surfaces thin or decaying pages → hand into `content-production.md` (refresh) or `content-quality-eeat.md` (rewrite-or-prune decision).
- Audit surfaces weak AI visibility → hand into `geo-citation-methods.md` to rework the highest-value pages first.

## Error handling

| Scenario | Action |
|---|---|
| URL unreachable | Report the error. Don't guess site content. Ask the user to verify the URL. |
| robots.txt blocks crawling | Report blocked paths, analyze accessible pages only, note the limitation. |
| Rate limited (429) | Back off, reduce concurrency, report partial results. |
| Very large site (500+ pages) | Cap the crawl, report findings for crawled pages, estimate total scope. |

## Optional enrichment

If, and only if, the user confirms these are available: Google Search Console / GA4 / CrUX for field data, DataForSEO or Moz for live SERP and backlink data, Firecrawl for full-site mapping. Otherwise use free/manual methods. Never assume credentials exist.
