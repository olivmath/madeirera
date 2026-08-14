## Why

Madeireira Baia Sul scores 19.5/100 in the benchmark — the worst active site among 20+ lumber yards in Grande Florianopolis. The site was generated with WebAcappella in 2014 and has not been meaningfully updated since. Critical problems:

- **Layout fixed at 1021px** — no viewport meta, completely broken on mobile (zero responsive behavior)
- **Zero H1/H2 headings, zero meta description, zero schema.org** — SEO is nonexistent
- **Zero CTAs, zero forms, zero lead capture** — the only conversion path is a floating WhatsApp button
- **Only 1 image on the entire site** (a GIF header) — zero product photos despite listing 13 wood species
- **WebAcappella table/div layout from 2014** — cannot be incrementally fixed; requires full rebuild

Despite these problems, the business has real content worth preserving: 27+ years in market, 13 documented wood species with technical descriptions, domain-based emails, 3 phone numbers, strategic BR-101 location, and service coverage across Sao Jose, Florianopolis, and Palhoca.

## What Changes

- Replace the entire WebAcappella site with a modern, mobile-first responsive site.
- Add a hero section with positioning, region, product categories, and primary CTA in the first viewport.
- Add a product catalog showcasing the 13 wood species with descriptions, applications, and photo placeholders.
- Add a quote request form with product context, name, phone, city, and message fields.
- Add semantic HTML structure: H1 per page, H2 sections, breadcrumbs, image alt text.
- Add meta descriptions, Open Graph metadata, canonical URLs, and JSON-LD structured data (LocalBusiness, Product).
- Add a sticky WhatsApp button with contextual prefilled messages per page/product.
- Keep the existing contact info (3 phones, 2 emails, address) visible in header/footer.
- Keep e-commerce checkout, online payment, and customer accounts out of scope.

## Capabilities

### New Capabilities

- `modern-responsive-site`: Defines the responsive layout, mobile-first design, navigation, hero section, footer, and overall site structure replacing the 2014 fixed-width layout.
- `seo-and-discoverability`: Defines semantic HTML, metadata, structured data, headings hierarchy, image alt text, and crawlability requirements to fix the zero-SEO baseline.
- `conversion-and-lead-capture`: Defines quote forms, CTAs, WhatsApp integration with context, phone click-to-call, and lead capture flows to replace the current zero-conversion state.

### Modified Capabilities

- None.

## Impact

- Replaces the entire existing site — no incremental migration possible from WebAcappella.
- Requires product photos (or professional placeholders) for the 13 wood species already documented on the site.
- Requires confirmation of business hours, service capabilities, and any updated contact details.
- Does not require checkout, payment processing, inventory systems, or customer login.
- Expected score improvement: 19.5 -> 70+/100, with gains across all 6 benchmark pillars.
