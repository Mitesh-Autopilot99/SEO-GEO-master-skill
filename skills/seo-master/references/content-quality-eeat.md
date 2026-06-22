# Content Quality & E-E-A-T

Assess content quality, E-E-A-T, publish-readiness, and AI-citation readiness. Use for "content quality", "E-E-A-T", "is this ready to publish", "audit my content", "thin content".

## E-E-A-T in plain terms

- **Experience**: first-hand use or involvement. Shown through specifics only someone who did the thing would know, original images, test data.
- **Expertise**: subject knowledge. Shown through depth, correct terminology, accurate detail, named credentials where relevant.
- **Authoritativeness**: recognition by others. Citations to the source, mentions, links, author entities that exist elsewhere on the web.
- **Trust**: the overarching one. Accurate, transparent, sourced, with clear authorship, dates, and contact/about signals. For YMYL (health, finance, legal, safety) topics, trust is weighted heavily.

## CORE-EEAT scoring

Score the page across two halves, then apply veto checks.

**CORE (content fundamentals, 40 items / 0-100):**
- Intent match: does it answer the query the title promises?
- Depth vs competitors: covers the subtopics the top results cover, plus something they don't.
- Structure: answer-first sections, scannable, logical flow.
- Readability: short paragraphs, plain words, defined jargon.
- Accuracy: claims are correct and current.
- Originality: not a rewrite of competitors; adds a distinct angle, data, or example.
- Completeness: no obvious unanswered follow-up question.
- Media: relevant images/diagrams/tables that add information.

**EEAT (trust signals, 40 items / 0-100):**
- Named author with a real, verifiable profile.
- Author/site demonstrates experience or expertise in the topic.
- External citations to authoritative sources for factual claims.
- Publish and last-updated dates present and honest.
- Clear sourcing for statistics.
- Transparency: about page, contact, disclosure of affiliations/sponsorship.
- For YMYL: credentials, review-by-expert, conservative claims.

**Combined score** = average of CORE and EEAT, but veto checks can cap it.

## Veto checks (any failure caps the score)

- Factual error on a material claim → cap at "not publishable until fixed".
- Unsourced statistics presented as fact → cap.
- No identifiable author on a YMYL page → cap.
- Intent mismatch (page doesn't answer its own title) → cap.
- AI-generated tells unaddressed (em-dashes, banned phrases, uniform rhythm) → cap; route through `writing-rules.md`.

## Publish-readiness gates

A page is publish-ready when: intent matches, it beats or matches the top results on depth, every material claim is sourced, author and dates are present, the writing passes `writing-rules.md`, and it has answer-first structure plus an FAQ where appropriate (see `geo-citation-methods.md`).

## AI-citation readiness

Separate from ranking. A page is citable by AI engines when:
- Each section opens with a self-contained, quotable answer.
- Claims carry statistics and named sources (AI engines prefer verifiable facts).
- Comparison data is in tables (AI models cite tables readily).
- There's an FAQ with complete 2-3 sentence answers.
- Entities are clear and consistent (see `backlinks-and-entities.md`).

Score citability 0-100 on those five and recommend the highest-leverage fix first.

## Thin content & decay

- Thin: little unique value, below intent-appropriate depth, or duplicative. Decide: expand, consolidate with a sibling page, or prune (noindex/410).
- Decaying: lost rankings/traffic over time. Hand to `content-production.md` for the refresh workflow.

## Output

Two scores (CORE, EEAT) + combined + citability, the veto results, and a ranked fix list. Don't pad; lead with the one change that moves the page most.
