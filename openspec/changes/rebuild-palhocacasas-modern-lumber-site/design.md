## Context

See `proposal.md` for motivation. Palhoca Casas de Madeira scores 40.5/100 — a pre-fabricated wooden house specialist with strong business differentiators (20 years, Caixa financing, extended hours) but a minimal single-page site that fails to showcase them. The site has basic WordPress/Elementor structure but wastes it on sparse content and broken SEO.

## Goals / Non-Goals

**Goals:**

- Build a responsive site that showcases pre-fabricated wooden houses as the primary product — not generic lumber.
- Create a house model catalog with specs, photos, and pricing indicators.
- Add quote and financing inquiry forms (currently zero forms exist).
- Fix all SEO deficiencies: duplicate H1, missing meta description, zero schema.org, empty alt text.
- Leverage the strong differentiators: Caixa financing, 20-year track record, extended hours, autoclave treatment.
- Expand the photo gallery beyond the current single project image.

**Non-Goals:**

- No e-commerce checkout, cart, or online payment.
- No customer accounts or login system.
- No real-time pricing — house models use "a partir de" or "sob consulta" pricing.
- No AI chatbot or advanced search.
- No custom CMS — the prototype is a static HTML site.

## Decisions

### Decision: Pre-fabricated house niche as primary identity

The site will position "casas de madeira pre-fabricadas" as the hero message, not generic lumber sales. The lumber catalog (pinus, eucalipto, angelim) appears as a secondary section.

**Rationale:** The business name is "Palhoca Casas de Madeira" — houses are the core product. The current site mentions house models and architect services but shows zero models. Competitors in the casas-de-madeira niche that showcase models with photos and specs convert significantly better.

### Decision: Caixa Economica financing as primary trust signal

The Caixa financing acceptance will be displayed as a prominent badge/banner in the hero section, not buried in a side column. This is a major differentiator — most small lumber yards cannot offer bank financing.

**Rationale:** The current site already shows the Caixa logo prominently in the hero area, indicating the business considers this a key selling point. Bank financing acceptance signals legitimacy, reduces purchase friction, and differentiates from informal competitors.

### Decision: Extended hours as conversion differentiator

The 08:00-22:00 schedule with weekend/holiday coverage will be displayed prominently in the header and contact section, not just in body text.

**Rationale:** Most lumber yards operate standard business hours. Extended hours (08:00-22:00, 7 days) is a significant convenience differentiator, especially for customers who work during the day. This should be immediately visible to reduce "are they open?" friction.

### Decision: Autoclave treatment as quality signal

The autoclave-treated pinus construction will be highlighted as a durability feature with explanation of benefits (resistance to sun, rain, humidity).

**Rationale:** The current site mentions autoclave treatment but buries it in a paragraph. This is a technical quality differentiator that justifies premium pricing and should be visually prominent.

### Decision: Warm wood-cabin visual identity

The site will use a color palette inspired by wooden houses: warm browns, honey tones, dark wood accents, and forest greens, with cream/white backgrounds for readability. Hero imagery should show completed wooden houses, not raw lumber.

**Rationale:** The site sells houses, not boards. The visual identity should evoke the finished product — cozy, natural, warm. This aligns with the casas-de-madeira market positioning and differentiates from generic lumber yard sites.

### Decision: Single-page prototype with anchor navigation

The prototype will be a single HTML file with sections (hero, house models, about, gallery, contact, footer) navigable via anchor links.

**Rationale:** The prototype's purpose is to demonstrate the visual and structural improvement. A single file is easier to share and review. The production site can expand to multi-page when needed.

### Decision: House model cards with placeholder specs

The catalog will show 4-6 house model cards with: name, size (m2), number of rooms, photo placeholder, price range indicator, and a "Solicitar Orcamento" CTA. Exact models and specs need client confirmation.

**Rationale:** The current site mentions "diversos modelos de casas" and "projetos juntos a nossos arquitetos" but shows zero models. Even placeholder cards demonstrate the catalog concept and dramatically improve the conversion path.

## Risks / Trade-offs

- **No real house model photos** -> Use placeholder areas with "foto do modelo" labels. Block production launch until real photos are available.
- **House model specs unknown** -> Use realistic placeholder specs (e.g., "Casa Araucaria - 45m2 - 2 quartos"). Client must confirm actual models offered.
- **Pricing sensitivity** -> Use "A partir de R$ XX.000" ranges or "Sob consulta" if the client prefers not to show pricing.
- **20 years claim** -> Site says "20 anos de experiencia" and also says the business started in the 80s. The timeline is inconsistent. Use "Mais de 20 anos" unless the client confirms the exact founding year.
- **12 years vs 20 years** -> The about text says "ha 12 anos no mercado" in one place and "20 anos de experiencia" in another. Needs client clarification.
- **Single WhatsApp number** -> All 5 WhatsApp links point to +55 48 99108-8224. Confirm this is still the active number.

## Open Questions

- Exact house models currently offered with specs (m2, rooms, features).
- Pricing approach: show ranges ("a partir de") or "sob consulta" only?
- Exact founding year (inconsistent: "anos 80" vs "12 anos no mercado" vs "20 anos de experiencia").
- Whether the business has completed project photos available for the gallery.
- Whether custom/architect projects should be a separate section or integrated into the catalog.
- Current WhatsApp number confirmation: +55 48 99108-8224.
