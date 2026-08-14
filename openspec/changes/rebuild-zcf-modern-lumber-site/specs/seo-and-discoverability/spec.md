## Purpose

Defines the SEO, semantic HTML, metadata, structured data, heading hierarchy, and geographic service area optimization requirements for ZCF Madeireira's standalone site. The current directory listing has: a present but generic H1 (about the directory, not ZCF), absent meta description, absent schema.org markup, partial alt text on images, and no individual page SEO. SEO score is 5.6/19.5.

The directory does have one major SEO asset: 100+ geographic keyword phrases ("Madeira tratada em [bairro] em [cidade]") across 5 cities. The standalone site should capture this local SEO value with proper structure.

## ADDED Requirements

### Requirement: Page has a semantic heading hierarchy specific to ZCF
The site SHALL use exactly one H1 containing ZCF's business name and primary keyword, with H2 headings for each major content section.

#### Scenario: Home page headings
- **WHEN** a crawler or accessibility tool inspects the home page
- **THEN** it finds exactly one H1 (e.g., "ZCF Madeireira - Madeira Tratada em Palhoca e Grande Florianopolis") and H2 headings for sections like "Nossos Produtos", "Sobre a ZCF", "Areas de Atendimento", "Solicite um Orcamento"

#### Scenario: Product section headings
- **WHEN** the products section is inspected
- **THEN** each product application category (Decks, Pergolados, Cercas, etc.) appears as an H3 heading under the products H2

#### Scenario: Service area section headings
- **WHEN** the service area section is inspected
- **THEN** each city name (Florianopolis, Sao Jose, Palhoca, Biguacu, Santo Amaro da Imperatriz) appears as an H3 heading under the service area H2

### Requirement: Meta description targets local treated-wood search intent
The site SHALL include a unique, descriptive meta description that references ZCF, treated wood, autoclave treatment, and service region.

#### Scenario: Meta description content
- **WHEN** a search engine reads the page metadata
- **THEN** the meta description is non-empty, between 120-160 characters, and includes "ZCF Madeireira", "madeira tratada", and at least one city reference (currently: no meta description at all on the directory)

#### Scenario: Title tag is keyword-rich and ZCF-specific
- **WHEN** a search engine reads the title tag
- **THEN** the title includes ZCF's business name, "madeira tratada", and service region — e.g., "ZCF Madeireira | Madeira Tratada em Palhoca - Florianopolis - Biguacu, SC" (currently: directory title mentions "Florianopolis Melhores Precos" which is generic and not ZCF-specific)

### Requirement: All images have descriptive alt text
The site SHALL provide non-empty, descriptive alt text for every image element.

#### Scenario: Product images
- **WHEN** a product card includes an image
- **THEN** the alt text describes the product shown (e.g., "Deck de madeira tratada em autoclave - ZCF Madeireira") rather than being a filename like "ZCF-MADEIREIRA_LOGO"

#### Scenario: Logo image
- **WHEN** the ZCF logo is displayed
- **THEN** the alt text is "ZCF Madeireira - Madeira Tratada" (currently: "ZCF-MADEIREIRA_LOGO" which is the raw filename)

#### Scenario: Decorative images
- **WHEN** an image is purely decorative
- **THEN** it uses `alt=""` with `role="presentation"` or is applied via CSS background

### Requirement: JSON-LD structured data describes the business
The site SHALL include valid JSON-LD structured data using schema.org LocalBusiness type with all available business details.

#### Scenario: LocalBusiness schema
- **WHEN** a search engine or rich-result validator processes the page
- **THEN** it finds a valid LocalBusiness JSON-LD block containing: name ("ZCF Madeireira"), address (R. Alvaro Joao Ferreira, 04, Guarda do Cubatao, Palhoca, SC, 88135-349), telephone, URL, sameAs (Instagram), and areaServed covering Florianopolis, Sao Jose, Palhoca, Biguacu, and Santo Amaro da Imperatriz (currently: zero schema.org on the directory)

#### Scenario: Product structured data
- **WHEN** a product card is rendered
- **THEN** it includes Product schema with name, description, category ("Madeira Tratada"), and a quote-based offer indication (not implying checkout availability)

### Requirement: Open Graph metadata supports social sharing
The site SHALL include Open Graph metadata for proper display when shared on WhatsApp, Instagram, or social media.

#### Scenario: WhatsApp share preview
- **WHEN** someone shares the ZCF site URL on WhatsApp
- **THEN** the preview shows "ZCF Madeireira", a descriptive snippet about treated wood, and the ZCF logo or a representative product image

### Requirement: Canonical URL uses HTTPS on ZCF's own domain
The site SHALL declare a canonical URL using HTTPS on zcfmadeireira.com.br.

#### Scenario: Canonical tag present
- **WHEN** the HTML source is inspected
- **THEN** a `<link rel="canonical" href="https://zcfmadeireira.com.br/">` tag is present (currently: the directory's canonical points to madeiratratada.floripa.br, not to ZCF)

### Requirement: Semantic HTML replaces directory listing structure
The site SHALL use semantic HTML5 elements (header, nav, main, section, article, footer) instead of existing Elementor-generated nested div structure.

#### Scenario: Crawler inspects page structure
- **WHEN** a crawler reads the HTML document
- **THEN** it finds semantic landmarks: header (with nav), main (with sections), and footer — not Elementor-generated class names like "elementor-element" and "jet-listing-dynamic-field"

### Requirement: Geographic service area content uses semantic structure
The site SHALL organize the 100+ bairro listings into a structured, crawlable format rather than the current flat paragraph of repeated phrases.

#### Scenario: Service area is crawlable
- **WHEN** a search engine crawls the service area section
- **THEN** it finds city names as H3 headings and bairros as structured lists under each city, not as a single paragraph of "Madeira tratada no [bairro] em [cidade]" repeated 100+ times with `<br>` tags (the current directory approach)

#### Scenario: Geographic keywords are preserved
- **WHEN** the service area section content is compared to the directory's geographic listings
- **THEN** all 5 cities and their bairros from the directory are present in the standalone site, preserving the local SEO keyword coverage
