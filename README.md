# SEO-GEO Master Skill

A single Claude Skill that handles the full SEO and GEO (Generative Engine Optimization) workflow for any website or business type: audits, technical SEO, on-page and meta, schema, keyword research, topic clusters, competitor and content-gap analysis, backlinks and entities, content production, and AI-search visibility for AI Overviews, ChatGPT, Perplexity, Gemini and Claude.

It is one router skill (`SKILL.md`) plus 12 focused reference modules. You read the one or two modules a task needs instead of loading everything at once.

## What it does

- **Audits**: full-site health check with a 0-100 score, plus single-page audits.
- **Technical SEO**: crawlability, indexability, Core Web Vitals (LCP, INP, CLS), security, JS rendering, redirects, migrations.
- **On-page and meta**: titles, meta descriptions, headings, Open Graph and Twitter cards.
- **Schema**: JSON-LD decision tree, templates, and validation.
- **Research and strategy**: keyword research, intent mapping, topic clusters, SERP analysis, competitor and content-gap analysis, programmatic SEO, sitemaps.
- **Off-page**: backlink profiles, internal linking, entity and Knowledge Graph optimization.
- **Content**: briefs, article writing, content refreshes, fact-checking, E-E-A-T scoring.
- **GEO**: the Princeton 9-method framework for getting content cited by AI engines.

## Structure

```
skills/seo-master/
  SKILL.md
  references/
    full-audit-playbook.md
    technical-audit.md
    on-page-and-meta.md
    content-quality-eeat.md
    schema.md
    keyword-clusters-serp.md
    competitor-and-gaps.md
    backlinks-and-entities.md
    strategy-and-planning.md
    content-production.md
    geo-citation-methods.md
    writing-rules.md
```

## Install

**Option 1: copy the folder.** Copy the `seo-master` folder (the one containing `SKILL.md`) into your Claude skills directory:

- Claude Code: `~/.claude/skills/seo-master/`
- Cowork: your skills directory, or use the Skills settings to add it.

**Option 2: packaged skill.** Download the `seo-master.skill` file from the [Releases](https://github.com/Mitesh-Autopilot99/SEO-GEO-master-skill/releases) page and install it (in Cowork, use the "Save skill" button when the file is shared).

Once installed, the skill triggers whenever you mention SEO, GEO, AEO, audits, schema, Core Web Vitals, keyword research, backlinks, E-E-A-T, AI Overviews, content briefs, or ask to make a page more visible in search or AI answers.

## Design notes

- No external paid tools required. Where the source packs called for paid platforms (DataForSEO, Moz, Ahrefs, Firecrawl, and so on), those are optional enrichment only; the skill falls back to free and manual methods.
- The writing rules deliberately ban em-dashes and a list of AI-tell phrases, so generated content reads like a person wrote it.
- Core Web Vitals use INP, not the retired FID.

## License

MIT
