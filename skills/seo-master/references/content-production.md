# Content Production: Briefs, Articles, Refreshes, Fact-Checking

Producing the content itself. Always pair with `writing-rules.md` (voice) and `geo-citation-methods.md` (citable structure). Use for "content brief", "write an article", "write this page", "refresh this content", "fact-check".

## Content briefs

A brief tells a writer exactly what to produce so the page wins its SERP.

Include:
- **Target query + secondary queries** and the dominant intent.
- **Search-intent summary**: what the searcher actually wants, from reading the SERP.
- **Recommended page type and angle**: including the gap the top results miss (from `competitor-and-gaps.md`).
- **Outline**: H1, then H2/H3 with a one-line note on what each section must cover. Phrase H2s as real queries.
- **Per-section word-count guidance**: derived from how deep the ranking pages go, not an arbitrary total.
- **Entities/terms to include**: topical and technical terms the topic requires.
- **Internal links**: which existing pages to link to/from (from `backlinks-and-entities.md`).
- **Schema** to apply (from `schema.md`).
- **GEO requirements**: answer-first sections, statistics to source, FAQ questions to answer.
- **Title and meta** options (from `on-page-and-meta.md`).

## Writing / generating an article

Order of operations:
1. Read `writing-rules.md` and the brand voice guide if one exists.
2. Read `geo-citation-methods.md` and apply all 9 methods, especially answer-first openings, statistics with sources, and an FAQ.
3. Draft to the brief's outline and word-count guidance.
4. **First paragraph is the article**: answer the title's promise in the first sentence. No "in this article", no TL;DR label at the top.
5. Comparison/listicle: the site's own product goes first (honestly); every item gets a real official link.
6. Self-check before delivering (checklist below).

### Pre-delivery checklist
- [ ] Zero em-dashes. Run `grep -c "—" file.md` → must be 0. Same for ` – ` and `--` as dashes.
- [ ] No banned words/phrases (see `writing-rules.md`).
- [ ] Answer-first in every section; first sentence of each is self-contained and quotable.
- [ ] 5+ sourced statistics, 5+ authoritative citations, 2-3 attributed quotes where the topic allows.
- [ ] Primary keyword used 2-3 times max, not stuffed.
- [ ] FAQ section with 5-7 complete 2-3 sentence answers.
- [ ] Comparison data in a table where relevant.
- [ ] Named author, publish/updated date, sources listed.
- [ ] Passes the E-E-A-T veto checks (`content-quality-eeat.md`).

## Refreshing decaying content

When a page has lost traffic/rankings:
- **Diagnose the decay**: is it stale facts/stats, a SERP-intent shift, new competitors with deeper content, lost links, or a technical issue? Fix the actual cause, not just the date.
- **Update**: refresh stats and examples with current sourced data, add sections covering subtopics now expected, improve the answer-first openings, strengthen E-E-A-T (author, sources, dates), re-cut the title/meta if CTR is the issue.
- **Don't fake freshness**: only bump `dateModified` when the content genuinely changed.
- **Consolidate**: if two weak pages compete, merge into one stronger page and redirect.
- Re-run the pre-delivery checklist.

## Fact-checking

Before publishing, verify accuracy to protect E-E-A-T (and avoid the unsourced-stat veto):
- Every statistic traces to a named, dated, authoritative source.
- Claims are current (check for superseded data, especially in fast-moving topics).
- Quotes are real and correctly attributed.
- No fabricated sources, studies, or figures. If a claimed source can't be verified, cut the claim or reword to what's actually supportable.
- Flag anything you can't verify rather than letting it through.

## Output

The brief, the drafted content (as a file), the refreshed page with a changelog of what changed and why, or a fact-check report listing each claim, its source, and verified/unverified/corrected status.
