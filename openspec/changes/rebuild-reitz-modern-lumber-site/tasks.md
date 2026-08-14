## 1. Infrastructure And SSL Resolution

- [ ] 1.1 Document the SSL issue: current cert belongs to uni5.net, does not cover esquadriasreitz.com.br.
- [ ] 1.2 Plan SSL fix: Let's Encrypt certificate for esquadriasreitz.com.br and www.esquadriasreitz.com.br.
- [ ] 1.3 Verify server can serve complete HTML (currently PHP includes fail, returning ~1023 bytes to crawlers).

## 2. Content Extraction And Validation

- [ ] 2.1 Extract and organize all text content from the current site (done — see `content.md`).
- [ ] 2.2 Download all 20 product images from the current site (hosted on esquadriasreitz.com.br and solucao782.tagx.com.br).
- [ ] 2.3 Confirm business details with client: founding year (1993?), current hours, WhatsApp number, payment methods, service scope.

## 3. Responsive Site Structure

- [ ] 3.1 Build mobile-first HTML structure with semantic elements: header, nav, main, sections, footer.
- [ ] 3.2 Build responsive navigation with hamburger menu on mobile, horizontal menu on desktop. Menu items: Home, Empresa, Produtos (with sub-menu), Servicos, Portfolio, Contato, Orcamento.
- [ ] 3.3 Build hero section with esquadrias positioning, "fabricacao propria" differentiator, and primary CTAs (WhatsApp + quote form).
- [ ] 3.4 Build about section highlighting 33+ years manufacturing esquadrias, own factory, Barreiros/Sao Jose location.
- [ ] 3.5 Build product showcase with 4 category sections: Portas (Pivotante, Estilo Mineiro, Georgia, Windsor), Janelas (Bay Window, Maxim-Ar, Basculante, Correr), Rodapes/Batentes/Guarnicoes (Batentes, Rodapes, Filetes, Vistas), Fechaduras/Dobradicas/Puxadores.
- [ ] 3.6 Build contact/quote section with structured form for custom esquadrias.
- [ ] 3.7 Build footer with full address (Av. Leoberto Leal, 699 - Barreiros, Sao Jose/SC, 88117-001), phone, WhatsApp, email, product links, payment methods.
- [ ] 3.8 Add viewport meta tag and responsive CSS ensuring no horizontal scroll on any device width.

## 4. SEO And Semantic Structure

- [ ] 4.1 Fix lang attribute: change `lang="en-US"` to `lang="pt-BR"`.
- [ ] 4.2 Add one proper H1 per page (currently H1 is misused on every product title — 12+ H1s on a single page).
- [ ] 4.3 Add H2 headings for each major section, H3 for product categories, H4 for individual products.
- [ ] 4.4 Preserve descriptive alt text on all product images (e.g., "Porta Pivotante", "Janela Bay Window de Madeira").
- [ ] 4.5 Update title tag: "Reitz Esquadrias e Madeiras | Portas e Janelas de Madeira em Sao Jose, SC".
- [ ] 4.6 Update meta description targeting local search + esquadrias niche.
- [ ] 4.7 Add Open Graph metadata (og:title, og:description, og:image, og:url).
- [ ] 4.8 Add JSON-LD structured data for LocalBusiness with name, address, phone, email, geo coordinates.
- [ ] 4.9 Add Product structured data for each product category.
- [ ] 4.10 Fix canonical URL to use HTTPS (currently `http://www.esquadriasreitz.com.br/`).

## 5. Conversion And Lead Capture

- [ ] 5.1 Build a quote request form with fields: tipo (Orcamento/Duvida), nome (required), telefone/WhatsApp (required), email, produto de interesse (select from categories), medida (padrao/sob medida), mensagem.
- [ ] 5.2 Add visible CTA buttons in hero section ("Solicite um Orcamento", "Fale pelo WhatsApp").
- [ ] 5.3 Add CTA on each product card linking to WhatsApp with product name prefilled.
- [ ] 5.4 Configure sticky WhatsApp button (bottom-left, matching current position) with correct number 5548999831254.
- [ ] 5.5 Add click-to-call link on phone number (48) 3246-0129.
- [ ] 5.6 Add click-to-email link on contato@esquadriasreitz.com.br.
- [ ] 5.7 Add form validation with visible error/success states.

## 6. Visual Design And Assets

- [ ] 6.1 Define color palette: warm wood tones (rich browns, creams, craft green accent) replacing the current gray (#666666) and teal (#2C97C3).
- [ ] 6.2 Select typography: clean sans-serif for body (Open Sans already used), craftsman-style for headings.
- [ ] 6.3 Create product card layout with photo area, product name (preserving alt text), category badge, and quote CTA.
- [ ] 6.4 Add wood texture or workshop imagery to hero section.
- [ ] 6.5 Ensure sufficient contrast ratios for accessibility (WCAG AA minimum).

## 7. Quality Gates

- [ ] 7.1 Validate mobile rendering: no horizontal scroll, readable text without zoom, tappable buttons (min 44x44px).
- [ ] 7.2 Validate SEO checklist: H1 present (only one), lang="pt-BR", meta description, structured data valid, all images have alt text.
- [ ] 7.3 Validate conversion paths: WhatsApp link works with correct number, form submits, phone number clickable.
- [ ] 7.4 Validate accessibility: keyboard navigation, form labels, contrast, semantic landmarks.
- [ ] 7.5 Re-score against benchmark rubric — target: UI 11+/15, UX 15+/20, SEO 14+/19.5, Conversao 18+/25, Tech 8+/10.5, Recomendacao 7+/10. Total 70+/100.
