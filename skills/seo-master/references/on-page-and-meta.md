# On-Page & Meta Optimization

Single-page audits and the title/meta/heading/link/image layer. Use for "audit this page", "check page SEO", "optimize meta tags", "title tag", "meta description".

## Single-page audit checklist

**Title tag**: one per page, primary keyword near the front, under ~60 chars / ~580px, unique across the site, compelling not just descriptive.

**Meta description**: under ~155 chars, includes the keyword and a reason to click, unique. Not a ranking factor directly, but drives CTR which matters.

**Headings**: exactly one H1, reflecting the page's primary intent. Logical H2/H3 nesting (no skipped levels). H2s phrased as the questions/queries people actually search.

**Content fit**: does the page match the dominant intent for its target query? (Informational, commercial, transactional, navigational.) Mismatched intent is the most common reason a well-built page doesn't rank.

**Internal links**: descriptive anchor text (not "click here"), links to relevant deeper pages, no orphaning. Hand to `backlinks-and-entities.md` for site-wide architecture.

**Images**: descriptive alt text, compressed, modern format (WebP/AVIF), explicit width/height (CLS), lazy-load below the fold, descriptive filenames.

**URL**: short, readable, keyword-relevant, hyphenated.

**Above the fold**: is the page's promise answered immediately? (Also a GEO win; see `geo-citation-methods.md`.)

## Scoring rubric (per page)

Score each area 0-100 and roll up:

| Area | Weight |
|---|---|
| Title & meta | 20% |
| Intent match & content depth | 30% |
| Heading structure | 15% |
| Internal linking | 15% |
| Images & media | 10% |
| URL & technical basics | 10% |

## Title formulas

- **Listicle:** `[Number] [Adjective] [Keyword] for [Audience] ([Year])`
- **How-to:** `How to [Outcome] in [Timeframe/Steps]`
- **Comparison:** `[A] vs [B]: Which [Category] for [Use case]?`
- **Commercial:** `Best [Keyword] for [Use case] in [Year]`
- **Definition:** `What Is [Keyword]? [Plain-English angle]`

Keep the keyword early. Front-load the distinctive word. Avoid stacking adjectives.

## Meta description formulas

- Problem + promise: state the reader's problem, then what the page delivers.
- Include a soft CTA verb (compare, learn, see, get) without being spammy.
- Match the searcher's wording where natural.

## Open Graph & Twitter cards

Minimum set for clean sharing:

```html
<meta property="og:title" content="...">
<meta property="og:description" content="...">
<meta property="og:image" content="https://.../image-1200x630.jpg">
<meta property="og:url" content="https://...">
<meta property="og:type" content="article">
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="...">
<meta name="twitter:description" content="...">
<meta name="twitter:image" content="https://.../image-1200x630.jpg">
```

OG image: 1200x630, under ~1MB, text legible at thumbnail size.

## CTR test variants

When optimizing for clicks, produce 2-3 title/description variants per page with different angles (curiosity, specificity/number, benefit) so the user can A/B test. Label what each variant is testing.

## Bulk / site-wide

For 5+ pages, build a table: URL, current title, issue, recommended title, current meta, recommended meta, priority. Cluster by issue type so fixes can be batched.
