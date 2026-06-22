# Strategy, Planning, Programmatic SEO & Sitemaps

Strategic planning, scale, and the structural plumbing. Use for "SEO plan", "SEO strategy", "content calendar", "programmatic SEO", "pages at scale", "sitemap", "content opportunities".

## Strategic SEO plan

Produce a plan adapted to business type (detect per SKILL.md). Structure:

1. **Goal & baseline**: what success looks like (traffic, rankings, leads, AI citations), and where the site is now.
2. **Audience & intent map**: who's searching, at what funnel stage, in what words.
3. **Keyword & cluster strategy**: pillars and spokes (hand to `keyword-clusters-serp.md`).
4. **Technical foundation**: what must be fixed first (hand to `technical-audit.md`).
5. **Content roadmap**: what to publish/refresh, in priority order, on a calendar.
6. **Off-page & entity**: link and entity-building priorities (hand to `backlinks-and-entities.md`).
7. **GEO layer**: how the plan also wins AI citations (hand to `geo-citation-methods.md`).
8. **Measurement**: what to track and how often.

### Business-type emphasis

- **SaaS**: feature/use-case/integration pages, comparison and alternatives pages, docs, free-tool linkable assets, bottom-funnel commercial terms.
- **Local service**: GBP optimization, location and service pages (genuinely unique), reviews, local citations, local schema.
- **E-commerce**: category page quality, product schema, faceted-nav control, review content, buying guides linking to categories.
- **Publisher**: topic authority via clusters, author E-E-A-T, freshness cadence, internal linking depth, news/article schema.
- **Agency**: case studies, service pages, industry pages, thought-leadership for entity/authority.

## Programmatic SEO (pages at scale)

Generate many pages from a data source (locations, products, combinations).

- **Template + data**: one template, structured data feeding unique values per page.
- **Unique value per page**: each page must answer a real query with genuinely different, useful content, not just a swapped variable.
- **Thin-content safeguards (hard gates):** warn at 30+ near-identical pages (enforce 60%+ unique content per page), hard stop at 50+ (require user justification). Pages that are just `[keyword] in [city]` with one word swapped are the failure mode.
- **Index management**: only let pages with real value into the index; noindex the rest to avoid index bloat.
- **Internal linking**: automate sensible cross-links (hub pages, related items), not a link dump.
- **URL pattern**: consistent, readable, scalable.

If the data can't support genuinely unique, useful pages at the requested scale, say so and recommend fewer, deeper pages.

## Sitemaps

- **Analyze:** valid XML, only canonical/indexable URLs (no noindex, no redirects, no 404s), accurate `lastmod`, under 50,000 URLs / 50MB per file (split with a sitemap index if larger), referenced in robots.txt and submitted to GSC/Bing.
- **Generate:** build from the live, indexable URL set; group logically (pages, posts, products) via a sitemap index; set honest `lastmod`. Optionally add image/video sitemaps where relevant.
- Common issues: orphaned URLs in the sitemap that aren't linked anywhere, non-canonical URLs included, stale lastmod, blocked URLs listed.

## Finding opportunities

Combine signals into a ranked opportunity list:
- Keyword gaps (from `competitor-and-gaps.md`).
- Pages ranking on page 2 that a refresh could push up (striking-distance).
- High-impression / low-CTR pages (title/meta fix; from `on-page-and-meta.md`).
- Decaying pages (refresh; from `content-production.md`).
- Queries triggering AI Overviews you're not cited in (from `geo-citation-methods.md`).

Rank by impact × achievability and present as a backlog with the recommended action per item.

## Output

A dated, prioritized plan or backlog. Tie every recommendation to the goal and name which module executes it.
