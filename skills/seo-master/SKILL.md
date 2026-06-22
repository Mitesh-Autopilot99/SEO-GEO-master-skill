---
name: seo-master
description: "End-to-end SEO and GEO (Generative Engine Optimization) for any website or business type. One skill for the whole workflow: full-site and single-page audits, technical SEO (crawlability, indexability, Core Web Vitals with INP), on-page and meta optimization, schema/structured data, internal linking, keyword research, topic clustering, SERP and competitor analysis, content gaps, backlink profiles, entity/Knowledge Graph optimization, content briefs and writing, content refreshes, fact-checking, and AI-search visibility for AI Overviews, ChatGPT, Perplexity, Gemini and Claude. Use this skill whenever the user mentions SEO, GEO, AEO, audits, schema, Core Web Vitals, sitemaps, E-E-A-T, AI Overviews, keyword research, backlinks, internal links, meta tags, content briefs, SEO writing, content decay, competitor or SERP analysis, AI citations, or wants any website or page made more visible in search or in AI answers, even if they don't name a specific technique."
license: MIT
metadata:
  author: consolidated by Mitesh Thaker
  category: seo
  version: 1.0.0
  consolidates: "Pack A (aaron-he-zhu suite), Pack B (AgriciDaniel seo-* suite), Pack C (xSeek suite)"
---

# SEO Master: Unified SEO + GEO Workflow

This skill replaces three overlapping SEO/GEO packs with one router. It covers the full lifecycle: research and planning, auditing, on-page and technical fixes, structured data, off-page and competitive work, content production, and AI-search (GEO) visibility.

**How to use it:** identify the task from the routing table below, read the one or two reference modules named for that task, then execute. Do not load every module at once. Most tasks need a single module plus the global standards in this file.

## Global standards (apply to every task)

These are non-negotiable and override anything in a reference module that conflicts:

- **No em-dashes.** Never use `—`, en-dashes used as punctuation ` – `, or `--` as a dash in any deliverable. Split into two sentences, or use a comma, colon, or parentheses. Before delivering written content, grep for `—`, `–`, and `--`; expect zero hits. (Full rationale in `references/writing-rules.md`.)
- **Core Web Vitals use INP, never FID.** FID was retired. The three CWV are LCP, INP, CLS.
- **Never recommend HowTo schema.** Deprecated by Google in September 2023.
- **FAQ schema, post-August 2023:** Google rich results only show for government and healthcare sites. Existing FAQPage on a commercial site = flag as Info priority (not Critical), noting AI/LLM citation benefit. Adding new FAQPage = not recommended for Google rich-result benefit, but still useful for AI citation.
- **Thin-content and scale gates:** warn at 30+ near-identical location/programmatic pages (enforce 60%+ unique content), hard stop at 50+ (require user justification). Detail in `references/strategy-and-planning.md`.
- **Evidence over assertion.** Don't invent metrics, rankings, or traffic numbers. If you don't have data, say what you'd measure and how. When a claim needs a figure you don't have, describe what actually happens instead.
- **Keyword stuffing is counterproductive for AI search.** Use the primary keyword 2-3 times max; rely on semantic variation. See `references/geo-citation-methods.md`.

## Routing table

| The user wants to... | Read this module | Notes |
|---|---|---|
| Full website audit / health check | `references/full-audit-playbook.md` | Orchestrates the other modules; produces a 0-100 health score + prioritized action plan |
| Audit / analyze a single page | `references/on-page-and-meta.md` | Titles, headings, links, images, content fit |
| Optimize title tags, meta descriptions, OG/Twitter cards | `references/on-page-and-meta.md` | CTR variants and code templates included |
| Technical SEO (crawl, index, robots, redirects, CWV, security, JS, migration) | `references/technical-audit.md` | 9 categories + LLM-crawler handling |
| Generate / detect / validate schema (JSON-LD) | `references/schema.md` | Decision tree + templates + global schema rules |
| Assess content quality / E-E-A-T / publish-readiness | `references/content-quality-eeat.md` | CORE-EEAT scoring with veto checks |
| Keyword research / intent mapping / prioritization | `references/keyword-clusters-serp.md` | Volume, difficulty, intent, clusters |
| Topic clusters / pillar-and-spoke / content architecture | `references/keyword-clusters-serp.md` | SERP-overlap clustering method |
| Analyze the SERP for a query | `references/keyword-clusters-serp.md` | Features, intent, AI Overview presence |
| Competitor analysis / content gaps / comparison pages | `references/competitor-and-gaps.md` | Keyword, content, link, AI-citation gaps |
| Backlink profile analysis | `references/backlinks-and-entities.md` | Free sources (Moz, Bing, Common Crawl) + toxicity |
| Internal linking / site architecture / orphan pages | `references/backlinks-and-entities.md` | Link-equity flow, anchor strategy |
| Entity / Knowledge Graph / Wikidata / sameAs | `references/backlinks-and-entities.md` | AI entity recognition signals |
| GEO: make content citable by AI engines | `references/geo-citation-methods.md` | The Princeton 9-method framework |
| GEO/AEO audit: how the brand appears in AI answers | `references/geo-citation-methods.md` + `references/content-quality-eeat.md` | Citability scoring, llms.txt, AI-crawler access |
| Write a content brief | `references/content-production.md` | Per-section word counts, outline, internal links |
| Write or generate an article / page | `references/content-production.md` + `references/writing-rules.md` + `references/geo-citation-methods.md` | Always apply writing rules + GEO methods together |
| Refresh / update decaying content | `references/content-production.md` | Decay signals + refresh templates |
| Fact-check content before publishing | `references/content-production.md` | Verify stats, claims, citations for E-E-A-T |
| Strategic SEO plan for a business | `references/strategy-and-planning.md` | Templates per business type |
| Programmatic SEO at scale | `references/strategy-and-planning.md` | Template engine, thin-content safeguards |
| Sitemap analysis or generation | `references/strategy-and-planning.md` | XML validation + generation |
| Find content / traffic opportunities | `references/strategy-and-planning.md` | Keyword gaps + competitor weaknesses |

