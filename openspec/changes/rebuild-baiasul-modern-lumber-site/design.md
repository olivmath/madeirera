## Context

See `proposal.md` for motivation. Baia Sul scores 19.5/100 — the lowest active site in the benchmark. The 2014 WebAcappella generator produced a fixed-width, table-based layout with no responsive behavior, no semantic HTML, no forms, and essentially no images. The site cannot be patched; it must be rebuilt from scratch.

The business has been operating for 27+ years and lists 13 wood species with technical descriptions. The rebuild should preserve and enhance this content while fixing every benchmark deficiency.

## Goals / Non-Goals

**Goals:**

- Build a mobile-first responsive site that works on all screen sizes (the current site is completely broken on mobile).
- Create a product showcase for the 13 documented wood species with space for photos when available.
- Add at least one quote/contact form to capture leads (currently zero forms exist).
- Implement basic SEO: one H1 per page, H2 sections, meta descriptions, structured data (currently all zero).
- Present Baia Sul as an established, trustworthy lumber yard with 27+ years of experience.
- Keep the existing WhatsApp integration but add contextual messages.

**Non-Goals:**

- No e-commerce checkout, cart, or online payment.
- No customer accounts or login system.
- No real-time inventory or pricing (products use "sob consulta" / quote-based pricing).
- No AI chatbot or advanced search functionality.
- No custom CMS — the prototype is a static HTML site.

## Decisions

### Decision: Full rebuild as static HTML prototype

The site will be rebuilt as a self-contained HTML/CSS/JS prototype, not patched from WebAcappella output.

**Rationale:** WebAcappella generates non-semantic table/div layouts with inline styles, absolute positioning, and IE-era compatibility hacks. There is no recoverable structure, template system, or content model. Every aspect — markup, styling, responsiveness, semantics — must be written from scratch.

**Alternative considered:** Extracting content and migrating to a CMS. Deferred to implementation phase; the prototype proves the design first.

### Decision: Warm, wood-toned visual identity

The site will use a color palette inspired by lumber and wood: warm browns, dark wood tones, and forest greens, with white/cream backgrounds for readability. This follows the visual pattern of successful competitors in the market (Ceratto Madeiras, Fontana Madeireira).

**Rationale:** The current site uses a cold navy/blue corporate palette (#01163f, #0d7eca) that does not communicate "lumber yard." Competitors that score higher use wood textures, warm tones, and nature imagery. The design should feel like a real madeireira, not a generic corporate page.

**Alternative considered:** Keeping the current blue palette. Rejected because it contradicts the product identity and falls behind competitor visual standards.

### Decision: Single-page prototype with anchor navigation

The prototype will be a single HTML file with sections (hero, about, products, contact, footer) navigable via anchor links, rather than multi-page.

**Rationale:** The prototype's purpose is to demonstrate the visual and structural improvement to the client. A single file is easier to share, review, and iterate on. The multi-page architecture is defined in specs for the production build.

**Alternative considered:** Multi-page prototype. Unnecessary complexity for a client presentation artifact.

### Decision: Product catalog uses existing species data with photo placeholders

The catalog will list all 13 wood species already documented on the current site, preserving the technical descriptions (color, texture, applications). Where real product photos are not available, the design will use clearly labeled placeholder areas.

**Rationale:** The current site already has detailed species information but zero photos. The prototype must show what the catalog looks like with imagery while making clear that real photos are needed for production.

### Decision: Quote form replaces the broken contact page form

The current site has a contact form on the Contato page but it appears non-functional (WebAcappella-generated). The new site will have a prominent quote request form with fields for: subject (Orcamento/Duvida), name, phone/WhatsApp, city, product interest, and message.

**Rationale:** The benchmark penalizes zero forms and zero lead capture. A working quote form is the minimum viable conversion mechanism for a lumber yard that does custom quotes.

## Risks / Trade-offs

- **No real product photos** -> Use placeholder areas with clear "foto do produto" labels. Block production launch until at least 6 species have real photos.
- **Business hours unknown** -> Display contact info without hours. Add hours when confirmed by the business.
- **27 years claim** -> The "Empresa" page says "Ha 27 anos no mercado." This was written around 2014, making the business approximately 39 years old in 2026. Use "Mais de 35 anos" unless the client confirms the exact founding year.
- **Email domain inconsistency** -> The site lists both @madeireirabaiasul.com.br and @madeiraireirabaiasul.com.br (typo). Use only the correctly spelled domain email.
- **CEP present only on some pages** -> Standardize: always show full address with CEP 88108-140.

## Open Questions

- Exact founding year and current years-in-market claim.
- Current business hours and days of operation.
- Whether the business has real product/project photos available.
- Whether the WhatsApp number (48) 99122-8781 is still the preferred contact.
- Whether the business serves delivery beyond Grande Florianopolis.
