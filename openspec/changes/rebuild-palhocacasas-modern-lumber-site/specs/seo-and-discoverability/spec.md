## Purpose

Defines the SEO, semantic HTML, metadata, structured data, and heading hierarchy requirements to fix Palhoca Casas de Madeira's SEO deficiencies. The current site has: 2 duplicate H1 tags ("CASAS DE MADEIRA NA PALHOCA" and "Vamos comecar?"), zero meta description, zero Open Graph, zero schema.org markup, a generic title tag ("Palhoca Casas de madeira"), and all 5 images with empty alt text. SEO score is 2.0/19.5.

## ADDED Requirements

### Requirement: Page has exactly one semantic H1 with primary keyword
The site SHALL use exactly one H1 per page containing the business identity and primary keyword, fixing the current duplicate H1 problem.

#### Scenario: Home page H1
- **WHEN** a crawler or accessibility tool inspects the home page
- **THEN** it finds exactly one H1 (e.g., "Casas de Madeira Pre-Fabricadas em Palhoca, SC") and H2 headings for sections like "Nossos Modelos", "Sobre Nos", "Galeria", "Solicite um Orcamento" (currently: 2 H1 tags — "CASAS DE MADEIRA NA PALHOCA" and "Vamos comecar?")

#### Scenario: Section headings use H2/H3
- **WHEN** the document outline is inspected
- **THEN** each major section uses H2, house models use H3 under the models H2, and no other H1 tags exist on the page — the "Vamos comecar?" CTA section uses H2, not H1

### Requirement: Meta description targets local pre-fab house search intent
The site SHALL include a unique, descriptive meta description that references the business, product niche (casas pre-fabricadas), and service region.

#### Scenario: Meta description content
- **WHEN** a search engine reads the page metadata
- **THEN** the meta description is non-empty, between 120-160 characters, and includes "casas de madeira", "Palhoca", and "pre-fabricadas" (currently: completely absent)

#### Scenario: Title tag is keyword-rich and specific
- **WHEN** a search engine reads the title tag
- **THEN** the title includes the business name, product niche, and region — e.g., "Palhoca Casas de Madeira | Casas Pre-Fabricadas em Palhoca - Grande Florianopolis, SC" (currently: generic "Palhoca Casas de madeira")

### Requirement: All images have descriptive alt text
The site SHALL provide non-empty, descriptive alt text for every content image.

#### Scenario: House model images
- **WHEN** a house model card includes a photo
- **THEN** the alt text describes the model (e.g., "Casa de madeira pre-fabricada modelo Araucaria - 45m2 - 2 quartos") rather than being empty (currently: all 5 images have alt="")

#### Scenario: Logo images
- **WHEN** the company logo is displayed
- **THEN** the alt text is "Palhoca Casas de Madeira - Logo" rather than empty

#### Scenario: Caixa logo
- **WHEN** the Caixa Economica Federal logo is displayed as a trust signal
- **THEN** the alt text is "Financiamento pela Caixa Economica Federal" rather than empty

#### Scenario: Decorative images
- **WHEN** an image is purely decorative (backgrounds, dividers)
- **THEN** it uses `alt=""` with `role="presentation"` or is applied via CSS background

### Requirement: JSON-LD structured data describes the business
The site SHALL include valid JSON-LD structured data using schema.org LocalBusiness type with all available business details.

#### Scenario: LocalBusiness schema
- **WHEN** a search engine or rich-result validator processes the page
- **THEN** it finds a valid LocalBusiness JSON-LD block containing: name ("Palhoca Casas de Madeira"), address (Rua Capitao Pedro Egydio Hoffmann, 107 - Palhoca, SC), telephone ((48) 99108-8224), URL, openingHoursSpecification (08:00-22:00, 7 days), and service area covering Grande Florianopolis (currently: zero schema.org markup)

#### Scenario: Product structured data for house models
- **WHEN** a house model card is rendered
- **THEN** it includes Product schema with name, description, category ("Casa de Madeira Pre-Fabricada"), and availability indication (quote-based, not implying checkout)

### Requirement: Open Graph metadata supports social sharing
The site SHALL include Open Graph metadata (og:title, og:description, og:image, og:url, og:type) for proper display when shared on WhatsApp or social media.

#### Scenario: WhatsApp share preview
- **WHEN** someone shares the site URL on WhatsApp
- **THEN** the preview shows the business name, a descriptive snippet about casas de madeira pre-fabricadas, and a representative house image rather than a blank or generic preview (currently: no OG metadata exists)

### Requirement: Canonical URL uses HTTPS on preferred domain
The site SHALL declare a canonical URL using HTTPS on the www-prefixed domain.

#### Scenario: Canonical tag present
- **WHEN** the HTML source is inspected
- **THEN** a `<link rel="canonical" href="https://www.palhocacasasdemadeira.com.br/">` tag is present (the site already has a canonical tag — verify it points to the correct preferred domain)

### Requirement: Semantic HTML replaces Elementor div-soup
The site SHALL use semantic HTML5 elements (header, nav, main, section, article, footer) instead of the current Elementor-generated nested div structure with data-elementor-* attributes.

#### Scenario: Crawler inspects page structure
- **WHEN** a crawler reads the HTML document
- **THEN** it finds semantic landmarks: header (with nav), main (with sections for models, about, gallery, contact), and footer — not nested divs with Elementor class names and data attributes