If a request spans several rows (e.g. "audit my site and tell me what to write"), run the audit first, then hand its findings into the planning/content modules. The full-audit playbook describes these handoffs.

## How the writing modules combine

When producing any written content (article, page, brief), three modules work together and must all be applied:

1. `references/writing-rules.md`: the voice: simple words, short paragraphs, no banned phrases, zero em-dashes.
2. `references/geo-citation-methods.md`: the structure that gets cited by AI: answer-first sections, statistics, citations, quotes, FAQ.
3. `references/content-production.md`: the format for the specific deliverable (brief vs article vs refresh).

If the user has a brand voice/style guide, it outranks the generic writing rules where they conflict.

## Business-type detection

Several modules adapt to business type. Detect it from homepage signals:

- **SaaS**: pricing page, /features, /integrations, /docs, "free trial", "sign up"
- **Local service**: phone, address, service area, "serving [city]", Maps embed
- **E-commerce**: /products, /collections, /cart, "add to cart", product schema
- **Publisher**: /blog, /articles, author pages, article schema, publish dates
- **Agency**: /case-studies, /portfolio, "our work", client logos

State the detected type and adapt recommendations accordingly.

## Output conventions

- Lead deliverables with the answer or the single most important finding. No throat-clearing.
- For audits: Executive summary → findings by category → prioritized action plan (Critical → High → Medium → Low). Critical = blocks indexing or causes penalties; High = significant ranking impact, fix within a week; Medium = optimization, within a month; Low = backlog.
- Save substantial outputs to files (reports, briefs, articles) rather than burying them in chat.
- Offer a PDF or doc export when a report is the deliverable, but don't assume external API tooling is present.

## What this skill deliberately does not do

- It does not depend on any external SaaS platform, CLI, or proprietary API. Where the source packs called out paid tools (DataForSEO, Moz, Firecrawl, Google API credentials, or a vendor CLI), treat those as *optional enrichment*: use them only if the user confirms the integration is available, and otherwise fall back to free/manual methods named in the modules.
- It does not track live rankings, AI-citation counts, or bot visits over time. That requires a monitoring platform with stored history. If the user needs ongoing tracking, tell them this skill handles the analysis and production work, and a tracking platform is a separate dependency.

## Reference modules

- `references/full-audit-playbook.md`: orchestrated full-site audit: scoring weights, report structure, handoffs
- `references/technical-audit.md`: technical SEO across 9 categories, crawl config, LLM-crawler handling, migrations
- `references/on-page-and-meta.md`: single-page audit rubric, title/meta/OG formulas and templates
- `references/content-quality-eeat.md`: E-E-A-T and CORE-EEAT scoring, AI-citation readiness
- `references/schema.md`: schema decision tree, JSON-LD templates, validation, global schema rules
- `references/keyword-clusters-serp.md`: keyword research, intent taxonomy, topic clustering, SERP analysis
- `references/competitor-and-gaps.md`: competitor analysis, content-gap analysis, comparison pages
- `references/backlinks-and-entities.md`: backlink profiles, internal linking, entity/Knowledge Graph
- `references/strategy-and-planning.md`: SEO plans by business type, programmatic SEO, sitemaps, opportunities
- `references/content-production.md`: briefs, article generation, content refresh, fact-checking
- `references/geo-citation-methods.md`: the Princeton 9-method GEO framework (verbatim, high value)
- `references/writing-rules.md`: human-like writing rules and the em-dash ban (verbatim, high value)
