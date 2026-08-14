## Purpose

Defines the SEO, semantic HTML, metadata, structured data, and heading hierarchy requirements to fix Baia Sul's zero-SEO baseline. The current site has: zero H1/H2 headings, empty meta description, empty keywords, zero schema.org markup, only 1 image with empty alt text, and a generic title tag. SEO score is 2.4/19.5.

## ADDED Requirements

### Requirement: Every page has a semantic heading hierarchy
The site SHALL use exactly one H1 per page containing the business name and primary keyword, with H2 headings for each major content section.

#### Scenario: Home page headings
- **WHEN** a crawler or accessibility tool inspects the home page
- **THEN** it finds exactly one H1 (e.g., "Madeireira Baia Sul - Madeiras em Sao Jose, SC") and H2 headings for sections like "Nossos Produtos", "Sobre a Empresa", "Solicite um Orcamento" (currently: zero H1, zero H2)

#### Scenario: Product section headings
- **WHEN** the products section is inspected
- **THEN** each wood species name appears as an H3 heading under the products H2, creating a scannable document outline

### Requirement: Meta description targets local search intent
The site SHALL include a unique, descriptive meta description that references the business, product categories, and service region.

#### Scenario: Meta description content
- **WHEN** a search engine reads the page metadata
- **THEN** the meta description is non-empty, between 120-160 characters, and includes "madeireira", "Sao Jose", and at least one product reference (currently: empty string)

#### Scenario: Title tag is keyword-rich
- **WHEN** a search engine reads the title tag
- **THEN** the title includes the business name, product category, and city — e.g., "Madeireira Baia Sul | Madeiras em Sao Jose - Florianopolis - Palhoca, SC" (currently: generic "Madeireira Baia Sul - Sao Jose - Florianopolis - Palhoca")

### Requirement: All images have descriptive alt text
The site SHALL provide non-empty, descriptive alt text for every image element.

#### Scenario: Product images
- **WHEN** a product card or section includes an image
- **THEN** the alt text describes the wood species shown (e.g., "Madeira Jatoba - cerne castanho-claro-rosado para assoalhos e moveis") rather than being empty or generic (currently: 1 image with alt="")

#### Scenario: Decorative images
- **WHEN** an image is purely decorative (dividers, backgrounds)
- **THEN** it uses `alt=""` with `role="presentation"` or is applied via CSS background, not as an img with missing alt

### Requirement: JSON-LD structured data describes the business
The site SHALL include valid JSON-LD structured data using schema.org LocalBusiness type with all available business details.

#### Scenario: LocalBusiness schema
- **WHEN** a search engine or rich-result validator processes the page
- **THEN** it finds a valid LocalBusiness JSON-LD block containing: name ("Madeireira Baia Sul"), address (Rua Francisco Pedro Cunha, 567, Rocado, Sao Jose, SC, 88108-140), telephone, email, URL, and service area covering Sao Jose, Florianopolis, and Palhoca (currently: zero schema.org markup)

#### Scenario: Product structured data
- **WHEN** a product card is rendered with sufficient detail
- **THEN** it includes Product schema with name, description, category, and a quote-based offer indication (not implying checkout availability)

### Requirement: Open Graph metadata supports social sharing
The site SHALL include Open Graph metadata (og:title, og:description, og:image, og:url, og:type) for proper display when shared on social media or messaging apps.

#### Scenario: WhatsApp share preview
- **WHEN** someone shares the site URL on WhatsApp or social media
- **THEN** the preview shows the business name, a descriptive snippet, and a representative image rather than a blank or generic preview

### Requirement: Canonical URL uses HTTPS
The site SHALL declare a canonical URL using HTTPS protocol on the preferred domain.

#### Scenario: Canonical tag present
- **WHEN** the HTML source is inspected
- **THEN** a `<link rel="canonical" href="https://baiasul.com.br/">` tag is present (the site already has HTTPS active but no canonical declaration)

### Requirement: Semantic HTML replaces table/div layout
The site SHALL use semantic HTML5 elements (header, nav, main, section, article, footer) instead of the current WebAcappella-generated table and absolutely-positioned div layout.

#### Scenario: Crawler inspects page structure
- **WHEN** a crawler reads the HTML document
- **THEN** it finds semantic landmarks: header (with nav), main (with sections), and footer — not nested tables and absolutely-positioned divs with generated class names like "wa-comp" and "waDynmenu-item"
