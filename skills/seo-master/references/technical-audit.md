# Technical SEO Audit

Covers crawlability, indexability, and rendering. Use for "technical SEO", "crawl issues", "robots.txt", "Core Web Vitals", "site speed", "redirects", "migration".

## The 9 categories

1. **Crawlability**: robots.txt rules, crawl budget, blocked resources (CSS/JS must not be blocked), orphan pages, redirect chains and loops, broken internal links.
2. **Indexability**: `noindex` tags, canonical correctness, parameter handling, pagination, soft 404s, index bloat (thin/duplicate URLs in the index).
3. **Security**: HTTPS everywhere, HSTS, mixed content, valid certificate, security headers (CSP, X-Content-Type-Options, Referrer-Policy).
4. **URL structure**: short, readable, lowercase, hyphenated, no session IDs, logical hierarchy, consistent trailing-slash policy.
5. **Mobile**: responsive, viewport set, tap targets, no horizontal scroll, parity of content between mobile and desktop (mobile-first indexing).
6. **Core Web Vitals**: LCP (≤2.5s good), INP (≤200ms good), CLS (≤0.1 good). Use INP, never FID. Prefer field data (CrUX) over lab when available.
7. **Structured data**: presence and validity (hand to `schema.md` for depth).
8. **JavaScript rendering**: does critical content render without JS? Check rendered vs raw HTML. Flag client-only content that crawlers may miss.
9. **IndexNow / crawl efficiency**: XML sitemap freshness, lastmod accuracy, IndexNow support for fast recrawl on supported engines.

## Core Web Vitals thresholds

| Metric | Good | Needs work | Poor |
|---|---|---|---|
| LCP | ≤2.5s | 2.5-4.0s | >4.0s |
| INP | ≤200ms | 200-500ms | >500ms |
| CLS | ≤0.1 | 0.1-0.25 | >0.25 |

Common LCP fixes: optimize the hero image (format, size, preload), reduce render-blocking CSS/JS, server response time. INP: break up long tasks, reduce main-thread work, defer non-critical JS. CLS: set dimensions on images/embeds, reserve space for ads, avoid late-injected content.

## robots.txt quick reference

- One `User-agent` block per agent; `Disallow:` (empty) allows all; `Disallow: /` blocks all.
- Don't block CSS/JS needed for rendering.
- `robots.txt` controls crawling, not indexing. To keep a page out of the index use `noindex` (and don't also block it in robots.txt, or the crawler can't see the noindex).
- Reference the XML sitemap with a `Sitemap:` line.

## LLM / AI-crawler handling

AI engines crawl too. Decide policy deliberately:

- Common AI agents: GPTBot, OAI-SearchBot, ClaudeBot, anthropic-ai, PerplexityBot, Google-Extended (controls Gemini/Vertex training and AI Overview use), CCBot (Common Crawl).
- Blocking `Google-Extended` can reduce AI Overview visibility; weigh that against training-data concerns.
- `llms.txt` (root-level) is an emerging convention to point AI engines at your most citable content. Add one for sites that want AI visibility.
- For GEO, you generally want AI crawlers *allowed* on the content you want cited.

## Redirects and migrations

- Use 301 for permanent moves, 302 only for genuinely temporary ones.
- One hop where possible; chains dilute and slow.
- On migration: map every old URL to its best new equivalent (not a blanket redirect to the homepage), preserve URL structure where you can, update internal links and the sitemap, keep the old XML sitemap live briefly to speed recrawl, monitor GSC coverage and 404s after launch.

## E-commerce platform patterns

Watch for faceted-navigation index bloat (filter URLs), duplicate product URLs across categories (canonical to one), out-of-stock handling (keep indexable if returning, 404/410 if gone), and thin category pages.

## Output

Group findings by category, mark each Critical/High/Medium/Low, give the fix and the reason. Lead with anything that blocks indexing.
