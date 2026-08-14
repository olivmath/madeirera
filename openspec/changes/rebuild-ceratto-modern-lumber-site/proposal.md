## Why

Ceratto Madeiras scores 50.0/100 in the benchmark — classified as "Fraco" despite having a WordPress/Elementor site with real product photos, prices, and WhatsApp integration. The site has real strengths (responsive Astra theme, visible pricing, multiple contact channels) but critical SEO and conversion deficiencies drag the score down:

- **Title tag keyword-stuffed** — 150+ characters, worst SERP snippet in the benchmark
- **Meta description ABSENT** — zero control over search result display
- **8 H1 tags on a single page** — the WORST case in the entire benchmark
- **15 of 16 images missing alt text** — near-total accessibility and SEO failure
- **ZERO forms** — no lead capture mechanism beyond WhatsApp
- **Moveis e Construcoes page returns 404** — broken internal link
- **Zero JSON-LD structured data** — no rich results, no local business schema
- **Gmail address** (cerattomadeiras@gmail.com) — no domain email

Unlike Baia Sul (19.5/100, full rebuild needed), Ceratto has a functional WordPress site with Elementor, real product photos, and working WhatsApp buttons. The fix is surgical: correct the SEO structure, add alt text to all images, add a quote form, fix the broken page, and add structured data.

## What Changes

- Rewrite the title tag to max 60 characters: "Ceratto Madeiras — Madeireira em Biguacu SC".
- Add meta description targeting local search: "Madeiras tratadas, moveis rusticos e kit tabuas em Biguacu. Itauba, cambara, garapeira, cedro e mais. Ligue ou envie WhatsApp."
- Fix heading hierarchy: reduce to exactly 1 H1 per page, use H2 for sections, H3 for products.
- Add descriptive alt text to all 15 images currently missing it.
- Add a quote request form with fields: nome, telefone/WhatsApp, tipo de madeira, mensagem.
- Fix the broken Moveis e Construcoes page (currently returning 404 from navigation link).
- Add JSON-LD structured data: LocalBusiness with address, phone, hours, service area.
- Add Open Graph metadata for WhatsApp/social sharing previews.
- Add canonical URL declaration.
- Keep existing WhatsApp buttons, pricing display, and product photos.
- Keep the current Astra/Elementor responsive layout (already functional).

## Capabilities

### New Capabilities

- `modern-responsive-site`: Defines improvements to the existing responsive layout — hero section refinement, product showcase with proper image presentation, footer consolidation, and navigation fixes (broken 404 link). Does NOT require a full rebuild; the Astra theme already provides responsive behavior.
- `seo-and-discoverability`: Defines the complete SEO overhaul — title rewrite, meta description, heading hierarchy fix (8 H1 down to 1), alt text for 15/16 images, JSON-LD LocalBusiness, Open Graph, and canonical URL.
- `conversion-and-lead-capture`: Defines the quote form, enhanced CTAs, WhatsApp contextual messages per product, and click-to-call improvements to fix the zero-form baseline.

### Modified Capabilities

- None.

## Impact

- Does NOT require a full site rebuild — the WordPress/Elementor structure is functional and responsive.
- Requires adding alt text to 15 images (product photos already exist on the site).
- Requires creating a quote form (no form exists anywhere on the current site).
- Requires fixing the broken Moveis e Construcoes navigation link (404 error).
- Requires rewriting title, adding meta description, restructuring headings — all content-level changes within the existing Elementor page builder.
- Does not require new product photos — the site already has photos for 8 wood species and product categories.
- Does not require checkout, payment processing, or customer accounts.
- Expected score improvement: 50.0 -> 70+/100, with largest gains in SEO (7.8 -> 15+) and Conversion (11.6 -> 20+).
