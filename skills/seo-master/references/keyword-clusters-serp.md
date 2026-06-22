# Keyword Research, Clusters & SERP Analysis

Keyword discovery and prioritization, topic-cluster architecture, and reading the SERP. Use for "find keywords", "keyword research", "topic cluster", "pillar page", "content architecture", "analyze the SERP".

## Keyword research workflow

1. **Seed** from the business, products, and the user's known terms.
2. **Expand** via related searches, People Also Ask, autocomplete, competitor terms, and any connected data the user has.
3. **Classify intent** for each (taxonomy below).
4. **Estimate** volume and difficulty. Use real data if connected; otherwise reason from SERP strength and label estimates as estimates.
5. **Prioritize** (framework below).
6. **Cluster** into topics that map to pages.

## Intent taxonomy

- **Informational**: "what/how/why...", guides, definitions. Top of funnel. Content: articles, explainers.
- **Commercial investigation**: "best", "vs", "review", "alternatives". Comparing options. Content: comparisons, listicles, buying guides.
- **Transactional**: "buy", "price", "discount", "near me". Ready to act. Content: product/category/service pages.
- **Navigational**: brand or specific page. Content: the page they want.

Match the page type to the dominant intent. Don't put a product page where the SERP is all guides.

## Prioritization framework

Score each keyword on:
- **Relevance** to what the site actually offers (highest weight).
- **Intent value** (transactional/commercial usually convert better; informational builds reach).
- **Opportunity** = volume × realistic chance to rank (low difficulty relative to the site's authority).
- **Effort** to produce a page that wins.

Prioritize high-relevance, achievable-difficulty terms with clear intent. A low-volume term you can win and convert beats a high-volume term you can't.

## Topic clusters (pillar-and-spoke)

- **Pillar**: broad page targeting the head term and the topic as a whole.
- **Spokes**: focused pages on subtopics/long-tail, each linking up to the pillar and to relevant siblings.
- Build the internal-link matrix so equity flows pillar↔spokes (see `backlinks-and-entities.md`).

### SERP-overlap clustering method

Group keywords by *actual SERP overlap*, not text similarity:
1. For each keyword, take the top ~10 ranking URLs.
2. Two keywords belong in the same cluster (= same page) if their results overlap by ~3+ shared URLs.
3. Keywords that share intent but don't overlap → separate pages.

This prevents building two pages that cannibalize each other, and reveals when one page can target several queries.

## SERP analysis

For a target query, read the live SERP and report:
- **Dominant intent**: what content type ranks (guides vs products vs tools).
- **SERP features present**: AI Overview, featured snippet, People Also Ask, image/video pack, local pack, shopping, knowledge panel, sitelinks.
- **Difficulty signals**: domain strength of top results, content depth, freshness.
- **Snippet opportunity**: is there a featured snippet to win, and in what format (paragraph, list, table)?
- **AI Overview presence**: if one shows, note what it cites; that's the GEO target (hand to `geo-citation-methods.md`).
- **Content angle gap**: what the top results all miss, which is your way in.

## Output

Keyword table (term, intent, volume/est, difficulty/est, priority, target page), the cluster map (pillar + spokes), and for SERP work a per-query readout with the recommended content type and snippet/AI-Overview play.
