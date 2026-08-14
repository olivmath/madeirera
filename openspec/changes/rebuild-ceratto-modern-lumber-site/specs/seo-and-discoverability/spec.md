## Purpose

Defines the complete SEO overhaul for Ceratto Madeiras — rewriting the keyword-stuffed title, adding missing meta description, fixing the worst heading hierarchy in the benchmark (8 H1 tags on one page), adding alt text to 15 of 16 images, adding JSON-LD structured data, and Open Graph metadata. Current SEO score is 7.8/19.5.

## ADDED Requirements

### Requirement: Title tag is concise and keyword-relevant
The site SHALL use a title tag under 60 characters containing the business name, product category, and city.

#### Scenario: Title tag content
- **WHEN** a search engine or browser reads the title tag
- **THEN** the title is "Ceratto Madeiras — Madeireira em Biguacu SC" (55 chars) replacing the current 150+ character keyword-stuffed title: "Ceratto Madeiras – Sua madeireira em Biguacu e Regiao – A Ceratto Madeiras e a sua madeireira em Biguacu e Regiao. Temos as melhores madeiras para diversos usos..."

#### Scenario: Moveis page title
- **WHEN** the Moveis e Construcoes page is loaded
- **THEN** the title is "Moveis Rusticos e Madeira para Construcao | Ceratto Madeiras" (max 60 chars), distinct from the home page title

### Requirement: Meta description targets local search intent
The site SHALL include a unique meta description between 120-160 characters referencing the business, products, and location.

#### Scenario: Home page meta description
- **WHEN** a search engine reads the home page metadata
- **THEN** the meta description is: "Madeiras tratadas, moveis rusticos e kit tabuas em Biguacu. Itauba, cambara, garapeira, cedro e mais. Ligue ou envie WhatsApp." (currently: ABSENT — zero meta description)

#### Scenario: SERP display
- **WHEN** the site appears in Google search results
- **THEN** the snippet shows the concise title and descriptive meta description instead of the current truncated 150-char keyword-stuffed title

### Requirement: Exactly one H1 per page with proper heading hierarchy
The site SHALL use exactly one H1 per page containing the primary topic, with H2 for sections and H3 for items within sections.

#### Scenario: Home page headings
- **WHEN** a crawler inspects the home page
- **THEN** it finds exactly 1 H1 (e.g., "Madeiras de Qualidade Vindas do Norte do Pais"), with H2s for sections ("Nosso Catalogo", "Moveis e Construcoes", "Madeira para Diversos Usos", "Fale Conosco"), and H3s for product names (Itauba, Cambara, etc.) — currently: 2 H1 tags on home page alone, benchmark reports 8 H1 across all pages

#### Scenario: Moveis page headings
- **WHEN** a crawler inspects the Moveis e Construcoes page
- **THEN** it finds exactly 1 H1 ("Moveis e Construcoes"), with H2s for product categories and H3s for individual items — currently: prices (R$450,00, R$200,00) are incorrectly marked as H2

#### Scenario: Prices are not headings
- **WHEN** the heading hierarchy is inspected
- **THEN** no price values (R$450, R$200, R$150) appear as H2 or any heading level — they use paragraph or span elements (currently: 4 price values are marked as H2)

### Requirement: All images have descriptive alt text
The site SHALL provide descriptive alt text for every content image, and proper handling for decorative images.

#### Scenario: Product images have species-specific alt text
- **WHEN** a product card image is rendered
- **THEN** the alt text describes the specific wood species, e.g., "Madeira Itauba - madeira nobre de alta durabilidade para decks e construcao" — not empty string (currently: 15 of 16 images have alt="", the worst ratio in the benchmark for a site with this many images)

#### Scenario: Logo image retains existing alt text
- **WHEN** the logo image is rendered
- **THEN** the alt text remains "Ceratto Madeiras – Sua madeireira em Biguacu e Regiao" (this is the only image with alt text currently)

#### Scenario: Decorative images use appropriate markup
- **WHEN** a decorative image (divider, background) is rendered
- **THEN** it uses `alt=""` with `role="presentation"` or is applied via CSS background-image

### Requirement: JSON-LD structured data describes the business
The site SHALL include valid JSON-LD structured data using schema.org LocalBusiness type.

#### Scenario: LocalBusiness schema
- **WHEN** a rich-result validator processes the page
- **THEN** it finds a valid LocalBusiness JSON-LD block containing:
  - name: "Ceratto Madeiras"
  - address: Rua Sebastiao Lara, 300, Universitario, Biguacu, SC
  - telephone: "(48) 3285-3293"
  - email: "cerattomadeiras@gmail.com"
  - url: "https://cerattomadeiras.com.br"
  - openingHours: "Mo-Fr 08:00-12:00, Mo-Fr 13:30-18:00"
  - areaServed: Biguacu, Florianopolis, Sao Jose, Palhoca, Garopaba, Itapema, Balneario Camboriu
  (currently: zero schema.org markup of any kind)

#### Scenario: Product structured data
- **WHEN** a priced product card is rendered
- **THEN** it includes Product schema with name, description, price, priceCurrency (BRL), and availability

### Requirement: Open Graph metadata supports social sharing
The site SHALL include Open Graph metadata for proper display when shared on WhatsApp or social media.

#### Scenario: WhatsApp share preview
- **WHEN** someone shares cerattomadeiras.com.br on WhatsApp
- **THEN** the preview shows: title "Ceratto Madeiras — Madeireira em Biguacu SC", description snippet, and a representative image (logo or hero) — not a blank or auto-generated preview

### Requirement: Canonical URL is declared
The site SHALL declare a canonical URL using HTTPS on the preferred domain.

#### Scenario: Canonical tag
- **WHEN** the HTML source is inspected
- **THEN** a `<link rel="canonical" href="https://cerattomadeiras.com.br/">` tag is present (HTTPS is already active on the site)

### Requirement: HTML lang attribute is correct
The site SHALL declare `lang="pt-BR"` on the html element.

#### Scenario: Language declaration
- **WHEN** the HTML source is inspected
- **THEN** the html element has `lang="pt-BR"` (currently: `lang="en-US"` — incorrect for Portuguese content)
