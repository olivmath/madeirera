## Purpose

Defines the SEO, semantic HTML, metadata, structured data, and heading hierarchy requirements to fix Santa Isabel's zero-SEO baseline. The current Adobe Muse site has: zero H1/H2 headings, 57 images with zero alt text (100%), menu text rendered as PNG images instead of real text, no schema.org markup, and a title/meta description that exist but are underoptimized. SEO score: 6.7/19.5.

## ADDED Requirements

### Requirement: Every page has a semantic heading hierarchy
The site SHALL use exactly one H1 per page containing the business name and primary keyword, with H2 headings for each major content section.

#### Scenario: Home page headings
- **WHEN** a crawler or accessibility tool inspects the home page
- **THEN** it finds exactly one H1 (e.g., "Madeireira Santa Isabel - Casas Pre-Fabricadas em Palhoca, SC") and H2 headings for sections like "Nossa Historia", "Nossos Projetos", "Sustentabilidade", "Solicite um Orcamento", "Dicas de Construcao" (currently: zero H1, zero H2 — Adobe Muse outputs all text as styled divs/spans)

#### Scenario: Project section headings
- **WHEN** the projects section is inspected
- **THEN** project categories ("Casas de Madeira", "Casas de Alvenaria e Concreto") appear as H3 headings under the projects H2

#### Scenario: Wood species section headings
- **WHEN** the raw materials section is inspected
- **THEN** each wood species name (Pinus, Eucalipto, Angelim, Itauba, Garapeira) appears as an H3 heading under a materials H2

### Requirement: Meta description targets local search intent for pre-fabricated houses
The site SHALL include a unique, descriptive meta description that references the business, product specialization, heritage, and service region.

#### Scenario: Meta description content
- **WHEN** a search engine reads the page metadata
- **THEN** the meta description is between 120-160 characters and includes "casas pre-fabricadas", "Palhoca", and "desde 1945" (current meta desc exists but is generic: "empresa especializada em Casas Pre-Fabricadas. Localizada no Municipio de Palhoca")

#### Scenario: Title tag leverages heritage
- **WHEN** a search engine reads the title tag
- **THEN** the title includes the business name, specialization, city, and heritage — e.g., "Madeireira Santa Isabel | Casas Pre-Fabricadas em Palhoca, SC | Desde 1945" (current: "Madeireira Santa Isabel - Home")

### Requirement: All images have descriptive alt text
The site SHALL provide non-empty, descriptive alt text for every image element, fixing the current 57-image, 100% alt-text deficit.

#### Scenario: Project photos
- **WHEN** a project gallery includes an image
- **THEN** the alt text describes the project shown (e.g., "Casa pre-fabricada de madeira construida pela Madeireira Santa Isabel em Palhoca") rather than being empty (currently: all 57 images have alt="" or no alt attribute)

#### Scenario: Heritage/facility photos
- **WHEN** the heritage or facility section includes images
- **THEN** the alt text describes the content (e.g., "Patio da Madeireira Santa Isabel com 1200m2 - area de armazenamento de madeira")

#### Scenario: Logo images
- **WHEN** the logo is displayed
- **THEN** the alt text reads "Madeireira Santa Isabel - Desde 1945" (currently: alt="" on both logo instances)

#### Scenario: Decorative images
- **WHEN** an image is purely decorative (dividers, backgrounds, section icons)
- **THEN** it uses `alt=""` with `role="presentation"` or is applied via CSS background, not as an img with missing alt

### Requirement: JSON-LD structured data describes the business with founding date
The site SHALL include valid JSON-LD structured data using schema.org LocalBusiness type with all available business details, including the 1945 founding date.

#### Scenario: LocalBusiness schema
- **WHEN** a search engine or rich-result validator processes the page
- **THEN** it finds a valid LocalBusiness JSON-LD block containing: name ("Madeireira Santa Isabel"), address (BR 101 - Km 217, Pachecos, Palhoca, SC), telephone ((48) 98454-1738), email (contato@madeireirasantaisabel.com.br), foundingDate (1945), openingHours (Mo-Fr 09:00-12:00, Mo-Fr 14:00-18:00), sameAs (Facebook, YouTube, Instagram URLs), and service area covering Santa Catarina (currently: zero schema.org markup)

#### Scenario: Product structured data for house types
- **WHEN** project categories are rendered
- **THEN** they include Product or Service schema with name ("Casa Pre-Fabricada de Madeira", "Casa Pre-Fabricada de Alvenaria"), description, and a quote-based offer indication

### Requirement: Open Graph metadata supports social sharing
The site SHALL include Open Graph metadata for proper display when shared on social media or messaging apps — especially important since the business has active Facebook, YouTube, and Instagram accounts.

#### Scenario: WhatsApp/Facebook share preview
- **WHEN** someone shares the site URL on WhatsApp, Facebook, or Instagram
- **THEN** the preview shows "Madeireira Santa Isabel", a descriptive snippet mentioning casas pre-fabricadas and the 1945 heritage, and a representative image — rather than a blank or generic preview

### Requirement: Canonical URL uses HTTPS on the business domain
The site SHALL declare a canonical URL using HTTPS protocol.

#### Scenario: Canonical tag present
- **WHEN** the HTML source is inspected
- **THEN** a `<link rel="canonical" href="https://madeireirasantaisabel.com.br/">` tag is present (the site has HTTPS active but no canonical declaration)

### Requirement: Semantic HTML replaces Adobe Muse absolute-positioned divs
The site SHALL use semantic HTML5 elements (header, nav, main, section, article, footer) instead of the current Adobe Muse-generated div soup with absolute positioning and CSS-sprite menu text.

#### Scenario: Crawler inspects page structure
- **WHEN** a crawler reads the HTML document
- **THEN** it finds semantic landmarks: header (with nav containing real text links), main (with sections), and footer — not the current Adobe Muse structure of absolutely-positioned divs with class names like "PamphletWidget", "MenuItemLabel", "ThumbGroup", and menu items rendered as PNG sprites instead of text

#### Scenario: Menu items are real text
- **WHEN** navigation is inspected
- **THEN** menu items ("Home", "Projetos", "Show Room", "Contato", etc.) are rendered as actual text in anchor elements, not as `<img>` tags pointing to blank.gif with alt text as the only readable content (the current Adobe Muse pattern)

### Requirement: Wood species content is indexable
The site SHALL present the 5 wood species descriptions (Pinus, Eucalipto, Angelim, Itauba, Garapeira) as structured, indexable text content with proper headings.

#### Scenario: Species page indexing
- **WHEN** a search engine crawls the materials section
- **THEN** each species has: an H3 heading with the species name, a text paragraph with characteristics and applications, and structured markup — making the content indexable for searches like "madeira itauba Palhoca" or "pinus construcao Santa Catarina"
