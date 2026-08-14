## Purpose

Defines the SEO, semantic HTML, metadata, structured data, heading hierarchy, and image alt text requirements to fix JL Correa's 9.3/19.5 SEO score. The current site has: 7 H1 tags (should be 1), 22 H2 tags (many decorative like "Ligue", "WhatsApp", "Segunda a Sexta"), EMPTY title tag, ABSENT meta description, zero schema.org markup, zero Open Graph, and 27 of 28 images without alt text — the second worst alt text coverage in the entire benchmark (96%).

## ADDED Requirements

### Requirement: Exactly one H1 with business name and primary keyword
The site SHALL use exactly one H1 per page containing the business name, product category, and location.

#### Scenario: Home page H1
- **WHEN** a crawler or accessibility tool inspects the home page
- **THEN** it finds exactly one H1 (e.g., "JL Correa Madeiras — Madeiras Certificadas em Palhoca, SC") replacing the current 7 H1 tags ("nome", "historia", "missao/visao", "especialidades", "produtos", "por que", "visite-nos")

#### Scenario: No decorative H1 tags
- **WHEN** the heading hierarchy is inspected
- **THEN** zero H1 tags are used for decorative or navigational purposes — all non-primary headings are H2 or lower

### Requirement: Semantic H2 headings replace decorative H2 tags
The site SHALL reduce from 22 H2 tags to approximately 6 semantic section headings, removing decorative uses like "Ligue", "WhatsApp", and "Segunda a Sexta".

#### Scenario: Section headings
- **WHEN** a crawler reads the document outline
- **THEN** H2 headings map to content sections: "Nossa Historia", "Nossos Produtos", "Galeria", "Por Que Nos Escolher", "Contato", "Localizacao" — not to UI labels like "Ligue" or "WhatsApp" (currently 22 H2 tags, many decorative)

#### Scenario: Contact details use proper markup
- **WHEN** phone numbers, WhatsApp, and hours are displayed
- **THEN** they use paragraph, list, or definition list markup — not H2 heading tags

### Requirement: Title tag is present and keyword-rich
The site SHALL include a non-empty, keyword-rich title tag replacing the current EMPTY title.

#### Scenario: Title tag content
- **WHEN** a search engine reads the title tag
- **THEN** the title is "JL Correa Madeiras — 50 Anos em Palhoca | Madeiras Certificadas" or equivalent containing: business name, years in market, city, and product category (currently: title tag is EMPTY — zero characters)

### Requirement: Meta description targets local search intent
The site SHALL include a descriptive meta description referencing the business, products, and service region.

#### Scenario: Meta description content
- **WHEN** a search engine reads the page metadata
- **THEN** the meta description is between 120-160 characters and includes "JL Correa Madeiras", "Palhoca", "madeiras certificadas", and at least one product reference (currently: ABSENT)

### Requirement: All 28 images have descriptive alt text
The site SHALL provide non-empty, descriptive alt text for every image element — fixing the catastrophic 27/28 images without alt text (96% missing, second worst in benchmark).

#### Scenario: Product/installation photos
- **WHEN** a gallery or product image is rendered
- **THEN** the alt text describes what is shown using species names, product types, and context (e.g., "Estrutura de telhado em madeira Angelim instalada pela JL Correa Madeiras" or "Tabuas de Pinus Tratado empilhadas no deposito") rather than being empty or generic

#### Scenario: Logo and icons
- **WHEN** the logo image is rendered
- **THEN** the alt text is "Logotipo JL Correa Madeiras" (currently missing)

#### Scenario: Decorative images
- **WHEN** an image is purely decorative (dividers, backgrounds)
- **THEN** it uses `alt=""` with `role="presentation"` or is applied via CSS background, not as an img with missing alt

#### Scenario: Alt text coverage validation
- **WHEN** an accessibility audit runs on the page
- **THEN** 100% of img elements have non-empty alt text (or intentional empty alt for decorative images) — up from 4% (1/28) currently

### Requirement: JSON-LD structured data describes the business
The site SHALL include valid JSON-LD structured data using schema.org LocalBusiness type.

#### Scenario: LocalBusiness schema
- **WHEN** a search engine or rich-result validator processes the page
- **THEN** it finds a valid LocalBusiness JSON-LD block containing: name ("JL Correa Madeiras"), address (R. Edeling Schutz, 135, Centro, Palhoca, SC, 88131-340), telephone ("(48) 3242-0186"), url, openingHours ("Mo-Fr 07:15-12:00, Mo-Fr 13:00-18:00"), foundingDate ("1974"), description, and service area covering Grande Florianopolis (currently: zero schema.org markup)

#### Scenario: Product structured data
- **WHEN** a product category card is rendered
- **THEN** it includes Product schema with name, description, category, and availability indication (quote-based, not implying checkout)

### Requirement: Open Graph metadata supports social sharing
The site SHALL include Open Graph metadata for proper display when shared on social media or WhatsApp.

#### Scenario: WhatsApp share preview
- **WHEN** someone shares the site URL on WhatsApp or social media
- **THEN** the preview shows "JL Correa Madeiras", a descriptive snippet about certified wood in Palhoca, and the business logo or a representative product image — rather than a blank preview (currently: no OG tags)

### Requirement: Canonical URL declared
The site SHALL declare a canonical URL using HTTPS protocol.

#### Scenario: Canonical tag present
- **WHEN** the HTML source is inspected
- **THEN** a `<link rel="canonical" href="https://jlcorreamadeiras.com.br/">` tag is present

### Requirement: Semantic HTML replaces Elementor div soup
The site SHALL use semantic HTML5 elements (header, nav, main, section, article, footer) instead of the Elementor-generated nested div structure with class names like "elementor-widget-container".

#### Scenario: Crawler inspects page structure
- **WHEN** a crawler reads the HTML document
- **THEN** it finds semantic landmarks: header (with nav), main (with sections), and footer — not deeply nested divs with Elementor class names

### Requirement: Language attribute is correct
The site SHALL declare `lang="pt-BR"` on the html element.

#### Scenario: Language declaration
- **WHEN** a crawler or screen reader inspects the page
- **THEN** the html element has `lang="pt-BR"` (the current site has this correctly — preserve it)
