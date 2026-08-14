## Purpose

Defines the SEO, metadata, structured data, heading hierarchy, and image alt text requirements to fix Cambirela's SEO gaps. The current site has: a generic title tag ("MADEIREIRA CAMBIRELA") identical across all pages, no meta description, no schema.org markup, and the majority of 30+ images with empty alt text. SEO score is 8.4/19.5.

## ADDED Requirements

### Requirement: Title tag includes business name, product category, and location
The site SHALL use a descriptive, keyword-rich title tag that differentiates it in search results.

#### Scenario: Title tag content
- **WHEN** a search engine reads the title tag
- **THEN** the title is "Madeireira Cambirela | Madeiras Tratadas em Palhoca - Grande Florianopolis, SC" (currently: generic "MADEIREIRA CAMBIRELA" on all pages)

### Requirement: Meta description targets local search intent
The site SHALL include a descriptive meta description referencing the business, products, and location.

#### Scenario: Meta description content
- **WHEN** a search engine reads the page metadata
- **THEN** the meta description is between 120-160 characters, includes "madeireira", "Palhoca", and at least one product reference (currently: ABSENT)

### Requirement: H1 includes business identity and location
The site SHALL use an H1 that combines the brand with location keywords — the current H1 is generic ("Construa com qualidade e sustentabilidade") with no mention of the business name or city.

#### Scenario: Home page H1
- **WHEN** a crawler or accessibility tool inspects the home page
- **THEN** it finds exactly one H1 containing "Madeireira Cambirela" and "Palhoca" (e.g., "Madeireira Cambirela — Madeiras Tratadas em Palhoca, SC")

#### Scenario: Section headings
- **WHEN** the page structure is inspected
- **THEN** H2 headings exist for each major section (Produtos, Nossa Empresa, Depoimentos, Contato) creating a scannable document outline

### Requirement: All images have descriptive alt text
The site SHALL provide non-empty, descriptive alt text for every content image — currently the majority of 30+ images have alt="" or alt missing.

#### Scenario: Product images
- **WHEN** a product card includes an image
- **THEN** the alt text describes the product (e.g., "Deck de pinus tratado para areas externas — Madeireira Cambirela") rather than being empty

#### Scenario: Gallery images
- **WHEN** a gallery image is rendered
- **THEN** the alt text describes the scene (e.g., "Forro de pinus tratado instalado em residencia") rather than the filename

#### Scenario: Decorative images
- **WHEN** an image is purely decorative (backgrounds, textures)
- **THEN** it uses `alt=""` with `role="presentation"` or is applied via CSS background

### Requirement: JSON-LD structured data describes the business
The site SHALL include valid JSON-LD structured data using schema.org LocalBusiness type — currently zero schema.org markup despite running WordPress.

#### Scenario: LocalBusiness schema
- **WHEN** a search engine or rich-result validator processes the page
- **THEN** it finds a valid LocalBusiness JSON-LD block containing: name ("Madeireira Cambirela"), address (R. Nereu Ghizoni, 1040, Palhoca, SC), telephone, email, URL, and service area (currently: zero schema.org markup)

### Requirement: Open Graph metadata supports social sharing
The site SHALL include Open Graph metadata for proper display when shared on social media or WhatsApp.

#### Scenario: WhatsApp share preview
- **WHEN** someone shares the site URL on WhatsApp or social media
- **THEN** the preview shows "Madeireira Cambirela", a descriptive snippet about products and location, and a representative image rather than a blank preview

### Requirement: Broken social media links are fixed
The site SHALL fix the malformed Instagram link that currently points to `http://@madeireiracambirela` — a non-functional URL.

#### Scenario: Instagram link
- **WHEN** a visitor clicks the Instagram icon in the footer
- **THEN** it navigates to `https://instagram.com/madeireiracambirela` (currently: `http://@madeireiracambirela` which is broken)

#### Scenario: Other social links
- **WHEN** the top bar social icons are rendered
- **THEN** Facebook, Twitter/X, and YouTube links point to valid URLs or are removed if no active profiles exist (currently: icons present with empty href)
