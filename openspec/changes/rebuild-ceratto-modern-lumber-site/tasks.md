## 1. SEO Critical Fixes

- [ ] 1.1 Rewrite title tag from 150+ chars to max 60: "Ceratto Madeiras — Madeireira em Biguacu SC".
- [ ] 1.2 Add meta description: "Madeiras tratadas, moveis rusticos e kit tabuas em Biguacu. Itauba, cambara, garapeira, cedro e mais. Ligue ou envie WhatsApp."
- [ ] 1.3 Fix heading hierarchy on home page: keep 1 H1 ("Ceratto Madeiras — Madeireira em Biguacu e Regiao"), demote "Fale Conosco" from H1 to H2.
- [ ] 1.4 Fix heading hierarchy on Moveis e Construcoes page: keep 1 H1 ("Moveis e Construcoes — Ceratto Madeiras"), demote prices from H2 to paragraph/span.
- [ ] 1.5 Add descriptive alt text to all 15 images missing it (see content.md for exact alt text per image).
- [ ] 1.6 Fix Tatajuba product description from "Madeira Eucalipto de alta qualidade" to "Madeira Tatajuba de alta qualidade".

## 2. Structured Data And Metadata

- [ ] 2.1 Add JSON-LD LocalBusiness: name "Ceratto Madeiras", address "Rua Sebastiao Lara, 300, Universitario, Biguacu, SC", phone "(48) 3285-3293", WhatsApp "(48) 99961-1658", hours "Mo-Fr 08:00-12:00, 13:30-18:00".
- [ ] 2.2 Add Open Graph metadata: og:title, og:description, og:image (logo), og:url, og:type=website.
- [ ] 2.3 Add canonical URL: `<link rel="canonical" href="https://cerattomadeiras.com.br/">`.
- [ ] 2.4 Fix lang attribute from "en-US" to "pt-BR".

## 3. Conversion And Lead Capture

- [ ] 3.1 Add quote request form with fields: nome (required), telefone/WhatsApp (required), tipo de madeira (dropdown: Itauba, Cambara, Garapeira, Cedro, Tatajuba, Angelim Pedra, Roxinho, Longarina, Outro), mensagem.
- [ ] 3.2 Add form to the "Fale Conosco" section alongside existing WhatsApp and phone info.
- [ ] 3.3 Add product-specific WhatsApp prefilled messages: "Ola, vim pelo site da Ceratto Madeiras e gostaria de um orcamento de [PRODUTO]."
- [ ] 3.4 Add "Solicite um Orcamento" CTA button in hero section linking to form.
- [ ] 3.5 Add form validation with visible error/success states.

## 4. Navigation And Content Fixes

- [ ] 4.1 Fix broken Moveis e Construcoes link (currently 404 from navigation).
- [ ] 4.2 Ensure all navigation items resolve: Inicio, Moveis e Construcoes, Contato.
- [ ] 4.3 Consolidate contact info in footer: phone (click-to-call), WhatsApp (click-to-chat), email (mailto), address, hours, service area.

## 5. Product Showcase Improvements

- [ ] 5.1 Add expanded descriptions for 8 wood species (replace generic "Madeira X de alta qualidade" with properties and applications).
- [ ] 5.2 Include priced products from Moveis page: Kit Tabuas R$450, Tabua Churrasco R$200, Petisqueira R$150.
- [ ] 5.3 Add "Pedir Orcamento" CTA per product card linking to form with product pre-selected.

## 6. Prototype Build

- [ ] 6.1 Build single-page HTML prototype with all fixes applied: proper headings, alt text, meta tags, form, structured data.
- [ ] 6.2 Include all sections: hero, about/quality, product catalog (8 species), moveis e construcoes (priced items), applications, contact/form, footer.
- [ ] 6.3 Use existing color palette (#db9423 amber, #935620 brown, Poppins/Roboto fonts).

## 7. Quality Gates

- [ ] 7.1 Validate: exactly 1 H1 per page, no prices as H2, proper heading nesting.
- [ ] 7.2 Validate: all 16 images have descriptive alt text.
- [ ] 7.3 Validate: meta description present and 120-160 chars.
- [ ] 7.4 Validate: title tag under 60 chars.
- [ ] 7.5 Validate: JSON-LD valid per schema.org.
- [ ] 7.6 Validate: form submits with validation, WhatsApp links work, phone numbers are click-to-call.
- [ ] 7.7 Re-score against benchmark — target: UI 10+/15, UX 14+/20, SEO 15+/19.5, Conversao 18+/25, Tech 8+/10.5, Recomendacao 6+/10. Total 70+/100.
