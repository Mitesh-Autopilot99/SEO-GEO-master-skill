# Schema & Structured Data

Detect, validate, and generate Schema.org markup. JSON-LD preferred. Use for "schema", "structured data", "rich results", "JSON-LD", "markup".

## Global schema rules (from SKILL.md, repeated for safety)

- **Never recommend HowTo schema**: deprecated September 2023.
- **FAQ schema**: Google rich results only for government and healthcare since August 2023. Existing FAQPage on a commercial site → Info priority, note AI-citation benefit. New FAQPage → not recommended for Google rich results, still useful for AI citation.
- Mark up only content that is actually visible on the page. Don't mark up hidden or absent content.
- Validate before recommending deployment.

## Decision tree (what to add)

- Article / blog post → `Article` (or `NewsArticle` / `BlogPosting`) with `author`, `datePublished`, `dateModified`, `publisher`, `image`, `headline`.
- Product page → `Product` with `offers` (price, availability, currency), `aggregateRating`/`review` only if genuinely present.
- Local business → `LocalBusiness` (or specific subtype) with `name`, `address`, `geo`, `openingHours`, `telephone`, `priceRange`.
- Organization / brand → `Organization` with `name`, `url`, `logo`, `sameAs` (links to social/Wikidata/Wikipedia). Key for entity recognition; see `backlinks-and-entities.md`.
- Person / author → `Person` with `name`, `jobTitle`, `sameAs`, `worksFor`.
- Recipe → `Recipe`. Event → `Event`. Job → `JobPosting`. Course → `Course`. Software → `SoftwareApplication`. Video → `VideoObject`.
- Breadcrumbs → `BreadcrumbList` (broadly safe and useful).
- FAQ → `FAQPage` only under the restriction above.

Always add `Organization` + `WebSite` (with `SearchAction` if site search exists) site-wide, and `BreadcrumbList` on deep pages.

## JSON-LD templates

**Article:**
```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "...",
  "author": { "@type": "Person", "name": "...", "url": "..." },
  "datePublished": "2026-01-01",
  "dateModified": "2026-01-01",
  "publisher": { "@type": "Organization", "name": "...", "logo": { "@type": "ImageObject", "url": "..." } },
  "image": "https://.../image.jpg"
}
```

**Organization (with entity signals):**
```json
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "...",
  "url": "https://...",
  "logo": "https://.../logo.png",
  "sameAs": ["https://www.linkedin.com/company/...", "https://www.wikidata.org/wiki/Q...", "https://en.wikipedia.org/wiki/..."]
}
```

**Product:**
```json
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "...",
  "image": "https://.../product.jpg",
  "description": "...",
  "brand": { "@type": "Brand", "name": "..." },
  "offers": { "@type": "Offer", "price": "29.00", "priceCurrency": "GBP", "availability": "https://schema.org/InStock", "url": "https://..." }
}
```

**LocalBusiness:**
```json
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "...",
  "address": { "@type": "PostalAddress", "streetAddress": "...", "addressLocality": "...", "postalCode": "...", "addressCountry": "GB" },
  "geo": { "@type": "GeoCoordinates", "latitude": "...", "longitude": "..." },
  "telephone": "...",
  "openingHoursSpecification": []
}
```

## Validation

- Check required vs recommended properties for the type.
- Confirm every marked-up value appears in visible page content.
- Test with Google's Rich Results Test (eligible types) and the Schema.org validator (syntax).
- Common errors: missing required field, wrong nesting, date format (use ISO 8601), marking up absent ratings/reviews, multiple conflicting types on one entity.

## Output

State current markup, validation errors, and the prioritized list of additions/fixes with ready-to-paste JSON-LD. Note which give Google rich-result eligibility vs which are primarily for AI/entity understanding.
