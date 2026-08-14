## Context

See `proposal.md` for motivation. ZCF Madeireira scores 40.5/100 on a directory/aggregator site (madeiratratada.floripa.br) where it appears as one card among several lumber businesses. The directory is operated by Agencia G13 and built with WordPress + Elementor + JetEngine. ZCF has no standalone site — only this directory card with a truncated description, a WhatsApp button, and a phone number.

The key challenge: this is NOT a "fix the existing site" scenario. This is a "build a standalone site from scratch" scenario using the business data extracted from the directory listing plus the dedicated ZCF page on that directory.

## Goals / Non-Goals

**Goals:**

- Build a mobile-first responsive standalone site for ZCF Madeireira as a treated-wood specialist.
- Create a product showcase for treated wood categories (decks, pergolados, cercas, casas de madeira, estruturas) with autoclave treatment as the differentiator.
- Add at least one quote/contact form to capture leads (currently zero forms anywhere).
- Implement proper SEO: H1 per page, H2 sections, meta descriptions, JSON-LD structured data.
- Leverage the 100+ bairro geographic coverage from the directory as service area landing content for local SEO.
- Present ZCF as a 25+ year established specialist in treated wood, not a generic directory listing.

**Non-Goals:**

- No e-commerce checkout, cart, or online payment.
- No customer accounts or login system.
- No real-time inventory or pricing (products use "sob consulta" / quote-based pricing).
- No replication of the directory model — this is ZCF's own site, not a multi-business aggregator.
- No custom CMS — the prototype is a static HTML site.

## Decisions

### Decision: Standalone site, not directory improvement

The prototype will be a standalone ZCF Madeireira site, not an improvement of the existing directory page.

**Rationale:** The directory (madeiratratada.floripa.br) is owned by Agencia G13, not by ZCF. ZCF cannot control its own content, SEO, forms, or conversion paths on the directory. A standalone site gives ZCF full control over branding, products, and lead capture. The directory can continue to exist as a referral source linking to ZCF's own site.

**Alternative considered:** Improving ZCF's listing within the directory. Rejected because ZCF would remain dependent on a third-party for its web presence and could never score above ~55 without forms, product pages, and independent SEO.

### Decision: Treated wood specialist positioning

The site will position ZCF as a treated-wood specialist (autoclave treatment) rather than a general lumber yard.

**Rationale:** ZCF's directory listing and dedicated page both emphasize "madeira tratada" (treated wood) with autoclave processing. This is a clear differentiator from competitors who sell general lumber. The site name itself references "madeira tratada." The product catalog should be organized around treated wood applications (decks, pergolados, cercas, casas de madeira) rather than raw wood species.

**Alternative considered:** General lumber yard positioning like Baia Sul (which lists 13 raw wood species). Rejected because ZCF's brand identity is built around treated wood, and the specialist positioning is stronger for SEO and conversion.

### Decision: Single-page prototype with anchor navigation

The prototype will be a single HTML file with sections (hero, about, products, service areas, contact, footer) navigable via anchor links.

**Rationale:** Same as Baia Sul — the prototype's purpose is to demonstrate the visual and structural improvement. A single file is easier to share, review, and iterate on.

### Decision: Warm, wood-toned visual identity with green accent

The site will use warm brown/wood tones for the primary palette with forest green as accent color, reflecting treated wood's natural appearance and durability.

**Rationale:** The directory currently uses a generic green (#0b9c1f) for ZCF's card border — this green can be refined as an accent (treated wood = preservation = green). The primary palette should be warm browns and creams to communicate "lumber yard." The Instagram (@zcfmadeireira) likely uses similar warm wood tones in product photos.

### Decision: Geographic service area content from directory data

The site will include a service area section that repurposes the directory's 100+ bairro listings across 5 cities (Florianopolis, Sao Jose, Palhoca, Biguacu, Santo Amaro da Imperatriz) as structured, SEO-optimized content.

**Rationale:** The directory already has this geographic coverage indexed. A standalone ZCF site should capture this local SEO value. Instead of repeating "Madeira tratada no [bairro] em [cidade]" as raw text (the current directory approach), the site will organize service areas by city with proper H2/H3 headings and structured data.

### Decision: Product catalog organized by application, not wood species

Products will be organized by use case (decks, pergolados, cercas, casas de madeira, estruturas rurais, estruturas urbanas) rather than by wood species.

**Rationale:** ZCF sells treated wood for specific applications. Customers search for "deck de madeira tratada" or "pergolado de madeira tratada", not for specific species. Application-based organization matches search intent and ZCF's positioning as a solutions provider.

## Risks / Trade-offs

- **Limited content from directory** -> The directory listing and dedicated page have only ~150 characters of description. Product details, technical specs, and trust signals will need to be sourced from ZCF's Instagram, WhatsApp conversations with the business, or generated as reasonable placeholders.
- **No product photos available** -> Use placeholder areas with clear labels. Block production launch until at least 4-6 application categories have real photos.
- **Address ambiguity** -> The directory lists ZCF's address as "R. Alvaro Joao Ferreira, 04 - Guarda do Cubatao, Palhoca - SC, 88135-349" but the benchmark classifies ZCF under Biguacu. Use the directory address (Palhoca) as canonical.
- **Existing domain** -> ZCF has zcfmadeireira.com.br registered. The prototype assumes deployment to this domain; confirm with client.
- **Years in market claim** -> Directory says "mais 25 anos" (which appears to have a typo — should be "mais de 25 anos"). Use "Mais de 25 anos" in content.

## Open Questions

- Exact founding year and current years-in-market claim.
- Current business hours and days of operation.
- Whether the business has real product/project photos available (check Instagram @zcfmadeireira).
- Full product/service list beyond what the directory mentions.
- Whether zcfmadeireira.com.br is active and available for the new site.
- Delivery area boundaries and logistics details.
- Autoclave treatment certifications or standards followed.
