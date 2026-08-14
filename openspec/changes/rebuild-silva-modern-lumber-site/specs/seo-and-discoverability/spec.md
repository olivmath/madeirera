## Purpose

Defines the SEO, semantic HTML, metadata, structured data, image alt text, and crawlability requirements to fix Silva's SEO deficiencies. The current site has: title "MadeireiraSilva" (no space, no location), lang="en" for Portuguese content, 15+ of 27 images without alt text, zero schema.org markup despite having 4.9/5 Google rating with 70 reviews, and all content behind client-side JS rendering. SEO score is 9.0/19.5.

## ADDED Requirements

### Requirement: Title tag includes business name, product, and location
The site SHALL use a descriptive title tag with proper spacing, product category, and location for local SEO.

#### Scenario: Title tag content
- **WHEN** a search engine reads the title tag
- **THEN** the title is "Madeireira Silva | Madeiras Sustentaveis em Palhoca SC | 57 Anos" — with proper spacing between words and location included (currently: "MadeireiraSilva" — no space, no location)

#### Scenario: Product page titles
- **WHEN** a search engine reads a product page title
- **THEN** the title includes the product name and location, e.g., "Deck e Pergolado | Madeireira Silva - Palhoca SC"

### Requirement: Every page has a semantic heading hierarchy
The site SHALL use exactly one H1 per page with H2 headings for each major content section.

#### Scenario: Home page headings
- **WHEN** a crawler inspects the home page
- **THEN** it finds exactly one H1 (e.g., "Madeireira Silva - Madeiras Sustentaveis em Palhoca") and H2 headings for sections: "Nossos Produtos", "Sobre Nos", "Depoimentos", "Fale Conosco" (currently: SPA renders H1 "Transformando lares com madeira sustentavel!" but behind JS)

#### Scenario: Product page headings
- **WHEN** a product page is inspected
- **THEN** it has one H1 with the product name (e.g., "Kit Casa em Madeira") and H2 headings for subsections

### Requirement: Meta description targets local search intent
The site SHALL include a unique meta description per page referencing the business, products, and service region.

#### Scenario: Home page meta description
- **WHEN** a search engine reads the home page metadata
- **THEN** the meta description is 120-160 characters, includes "Madeireira Silva", "Palhoca", and product references (currently: "Transformando lares com madeira sustentavel 57 anos de historia | 3a geracao" — descriptive but missing location keywords)

#### Scenario: Product page meta descriptions
- **WHEN** a search engine reads a product page
- **THEN** each product page has a unique meta description referencing the specific product and location

### Requirement: All 27 images have descriptive alt text
The site SHALL provide non-empty, descriptive alt text for every image element, fixing the 15+ currently missing.

#### Scenario: Product images
- **WHEN** a product page includes an image
- **THEN** the alt text describes what is shown (e.g., "Deck de madeira Pinus tratado com acabamento natural - Madeireira Silva") — not empty or generic (currently: 15+ images have no alt text)

#### Scenario: Hero images
- **WHEN** the hero slider displays images
- **THEN** the first (visible) image has descriptive alt text; subsequent slides may use `alt=""` as decorative since the same content is repeated (currently: all hero images have `alt=""`)

#### Scenario: Decorative images
- **WHEN** an image is purely decorative
- **THEN** it uses `alt=""` with `role="presentation"` or is applied via CSS background

### Requirement: JSON-LD LocalBusiness describes both locations
The site SHALL include valid JSON-LD structured data for both physical locations.

#### Scenario: LocalBusiness schema
- **WHEN** a search engine processes the page
- **THEN** it finds valid LocalBusiness JSON-LD with: name ("Madeireira Silva"), both addresses (Alto Aririu and Jardim Eldorado), telephone, email, URL, opening hours (Seg-Qui 07:30-18:00, Sex 07:30-17:00), and geo coordinates (currently: zero schema.org markup)

#### Scenario: Multi-location handling
- **WHEN** structured data is validated
- **THEN** the two locations are represented as either two LocalBusiness entities or one with two locations, following schema.org best practices

### Requirement: AggregateRating schema surfaces the 4.9/5 rating
The site SHALL include AggregateRating structured data reflecting the Google reviews.

#### Scenario: Rating in search results
- **WHEN** a search engine processes the structured data
- **THEN** it finds a valid AggregateRating with ratingValue "4.9", bestRating "5", reviewCount "70" — enabling star rating rich snippets in SERPs (currently: zero structured data despite having the best Google rating among all benchmarked competitors)

### Requirement: Product structured data per product page
The site SHALL include Product schema.org markup on each product category page.

#### Scenario: Product schema
- **WHEN** a product page is processed by a rich-result validator
- **THEN** it contains Product JSON-LD with: name, description, category, image, and an offer indication as "sob consulta" (not implying checkout availability)

### Requirement: Open Graph metadata supports social sharing
The site SHALL include Open Graph metadata for proper display when shared on social media or messaging apps.

#### Scenario: WhatsApp share preview
- **WHEN** someone shares the site URL on WhatsApp
- **THEN** the preview shows "Madeireira Silva", a descriptive snippet, and a representative image (currently: shows "MadeireiraSilva" with no space)

### Requirement: Document language is set to Portuguese
The site SHALL declare the correct language attribute.

#### Scenario: Language attribute
- **WHEN** the HTML source is inspected
- **THEN** the `<html>` tag has `lang="pt-BR"` (currently: `lang="en"` — incorrect for Portuguese content)

### Requirement: Canonical URL uses HTTPS on the primary domain
The site SHALL declare a canonical URL.

#### Scenario: Canonical tag
- **WHEN** the HTML source is inspected
- **THEN** a `<link rel="canonical" href="https://madeireirasilva.ind.br/">` tag is present

### Requirement: Semantic HTML replaces SPA div structure
The site SHALL use semantic HTML5 elements instead of the current single `<div id="root">` container.

#### Scenario: Crawler inspects page structure
- **WHEN** a crawler reads the HTML document
- **THEN** it finds semantic landmarks: `<header>` (with `<nav>`), `<main>` (with `<section>` elements), and `<footer>` — not a single empty div that gets populated by JavaScript
