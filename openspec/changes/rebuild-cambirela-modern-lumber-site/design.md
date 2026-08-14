## Context

See `proposal.md` for motivation. Cambirela scores 52.4/100 — "Fraco" but with a notable strength: 8.0/10 recommendation score. The business has 20+ years of operation, active social media, real customer testimonials, and a broad product catalog (25+ items). The problem is not the business — it is the site's inability to capture leads and its invisible SEO.

The current site uses WordPress + Elementor + OceanWP theme. It has a working responsive layout, a photo gallery with 20+ real images, and a testimonials carousel. The rebuild should enhance what works and fix what is broken.

## Goals / Non-Goals

**Goals:**

- Add at least one structured quote form to capture leads (currently zero forms exist).
- Unify the 3 scattered WhatsApp numbers into 1 primary contact with clear routing.
- Create product cards with individual photos, descriptions, and per-product quote CTAs.
- Fix all SEO gaps: meta descriptions, unique title tags, schema.org, image alt text.
- Fix broken links (Instagram URL).
- Preserve and enhance the existing testimonials, gallery, and company history sections.

**Non-Goals:**

- No e-commerce checkout, cart, or online payment.
- No customer accounts or login system.
- No real-time inventory or pricing (products use quote-based pricing).
- No CMS migration — the prototype is a static HTML site.
- No visual redesign of the color palette — the existing warm wood tones are appropriate.

## Decisions

### Decision: Enhancement prototype, not full rebuild

The site will be rebuilt as a static HTML prototype that improves upon the current structure rather than starting from scratch. The current site has a functional responsive layout and real content — the problems are in conversion, SEO, and product presentation.

**Rationale:** Unlike Baia Sul (19.5/100, completely broken), Cambirela has a working foundation. The prototype demonstrates how to fix the specific gaps rather than reimagining the entire site.

**Alternative considered:** Patching the existing WordPress site. Deferred to implementation phase; the prototype proves the improvements first.

### Decision: Keep existing warm visual identity

The current site uses a warm color palette with wood-toned background textures, dark green accents, and earth tones. This is appropriate for a lumber yard and should be preserved.

**Rationale:** The visual identity already communicates "lumber yard" effectively. The benchmark does not penalize the aesthetics — it penalizes the missing conversion and SEO elements.

### Decision: Unified WhatsApp with named contacts

The prototype will display 1 primary WhatsApp number in the header/CTA, with a contact section showing all 3 named contacts (Denise, Amanda, Adriana) for direct routing. The floating WhatsApp button uses the primary number only.

**Rationale:** The current 3-number approach confuses visitors. A single entry point with internal routing preserves the multi-agent benefit while simplifying the UX. The named contacts add a personal touch that matches the high-recommendation business culture.

### Decision: Product catalog with individual cards replaces flat list

The current product list is a single `<ul>` with 35+ bold items (many duplicated). The prototype will consolidate into ~17 unique product cards with photo, description, and quote CTA each.

**Rationale:** The flat list buries products and provides no visual distinction or call-to-action per item. Cards allow photo showcase, contextual WhatsApp messages, and scannable browsing.

### Decision: Single-page prototype with anchor navigation

The prototype will be a single HTML file with sections (hero, about, products, testimonials, contact, footer) navigable via anchor links, matching the current site structure.

**Rationale:** The current site already uses anchor navigation (#nossa-empresa, #produtos, #galeria, #depoimentos). Preserving this pattern makes the prototype feel familiar while demonstrating the improvements.

## Risks / Trade-offs

- **Product photos**: Only ~8 real images exist for 25+ products. Use existing gallery photos where applicable and placeholder areas for missing products. Block production launch until at least 10 products have real individual photos.
- **WhatsApp number choice**: The business must decide which number becomes primary. Default to (48) 99205-8040 (Denise) as it appears first and most frequently in the current site.
- **Duplicate product entries**: The current list has ~35 items but many are duplicates (e.g., "Forro de Pinus Tratado" appears in both the detailed list and the keyword list). Consolidate to ~17 unique products.
- **Address unknown**: No physical address is visible on the current site. The Google Maps embed points to "R. Nereu Ghizoni, 1040" in Palhoca. Use this as the address pending confirmation.
- **Business hours unknown**: Not displayed on the current site. Add placeholder or omit until confirmed.

## Open Questions

- Physical address confirmation (R. Nereu Ghizoni, 1040 - Palhoca?).
- Business hours and days of operation.
- Which WhatsApp number should be primary.
- Whether the business has individual product photos available beyond the gallery.
- Exact founding year for the "20+ years" claim.
