## Purpose

Defines the SEO, semantic HTML, metadata, structured data, lang attribute, heading hierarchy, and image alt text requirements to fix Fontana's technical baseline. The current site has: no H1 on home page, `lang="en-US"` instead of `lang="pt-BR"`, zero meta descriptions on any page, 8/8 home images with empty alt text (100%), and WordPress 4.3 generator tags leaking version info. Tech score is 3.3/10.5 — the worst in the entire benchmark. SEO score is 8.0/19.5.

## ADDED Requirements

### Requirement: HTML lang attribute set to pt-BR
The site SHALL declare the correct language attribute for Portuguese-Brazilian content.

#### Scenario: Language declaration
- **WHEN** a crawler or browser inspects the HTML element
- **THEN** it finds `<html lang="pt-BR">` (currently: `<html lang="en-US">` — incorrect for a Brazilian Portuguese site, causing screen readers to use wrong pronunciation and search engines to misclassify the content)

### Requirement: Every page has a semantic heading hierarchy
The site SHALL use exactly one H1 per page containing the business name and primary keyword, with H2 headings for each major content section.

#### Scenario: Home page headings
- **WHEN** a crawler or accessibility tool inspects the home page
- **THEN** it finds exactly one H1 (e.g., "Madeireira Fontana — Madeiras em Sao Jose, SC") and H2 headings for sections like "Produtos e Servicos", "Sobre a Fontana", "Depoimentos", "Contato" (currently: no H1 on home, H2s used for section titles but without the H1 parent)

#### Scenario: Product section headings
- **WHEN** the products section is inspected
- **THEN** each wood species name appears as an H3 heading under the products H2, creating a scannable document outline (currently: species names are H3 headings but orphaned without proper hierarchy)

### Requirement: Meta description targets local search intent
The site SHALL include a unique, descriptive meta description on every page.

#### Scenario: Home page meta description
- **WHEN** a search engine reads the home page metadata
- **THEN** the meta description is between 120-160 characters and includes "madeireira", "Sao Jose", and product references (currently: zero meta description on any page — completely absent)

#### Scenario: Title tag is keyword-rich and properly formatted
- **WHEN** a search engine reads the title tag
- **THEN** the title includes business name, product category, and city — e.g., "Madeireira Fontana | Madeiras, Pinus Autoclave e Moveis em Sao Jose, SC" (currently: just "Madeireira Fontana" — too generic, missing keywords and location)

### Requirement: All images have descriptive alt text
The site SHALL provide non-empty, descriptive alt text for every content image.

#### Scenario: Home page slider images
- **WHEN** the home page images are inspected
- **THEN** all images have descriptive alt text (e.g., "Estoque de madeiras Fontana — galpao com pinus autoclave") instead of `alt=""` (currently: 8/8 images on home have empty alt — 100% failure rate)

#### Scenario: Product catalog images
- **WHEN** a product card includes an image
- **THEN** the alt text describes the wood species shown (e.g., "Madeira Cumaru — textura fina, densidade alta, para assoalhos e forros")

#### Scenario: Gallery images
- **WHEN** gallery photos are rendered
- **THEN** each image has contextual alt text including the species or furniture type (currently: gallery images use generic filenames like "033" as alt text)

#### Scenario: Decorative images
- **WHEN** an image is purely decorative (backgrounds, dividers)
- **THEN** it uses `alt=""` with `role="presentation"` or is applied via CSS background

### Requirement: JSON-LD structured data describes the business
The site SHALL include valid JSON-LD structured data using schema.org LocalBusiness type.

#### Scenario: LocalBusiness schema
- **WHEN** a search engine or rich-result validator processes the page
- **THEN** it finds a valid LocalBusiness JSON-LD block containing: name ("Madeireira Fontana"), address (Rua Italia n200, Serraria, Sao Jose, SC, 88115-360), telephone ((48) 3258-1500), email (vendas@fontanamadeireira.com.br), URL, founding date (1985-08-09), and payment methods accepted (currently: zero schema.org for LocalBusiness — only Review markup exists on testimonials)

#### Scenario: Product structured data
- **WHEN** a product card is rendered with sufficient detail
- **THEN** it includes Product schema with name, description, category ("Madeira"), and availability indication

### Requirement: Preserve and enhance existing Schema.org/Review markup
The site SHALL maintain the Schema.org/Review structured data already present on testimonials and ensure it validates correctly.

#### Scenario: Review markup validation
- **WHEN** the testimonials section is crawled
- **THEN** each testimonial has valid itemscope/itemtype Review markup with reviewBody and author Person — matching or improving the current implementation

### Requirement: Open Graph metadata supports social sharing
The site SHALL include Open Graph metadata for proper display when shared on WhatsApp, Instagram, or Facebook.

#### Scenario: WhatsApp share preview
- **WHEN** someone shares the site URL on WhatsApp
- **THEN** the preview shows "Madeireira Fontana", a descriptive snippet about the business, and a representative image of the lumber yard or products

### Requirement: Canonical URL uses HTTPS on correct domain
The site SHALL declare a canonical URL using HTTPS protocol.

#### Scenario: Canonical tag present
- **WHEN** the HTML source is inspected
- **THEN** a `<link rel="canonical" href="https://fontanamadeireira.com.br/">` tag is present (the site currently has a canonical but some internal links use HTTP instead of HTTPS — e.g., CTA buttons link to `http://fontanamadeireira.com.br/contato`)

#### Scenario: No mixed HTTP/HTTPS content
- **WHEN** internal links are inspected
- **THEN** all links use HTTPS consistently (currently: logo src uses HTTP `http://fontanamadeireira.com.br/wp-content/uploads/...` and several CTA buttons link to HTTP URLs)

### Requirement: Remove WordPress version leaks and unnecessary meta tags
The site SHALL not expose CMS version information or unnecessary generator tags.

#### Scenario: No version disclosure
- **WHEN** the HTML source is inspected
- **THEN** there are no `<meta name="generator" content="WordPress 4.3.34">` tags, no Visual Composer generator tags, no Revolution Slider version tags, and no XML-RPC pingback links (currently: 3 generator meta tags expose exact versions of WordPress, Visual Composer, and Revolution Slider)

### Requirement: Semantic HTML replaces Visual Composer output
The site SHALL use semantic HTML5 elements (header, nav, main, section, article, footer) instead of the current Visual Composer-generated div soup with classes like `vc_row`, `wpb_column`, `vc_column_container`.

#### Scenario: Crawler inspects page structure
- **WHEN** a crawler reads the HTML document
- **THEN** it finds semantic landmarks: header (with nav), main (with sections), and footer — not nested divs with VC-generated class names
