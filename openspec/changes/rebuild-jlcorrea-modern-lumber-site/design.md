## Context

See `proposal.md` for motivation. JL Correa Madeiras scores 47.5/100 — "Fraco" classification. Unlike the lowest-scoring sites that need full rebuilds, JL Correa has a functional Elementor layout with decent UI (11.2/15). The problems are structural: broken heading hierarchy, missing metadata, zero forms, and catastrophic alt text coverage (27/28 images missing alt).

The business has been operating since 1974 (50+ years), spans 3 generations, and has strong storytelling content already on the site. The rebuild should preserve this content and the visual identity while fixing every structural and SEO deficiency.

## Goals / Non-Goals

**Goals:**

- Fix the catastrophic alt text problem: add descriptive alt to all 27 images currently without it.
- Restructure heading hierarchy from 7 H1 + 22 H2 to 1 H1 + ~6 semantic H2 headings.
- Add title tag, meta description, Open Graph, and JSON-LD structured data (all currently absent).
- Add at least one quote/contact form to create a non-WhatsApp conversion path (currently zero forms).
- Create product showcase sections with individual cards for each wood species and service category.
- Present JL Correa as an established, certified, family-run lumber yard with 50+ years of history.
- Keep the existing WhatsApp integration but add contextual prefilled messages per product.

**Non-Goals:**

- No e-commerce checkout, cart, or online payment.
- No customer accounts or login system.
- No real-time inventory or pricing (quote-based pricing model).
- No custom CMS — the prototype is a static HTML site.
- No radical visual redesign — the current Elementor layout is already clean and modern.

## Decisions

### Decision: Structural rebuild preserving visual identity

The site will be rebuilt as a static HTML/CSS/JS prototype that preserves the current visual language (warm tones, clean layout, modern typography from Elementor) while fixing all structural problems.

**Rationale:** The UI score (11.2/15) is already the 4th best in the benchmark. The problems are not visual — they are semantic (heading hierarchy), technical (missing metadata), and functional (zero forms). A visual redesign would waste effort on the strongest dimension while ignoring the weakest.

**Alternative considered:** Full visual redesign. Rejected because UI is already competitive; effort should target SEO (9.3) and Conversion (10.0).

### Decision: Single-page prototype with anchor navigation

The prototype will be a single HTML file with sections (hero, about/history, products, gallery, contact, footer) navigable via anchor links.

**Rationale:** The current site is already single-page. The prototype's purpose is to demonstrate structural and conversion improvements to the client. Multi-page architecture is defined in specs for production.

**Alternative considered:** Multi-page prototype with separate product pages. Deferred to production phase.

### Decision: Product catalog organized by category, not individual species

The product showcase will organize products by category (Madeiras Certificadas, Aberturas, Pinus Tratado) with species listed within each category, rather than 13+ individual product cards.

**Rationale:** The current site already groups products this way. JL Correa's catalog is service-oriented (certified wood, custom openings, treated pine) rather than species-oriented like Baia Sul's 13-species technical catalog. The showcase should match the business model.

**Alternative considered:** Individual species cards like Baia Sul. Rejected because JL Correa's content emphasizes service categories, not species-level technical data.

### Decision: Quote form as primary conversion mechanism

A structured quote form will be added as the primary conversion mechanism alongside the existing WhatsApp integration. The form will capture: name, phone/WhatsApp, product interest (dropdown with categories), quantity/dimensions, intended use, and message.

**Rationale:** The benchmark penalizes zero forms heavily (Conversion: 10.0/25). WhatsApp is effective but exclusive reliance on it loses visitors who prefer form-based contact. The form also creates structured lead data.

### Decision: Preserve the 50-year family history narrative

The about/history section will preserve the 3-generation timeline (1974 founding, second generation, Joao Luiz Correa as current leader) and the mission/vision/values content, presenting it with proper semantic structure.

**Rationale:** This is a genuine competitive advantage. Few competitors in the benchmark have 50+ years of documented history. The content exists but is buried under broken heading hierarchy.

## Risks / Trade-offs

- **Alt text for 27 images requires manual description** -> Each product/installation photo needs a specific, keyword-relevant alt text. Use the gallery context and product names visible in the photos to write accurate descriptions.
- **Business hours may have changed** -> The site says "7:15-12:00, 13:00-18:00, closed Saturdays." Confirm with client before production.
- **Wood species list is incomplete** -> Only "Angelim, Cambara, Eucalipto, Pinus Tratado, entre outras" are named. Full species list needed for the product catalog.
- **Social media links may be inactive** -> Facebook, Twitter, YouTube are listed but may not have active profiles. Verify before including.
- **CEP needs verification** -> Address shows R. Edeling Schutz, 135, Centro, Palhoca - SC. CEP 88131-340 from live site needs confirmation.

## Open Questions

- Complete list of wood species and products currently in stock.
- Whether "Vendas de Aberturas" (door/window frames) is still an active service line.
- Active social media profiles — are Facebook, Twitter, YouTube maintained?
- Whether the business serves delivery beyond Palhoca/Grande Florianopolis.
- Current WhatsApp number confirmation: (48) 9 9697-3814.
- Whether the business has additional product photos beyond the current gallery of ~24 images.
