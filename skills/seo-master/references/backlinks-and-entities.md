# Backlinks, Internal Linking & Entity Optimization

Off-page authority, site architecture, and entity signals. Use for "backlinks", "link profile", "referring domains", "toxic links", "internal linking", "orphan pages", "entity", "Knowledge Graph", "Wikidata", "sameAs".

## Backlink profile analysis

Free/low-cost sources first; paid only if the user confirms access.

- **Free signals:** Common Crawl (domain-level link data), Bing Webmaster Tools, Google Search Console (the site's own inbound links), Moz free tier (DA/PA), manual SERP checks.
- **Paid enrichment (optional):** DataForSEO, Ahrefs, Semrush, Majestic. Use only if available.

Report on:
- **Referring domains**: count and quality (relevance + authority), trend over time if data allows.
- **Anchor text distribution**: healthy mix of branded, naked URL, and partial-match; over-optimized exact-match anchors are a risk signal.
- **Toxic links**: spammy, irrelevant, or paid-link-network domains. Most should be ignored (Google usually discounts them); only consider disavow for a clear, harmful pattern, and cautiously.
- **Link gap vs competitors**: referring domains competitors have that you don't = an outreach target list (hand from `competitor-and-gaps.md`).

Link building that holds up: digital PR and original data, genuinely useful linkable assets (tools, research), and relevant guest/partner placements. No link schemes.

## Internal linking & site architecture

Internal links you fully control; they're high-leverage.

- **Flat-enough depth**: important pages reachable within ~3 clicks of the homepage.
- **Equity flow**: link from high-authority pages to the pages you want to rank; pillar↔spoke linking for clusters.
- **Descriptive anchors**: use the target's topic words, vary them naturally, avoid "click here".
- **Orphan pages**: pages with no internal links in. Find them and link them in, or prune if low value.
- **Contextual over boilerplate**: in-content links carry more signal than footer/nav.
- **Avoid over-linking** a single page from everywhere; be deliberate.

Deliverable: an internal-link map (which pages link to which), the orphan list, and a prioritized set of links to add with suggested anchors.

## Entity optimization (Knowledge Graph / AI recognition)

Getting search and AI engines to recognize the brand/person/product as a distinct entity.

- **Consistency**: exact-match name, description, and details everywhere (NAP for local; name/role for people).
- **`sameAs` links**: connect the entity across the web: official site, LinkedIn, Crunchbase, Wikipedia, Wikidata, social profiles. Put these in `Organization`/`Person` schema (see `schema.md`).
- **Wikidata**: a structured Wikidata item is one of the strongest entity signals; create/claim one with sourced statements where the entity is notable enough.
- **Wikipedia**: only if genuinely notable by their criteria; don't force it.
- **Corroboration**: the entity's claimed attributes should be confirmed by independent third-party sources (press, directories, profiles).
- **Knowledge panel**: triggered by a recognized entity with enough corroborated signals; you influence it via the above, not directly.

This matters more every quarter because AI answers reason over entities, not just keywords. A well-defined entity gets cited and attributed correctly in AI responses.

## Output

For backlinks: profile summary, anchor distribution, toxicity note, and a competitor-gap outreach list. For internal linking: the map, orphans, and add-these-links list. For entities: a signal audit and a prioritized build plan (schema `sameAs`, Wikidata, corroboration).
