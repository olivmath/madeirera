## Why

Madeireira Silva scores 52.2/100 in the benchmark — classified as "Fraco." The site was built with Lovable (AI-generated React SPA) and has strong brand content but critical technical and conversion deficiencies:

- **SPA client-side rendering without SSR** — Google may not index content correctly; all text lives inside a 870KB JS bundle
- **ZERO forms on the entire site** — the only conversion path is WhatsApp
- **Title "MadeireiraSilva"** — no space, no location, no keywords; SEO-hostile
- **15+ of 27 images missing alt text** — accessibility and SEO penalty
- **Zero schema.org structured data** — no rich snippets despite having 4.9/5 Google rating with 70 reviews
- **No individual product pages** — everything in a single-page scroll; no deep-linkable product URLs

Despite these problems, Silva has exceptional brand assets worth preserving and amplifying: 57 years in business (since 1960), 3rd generation family ownership, exclusive "Encaixe Deep Fitting" technology, 100% reforestation wood commitment, 4.9/5 Google rating (70 reviews), 2 physical locations in Palhoca, blog content, and a clear sustainability positioning.

## What Changes

- Replace the Lovable SPA with a server-rendered (or pre-rendered) site ensuring Google indexes all content.
- Fix the title tag: "Madeireira Silva | Madeiras Sustentaveis em Palhoca SC | 57 Anos."
- Add a structured quote request form with product context, replacing WhatsApp-only conversion.
- Add alt text to all 27 images with descriptive, keyword-rich content.
- Add JSON-LD structured data: LocalBusiness (2 locations), Product, Review aggregate.
- Create individual product pages for Kit Casa, Deck/Pergolado, Aberturas, Madeiras em Geral, and Eucalipto.
- Consolidate the 3 WhatsApp entry points (nav, hero, contact) into a consistent pattern with contextual prefilled messages.
- Preserve all existing brand assets: Deep Fitting technology section, sustainability messaging, testimonials, blog posts, business history.
- Keep e-commerce checkout, payment processing, and customer accounts out of scope.

## Capabilities

### New Capabilities

- `modern-responsive-site`: Defines the server-rendered site structure, navigation, hero, product showcase, and footer — replacing the client-side SPA that blocks SEO indexing.
- `seo-and-discoverability`: Defines semantic HTML, metadata, structured data, image alt text, and crawlability fixes for the 15+ missing alt texts and zero schema.org baseline.
- `conversion-and-lead-capture`: Defines quote forms, CTAs, WhatsApp integration with context, and lead capture flows to replace the current zero-form state.

### Modified Capabilities

- None.

## Impact

- Replaces the Lovable SPA rendering model — requires migration from React client-side to SSR/SSG or static HTML.
- Preserves all existing content: product catalog, blog posts, testimonials, Deep Fitting section, company history.
- Requires no new product photos — the existing 27 images are sufficient; they just need alt text.
- Requires confirmation of business hours accuracy and preferred WhatsApp number.
- Does not require checkout, payment processing, inventory systems, or customer login.
- Expected score improvement: 52.2 -> 70+/100, with primary gains in SEO (+5), Conversion (+8), and Tech (+3).
