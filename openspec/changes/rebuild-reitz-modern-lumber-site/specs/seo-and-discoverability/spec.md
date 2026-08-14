## Purpose

Defines the SEO, semantic HTML, metadata, structured data, lang tag fix, heading hierarchy, and image accessibility requirements for Reitz's rebuild. The current site has several SEO issues despite having some good practices:

**What's broken:**
- `lang="en-US"` on a 100% Portuguese site
- H1 tag misused on every product title (12+ H1s on a single page instead of 1)
- Canonical URL uses HTTP instead of HTTPS
- Zero schema.org markup
- Server returns ~1023 bytes to crawlers (PHP includes failing)
- Scripts reference discontinued HTTP URLs

**What's good (preserve):**
- Title tag is well-targeted: "Reitz Esquadrias e Madeiras - Barreiros, Sao Jose, SC"
- Meta description is niche-specific: "Fabrica de portas de madeira, janelas de madeira e esquadrias de madeira em tamanhos padrao ou sob medida."
- ALL 12 product images have descriptive alt text — best image accessibility in the benchmark
- Viewport meta tag is present

SEO score is 6.0/19.5.

## ADDED Requirements

### Requirement: HTML lang attribute is pt-BR
The site SHALL declare `lang="pt-BR"` on the html element — the current `lang="en-US"` is incorrect for a 100% Portuguese-language site.

#### Scenario: Language declaration
- **WHEN** a crawler or accessibility tool inspects the html element
- **THEN** it finds `<html lang="pt-BR">` (currently: `<html lang="en-US">`)

### Requirement: Exactly one H1 per page with business identity
The site SHALL use exactly one H1 per page containing the business name and primary keyword. The current site misuses H1 on every product title (e.g., `<h1 class="portfolio-title-below">Porta Pivotante</h1>`) resulting in 12+ H1s on a single page.

#### Scenario: Home page H1
- **WHEN** a crawler inspects the home page
- **THEN** it finds exactly one H1: "Reitz Esquadrias e Madeiras - Portas e Janelas de Madeira em Sao Jose, SC" (currently: 12+ H1 tags, one per product)

#### Scenario: Heading hierarchy
- **WHEN** the document outline is inspected
- **THEN** it follows: H1 (business identity) > H2 (section titles: Produtos, Empresa, Contato) > H3 (category names: Portas, Janelas) > H4 (individual products: Porta Pivotante, Janela Bay Window)

### Requirement: Meta description preserves niche targeting
The site SHALL keep the existing meta description's niche focus on esquadrias while expanding it to include the custom sizing differentiator and service region.

#### Scenario: Meta description content
- **WHEN** a search engine reads the page metadata
- **THEN** the meta description is 120-160 characters, includes "esquadrias de madeira", "portas", "janelas", "Sao Jose", and "sob medida" — enhancing the current description which already targets the niche well

#### Scenario: Title tag enhancement
- **WHEN** a search engine reads the title tag
- **THEN** the title includes business name, product niche, and city — e.g., "Reitz Esquadrias e Madeiras | Portas e Janelas de Madeira em Sao Jose, SC" (current title is good but can be enhanced with product keywords)

### Requirement: All images preserve descriptive alt text
The site SHALL maintain descriptive alt text on all product images — Reitz's current standard is the best in the benchmark and must not be degraded.

#### Scenario: Product images retain alt text
- **WHEN** product images are rendered
- **THEN** each image has the same or improved descriptive alt text as the current site: "Porta Pivotante", "Janela Bay Window de Madeira", "Batentes de Madeira", etc.

#### Scenario: New images added in rebuild
- **WHEN** new images are added (hero backgrounds, decorative elements)
- **THEN** content images have descriptive alt text, decorative images use `alt=""` with `role="presentation"` or CSS backgrounds

#### Scenario: Alt text includes material context
- **WHEN** a product image alt text is written
- **THEN** it includes "de Madeira" suffix where applicable (following the current pattern: "Janela Bay Window de Madeira", "Batentes de Madeira") to reinforce the wood/esquadrias niche for image search

### Requirement: JSON-LD structured data describes the business and products
The site SHALL include valid JSON-LD structured data using schema.org types for LocalBusiness and Product categories.

#### Scenario: LocalBusiness schema
- **WHEN** a search engine processes the page
- **THEN** it finds a valid LocalBusiness JSON-LD block containing: name ("Reitz Esquadrias e Madeiras"), address (Av. Leoberto Leal, 699, Barreiros, Sao Jose, SC, 88117-001), telephone ("(48) 3246-0129"), email ("contato@esquadriasreitz.com.br"), URL, founding date (1993), and description mentioning esquadrias manufacturing

#### Scenario: Product structured data
- **WHEN** a product category section is rendered
- **THEN** it includes Product schema with name, description, category ("Esquadrias de Madeira"), and availability indication (quote-based, not implying checkout)

### Requirement: Open Graph metadata supports social sharing
The site SHALL include Open Graph metadata for proper WhatsApp and social media preview — important because the primary contact channel is WhatsApp.

#### Scenario: WhatsApp share preview
- **WHEN** someone shares the site URL on WhatsApp
- **THEN** the preview shows "Reitz Esquadrias e Madeiras", a descriptive snippet about portas/janelas/esquadrias, and a representative product image

### Requirement: Canonical URL uses HTTPS
The site SHALL declare a canonical URL using HTTPS protocol.

#### Scenario: Canonical tag
- **WHEN** the HTML source is inspected
- **THEN** a `<link rel="canonical" href="https://www.esquadriasreitz.com.br/">` tag is present (currently: `http://www.esquadriasreitz.com.br/` — HTTP)

### Requirement: Semantic HTML replaces the Nevada theme layout
The site SHALL use semantic HTML5 elements (header, nav, main, section, article, footer) instead of the current theme-based div structure with class names like "lambda_widget_contact", "portfolio-title-below", and "service-columns".

#### Scenario: Crawler inspects page structure
- **WHEN** a crawler reads the HTML document
- **THEN** it finds semantic landmarks: header (with nav), main (with sections for products, about, contact), and footer — not nested divs with theme-specific classes and IE conditional blocks
