## Context

See `proposal.md` for motivation. Madeireira Silva scores 52.2/100 — classified as "Fraco" despite having strong brand content. The site was built with Lovable (AI-generated React SPA) which produces visually decent layouts but fails on SEO (client-side rendering, missing alt text, no structured data) and conversion (zero forms). Unlike Baia Sul's full rebuild, Silva's redesign is about fixing the technical delivery of already-good content.

## Goals / Non-Goals

**Goals:**

- Deliver all existing content via server-rendered or pre-rendered HTML so Google can index it.
- Add a quote request form as an alternative conversion path alongside WhatsApp.
- Fix all 15+ images missing alt text with descriptive, keyword-rich alternatives.
- Add JSON-LD structured data for LocalBusiness (2 locations), products, and aggregate reviews.
- Correct the title tag and meta description for local SEO targeting Palhoca.
- Preserve the existing visual identity — the Lovable-generated design is already warm, wood-toned, and appropriate.
- Maintain all existing content: Deep Fitting section, blog, testimonials, product catalog, company history.

**Non-Goals:**

- No visual redesign — the current aesthetic is adequate (UI: 10.4/15 is competitive).
- No e-commerce checkout, cart, or online payment.
- No customer accounts or login system.
- No real-time inventory or pricing.
- No CMS — the prototype is a static HTML site.

## Decisions

### Decision: Pre-rendered static HTML preserving current visual design

The site will be rebuilt as pre-rendered HTML/CSS/JS that delivers the same visual design but with server-rendered content instead of client-side React hydration.

**Rationale:** Silva's visual design is already good (UI: 10.4/15). The problem is not aesthetics but delivery: a 870KB JS bundle that must execute before any content is visible to crawlers. Pre-rendering solves SEO without requiring a visual redesign.

**Alternative considered:** Adding SSR to the existing React app (Next.js migration). More complex and out of scope for a prototype; deferred to production phase.

### Decision: Keep existing warm green/wood color palette

The current site uses a nature-inspired palette with forest greens, warm wood tones, and cream backgrounds that already communicates "sustainable lumber yard" effectively.

**Rationale:** Unlike Baia Sul (cold navy/blue), Silva's palette already matches the product identity. The benchmark scored UI at 10.4/15 — the 2nd highest among Palhoca competitors. Changing the palette would lose existing brand recognition with no benchmark gain.

### Decision: Add quote form alongside WhatsApp, not replacing it

A structured quote request form will be added as an additional conversion channel. WhatsApp remains the primary channel but with consolidated, contextual integration.

**Rationale:** The benchmark penalizes zero forms (-3 to -5 points in Conversion). Adding a form while keeping WhatsApp provides two conversion paths. The current site has 3 separate WhatsApp entry points (nav, hero, contact section) — these will be consolidated into a consistent pattern.

### Decision: Individual product pages with deep-linkable URLs

Each product category (Kit Casa, Deck/Pergolado, Aberturas, Madeiras em Geral, Eucalipto) will have its own URL-addressable page instead of being sections in a single-page scroll.

**Rationale:** Individual pages allow: (1) unique title/meta per product for SEO, (2) direct linking from search results, (3) Product schema.org markup per page, (4) contextual WhatsApp prefills. The current single-page approach means all products share one generic title.

### Decision: Leverage existing 4.9/5 Google rating with AggregateRating schema

The site will include AggregateRating structured data reflecting the 4.9/5 rating with 70 reviews already visible on Google.

**Rationale:** Silva has the best Google rating among all benchmarked competitors but zero structured data to surface this in search results. Adding AggregateRating schema is a low-effort, high-impact SEO win that could enable rich snippets with star ratings in SERPs.

## Risks / Trade-offs

- **SPA to static migration may lose interactive features** -> The prototype only needs to demonstrate content and structure; interactive features (hero slider, smooth scroll) can use vanilla JS or CSS.
- **Blog content migration** -> The current site has blog posts (Pinus vs Eucalipto, Madeira Autoclavada). The prototype should include blog structure but full blog migration is out of scope.
- **Two physical locations** -> Both addresses must appear in LocalBusiness schema; structured data needs to handle multi-location correctly.
- **Deep Fitting technology claims** -> Preserve the marketing language exactly as-is; do not add or modify technical claims about the proprietary technology.

## Open Questions

- Whether the WhatsApp number (48) 99858-5524 is the preferred contact for both locations.
- Whether the blog should be included in the prototype or deferred.
- Whether the business has updated hours or seasonal variations.
- Current status of Instagram (@madeireirasilvaoficial) and YouTube (@MadeireiraSilvaoficial) channels.
