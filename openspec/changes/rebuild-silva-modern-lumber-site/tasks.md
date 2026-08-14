## 1. Content Extraction And Validation

- [ ] 1.1 Extract and organize all text content from the current Lovable SPA (done — see `content.md`).
- [ ] 1.2 Confirm business details with client: preferred WhatsApp number, hours accuracy, Instagram/YouTube status.
- [ ] 1.3 Catalog all 27 existing images and write alt text for the 15+ currently missing it.

## 2. Responsive Site Structure

- [ ] 2.1 Build pre-rendered HTML structure with semantic elements: header, nav, main, sections, footer.
- [ ] 2.2 Build responsive navigation with hamburger menu on mobile, horizontal menu on desktop — matching current sections (Inicio, Produtos, Sobre Nos, Blog, Contato).
- [ ] 2.3 Build hero section preserving the image slider, tagline "Transformando lares com madeira sustentavel," trust signals (57 anos, 3a geracao), and primary CTAs.
- [ ] 2.4 Build about section with company history (1960 founding, 1968 serraria, 3rd generation), sustainability commitment, and Deep Fitting technology showcase.
- [ ] 2.5 Build product catalog with individual pages for: Kit Casa, Deck/Pergolado, Aberturas, Madeiras em Geral, Eucalipto — each with images, descriptions, and quote CTA.
- [ ] 2.6 Build contact/quote section with structured form (nome, telefone, produto de interesse, mensagem) and all contact channels.
- [ ] 2.7 Build footer with both addresses (Alto Aririu + Jardim Eldorado), phone, email, CNPJ, hours, social links, and map links.
- [ ] 2.8 Build testimonials section with the 6+ Google reviews (4.9/5, 70 reviews).

## 3. SEO And Semantic Structure

- [ ] 3.1 Set correct title: "Madeireira Silva | Madeiras Sustentaveis em Palhoca SC | 57 Anos."
- [ ] 3.2 Add H1 per page with descriptive, keyword-relevant content.
- [ ] 3.3 Write meta description: "Madeireira Silva em Palhoca SC. Madeiras de reflorestamento, deck, pergolado, kit casa e aberturas. 57 anos, 3a geracao. Orcamento pelo WhatsApp."
- [ ] 3.4 Add alt text to all 27 images — descriptive, keyword-rich.
- [ ] 3.5 Add JSON-LD LocalBusiness for both locations (Alto Aririu + Jardim Eldorado).
- [ ] 3.6 Add JSON-LD AggregateRating (4.9/5, 70 reviews).
- [ ] 3.7 Add JSON-LD Product markup for each product category page.
- [ ] 3.8 Add Open Graph metadata (og:title, og:description, og:image, og:url).
- [ ] 3.9 Add canonical URL using HTTPS on madeireirasilva.ind.br.
- [ ] 3.10 Set lang="pt-BR" (current site has lang="en").

## 4. Conversion And Lead Capture

- [ ] 4.1 Build a quote request form with fields: nome (required), telefone/WhatsApp (required), produto de interesse (select from catalog), mensagem.
- [ ] 4.2 Add visible CTAs in hero and after each product section ("Solicite um Orcamento", "Fale pelo WhatsApp").
- [ ] 4.3 Consolidate WhatsApp integration: single number (48) 99858-5524, contextual prefilled messages per page/product.
- [ ] 4.4 Add click-to-call on phone number and click-to-email on contato@madeireirasilva.ind.br.
- [ ] 4.5 Add form validation with visible error/success states.
- [ ] 4.6 Add product interest pre-selection when arriving at form from a product page.

## 5. Visual Design And Assets

- [ ] 5.1 Preserve current warm green/wood color palette from the Lovable design.
- [ ] 5.2 Reproduce hero image slider with CSS transitions (no React dependency).
- [ ] 5.3 Reproduce product card layout with images, descriptions, and quote CTAs.
- [ ] 5.4 Reproduce Deep Fitting technology showcase section.
- [ ] 5.5 Ensure WCAG AA contrast ratios on all text/background combinations.

## 6. Quality Gates

- [ ] 6.1 Validate: all content is present in HTML source (not behind JS execution).
- [ ] 6.2 Validate mobile rendering: no horizontal scroll, readable text, tappable buttons (min 44x44px).
- [ ] 6.3 Validate SEO: H1 present, meta description present, structured data valid (test with Google Rich Results Test), all images have alt text, lang="pt-BR".
- [ ] 6.4 Validate conversion: form submits, WhatsApp links work with prefilled messages, phone is clickable.
- [ ] 6.5 Re-score against benchmark rubric — target: UI 11+/15, UX 14+/20, SEO 14+/19.5, Conversao 16+/25, Tech 8+/10.5, Recomendacao 7+/10. Total 70+/100.
