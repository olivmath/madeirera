## Context

See `proposal.md` for motivation. Fontana scores 48.3/100 — mid-range overall but with the worst tech score in the benchmark (3.3/10.5). The WordPress 4.3.34 installation from 2015 is a security liability with XML-RPC exposed. The site has real content (17 wood species, testimonials, 65+ gallery photos, 30+ years of history) but fails on technical fundamentals: zero WhatsApp, zero meta descriptions, 100% images without alt on home, no H1 on home, wrong lang attribute.

Unlike Baia Sul (19.5/100, full rebuild from nothing), Fontana has a functional visual identity (warm wood tones via the tm-wood-worker theme, brand colors #bf0310 red accent, #C69453 gold, #594431 dark brown) and substantial content to preserve.

## Goals / Non-Goals

**Goals:**

- Build a mobile-first responsive site preserving Fontana's warm wood-toned visual identity.
- Showcase all 17 wood species with descriptions, applications, and photos from the existing gallery.
- Add WhatsApp as primary contact channel (currently completely absent).
- Add a prominent, accessible quote request form (not just buried in footer).
- Fix all technical SEO: meta descriptions, lang="pt-BR", H1 on home, image alt text, JSON-LD.
- Present the 41-year history (founded 1985), quality certificate, and testimonials as trust signals.
- Preserve the existing payment options information (Visa, Mastercard, Construcard, Losango 24x, etc.).

**Non-Goals:**

- No e-commerce checkout, cart, or online payment processing.
- No customer accounts or login system.
- No real-time inventory or pricing (products use "sob consulta" / quote-based pricing).
- No WordPress migration — the prototype is a static HTML site.
- No AI chatbot or advanced search functionality.

## Decisions

### Decision: Full rebuild as static HTML prototype, not WordPress update

The site will be rebuilt as a self-contained HTML/CSS/JS prototype rather than updating the WordPress 4.3 installation.

**Rationale:** WordPress 4.3.34 is 11 years old with known vulnerabilities. The XML-RPC endpoint is exposed. The tm-wood-worker theme and Visual Composer 4.6.2 are discontinued. Updating WP core, theme, and all plugins would risk breaking the site with no guarantee of fixing the structural issues (missing WhatsApp, poor SEO, no forms). A static prototype proves the design improvement first; CMS choice is a production decision.

**Alternative considered:** Updating WordPress to current version. Rejected due to theme/plugin incompatibility risk and because the structural problems (zero WhatsApp, zero meta descriptions, no H1) require design changes, not just version bumps.

### Decision: Preserve Fontana's existing warm color palette

The site will use the existing brand colors: #bf0310 (red accent), #C69453 (gold/warm wood), #594431 (dark brown), with white/cream backgrounds for readability.

**Rationale:** Unlike Baia Sul which had a mismatched cold blue palette, Fontana already uses appropriate warm wood tones that communicate "madeireira." The tm-wood-worker theme established a visual identity that works for the product category. Preserving these colors maintains brand recognition for existing customers.

### Decision: Single-page prototype with anchor navigation

The prototype will be a single HTML file with sections (hero, about, products, testimonials, contact, footer) navigable via anchor links.

**Rationale:** The current site has 5 pages (Home, A Fontana, Produtos, Galeria, Contato). The prototype consolidates this into a single-page experience for easier client review and iteration. Multi-page architecture is defined in specs for production.

### Decision: Product catalog uses existing gallery photos mapped to species

The catalog will map the 65+ existing gallery photos to the 17 documented wood species. The gallery already has photos organized by species name (angelim, cambara, cumaru, etc.).

**Rationale:** Unlike Baia Sul which had only 1 image, Fontana has a rich photo library already organized by wood type. The rebuild should leverage these existing assets rather than using placeholders.

### Decision: Add WhatsApp as primary CTA alongside quote form

WhatsApp click-to-chat will be added as a sticky floating button plus inline CTAs throughout the site. A separate WhatsApp number must be confirmed with the business (currently only landline (48) 3258-1500 is listed).

**Rationale:** WhatsApp is completely absent from the current site — the single most impactful conversion channel missing. The benchmark shows top-scoring competitors have 3-8 WhatsApp touchpoints. A mobile number for WhatsApp must be obtained from the client.

## Risks / Trade-offs

- **No WhatsApp number available** -> The current site only lists a landline. Must confirm a mobile/WhatsApp number with the client before production. Use placeholder in prototype.
- **WordPress content extraction** -> All content has been extracted from the live site. If the WP site goes down, content is preserved in `content.md`.
- **Gallery photo quality** -> The 65+ photos are from 2015 and may be low resolution. The prototype will reference them; production may need re-photography.
- **Testimonials Schema.org** -> The current site already has Schema.org/Review markup on testimonials — one of the few things done right. The rebuild must preserve this.
- **"Mais de 30 anos" claim** -> Founded August 1985. In 2026, the business is 41 years old. Update to "Mais de 40 anos de historia."
- **Business hours unknown** -> Not displayed anywhere on the current site. Add when confirmed.
- **Construcard/Losango payment details** -> Referenced on the about page but not on home. Surface these on the new site as trust signals.

## Open Questions

- WhatsApp number: does the business have a mobile number for WhatsApp? The current site only lists (48) 3258-1500 (landline).
- Current business hours and days of operation.
- Whether the 2015 quality certificate from Sao Jose is still valid/displayable.
- Whether the gallery photos are available in higher resolution.
- Whether the business has social media profiles to link.
- Delivery area: Sao Jose only or broader Grande Florianopolis?
