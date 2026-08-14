## Context

See `proposal.md` for motivation. Ceratto Madeiras scores 50.0/100 — a "Fraco" classification. Unlike the lowest-scoring sites that need full rebuilds, Ceratto has a functional WordPress site with Elementor, the Astra theme (responsive), real product photos, visible pricing, and working WhatsApp integration. The problems are structural (SEO, headings, alt text, forms) rather than visual.

The site serves Biguacu and the broader Grande Florianopolis region, selling lumber (itauba, cambara, garapeira, cedro, tatajuba, angelim pedra, roxinho, longarina) plus rustic furniture products (cutting boards, BBQ boards, petisqueiras) with visible prices.

## Goals / Non-Goals

**Goals:**

- Fix the 8-H1-per-page problem (worst in benchmark) with proper heading hierarchy.
- Add alt text to all 15 images currently missing it.
- Rewrite the keyword-stuffed title tag (150+ chars) to under 60 characters.
- Add meta description (currently absent).
- Add a quote/contact form (currently zero forms exist).
- Fix the broken Moveis e Construcoes page (404).
- Add JSON-LD LocalBusiness structured data.
- Improve product showcase with proper image alt text and descriptions.
- Preserve existing pricing display (Kit Tabuas R$450, Tabua Churrasco R$200, Petisqueiras R$150).

**Non-Goals:**

- No full site rebuild — the WordPress/Elementor/Astra stack is adequate.
- No e-commerce checkout, cart, or online payment.
- No customer accounts or login system.
- No domain email migration (Gmail is a business decision, not a prototype concern).
- No CMS migration — stays on WordPress.
- No custom theme development — Astra works.

## Decisions

### Decision: Surgical fix within existing WordPress/Elementor, not full rebuild

The prototype will demonstrate what the fixed site looks like as a single HTML file, but the actual implementation path is fixing the existing WordPress site, not replacing it.

**Rationale:** Ceratto already has a responsive layout (Astra theme), real product photos, working WhatsApp integration, and Elementor page builder. The score is 50/100, not 19.5/100 — the problems are fixable within the existing stack. A full rebuild would be unnecessary cost.

**Alternative considered:** Full rebuild from scratch (like Baia Sul). Rejected because the existing infrastructure works; only the content structure is broken.

### Decision: Keep existing warm color palette

The site already uses warm wood tones (#db9423 amber/gold, #935620 brown, #ed7a00 orange hover) with Poppins/Roboto typography. This palette correctly communicates "lumber yard" and scores well on UI.

**Rationale:** The current visual identity is one of Ceratto's strengths (UI score 8.2/15 is decent). The palette matches competitors who score higher. No visual redesign needed.

### Decision: Single-page HTML prototype for client presentation

The prototype will be a self-contained HTML file demonstrating the improved structure, proper headings, alt text, form, and SEO elements — showing what the fixed site should look like.

**Rationale:** Demonstrates all improvements in one shareable file. The production implementation would apply these changes within WordPress/Elementor.

### Decision: Preserve existing product pricing

The site uniquely displays actual prices (R$450, R$200, R$150 for specific products). These will be preserved exactly as-is in the prototype.

**Rationale:** Visible pricing is a competitive advantage — most competitors use "sob consulta." Changing or removing prices would reduce conversion potential.

### Decision: Add quote form to contact section

A structured quote form will be added to the existing "Fale Conosco" section, alongside the current WhatsApp and phone contact options.

**Rationale:** Zero forms is a major conversion penalty. The form should capture: name, phone/WhatsApp, product interest (dropdown of wood species), and message. This complements rather than replaces the existing WhatsApp workflow.

## Risks / Trade-offs

- **Gmail email persists** -> The site uses cerattomadeiras@gmail.com. Domain email would improve trust score but is a business decision outside prototype scope. Flag as recommendation.
- **Moveis e Construcoes 404** -> The navigation link to this page is broken. The saved copy has content (prices, products). The prototype must include this content; production fix requires restoring the WordPress page.
- **8 H1 tags across pages** -> Benchmark counts across all pages. The home page alone has 2 H1s, the moveis page has 2 H1s, likely more on contact page. Each page needs exactly 1 H1.
- **Product descriptions are generic** -> Each wood species says "Madeira X de alta qualidade." The prototype should expand these with actual properties where known.
- **Tatajuba image mislabeled** -> The Tatajuba product card says "Madeira Eucalipto de alta qualidade" — this is a data error on the current site. The prototype must correct it.
- **Business hours are known** -> Monday to Friday, 08:00-12:00 and 13:30-18:00. Include in structured data.

## Open Questions

- Whether the Moveis e Construcoes page 404 is intentional (content removed) or accidental (permalink broken).
- Whether additional wood species should be added beyond the current 8 shown on the home page.
- Whether the business has a domain email available (currently only Gmail shown).
- Whether weekend hours or Saturday service exists.
