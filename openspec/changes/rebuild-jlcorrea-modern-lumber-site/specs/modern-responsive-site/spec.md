## Purpose

Defines the restructured layout, navigation, hero section, product showcase, gallery, and overall site architecture that replaces JL Correa's flat single-page Elementor structure. The current site has decent visual design (UI: 11.2/15) but broken semantic structure: 7 H1 tags, 22 H2 tags (many decorative), and no indexable sub-pages for long-tail SEO. The rebuild preserves the clean visual identity while fixing the structural foundation.

## ADDED Requirements

### Requirement: Site uses mobile-first responsive layout
The site SHALL render correctly on all viewport widths from 320px to 1920px+ without horizontal scrolling, text overflow, or layout breakage — preserving the clean Elementor aesthetic.

#### Scenario: Mobile visitor opens the site
- **WHEN** a visitor opens the site on a 375px-wide mobile screen
- **THEN** the layout adapts to the viewport width, text is readable without zooming, and all interactive elements are tappable (minimum 44x44px touch targets)

#### Scenario: Desktop visitor opens the site
- **WHEN** a visitor opens the site on a 1440px desktop screen
- **THEN** the layout uses the available width with a max-width container, product categories display in a multi-column grid, and navigation is fully visible

#### Scenario: Viewport meta tag is present
- **WHEN** the HTML source is inspected
- **THEN** a `<meta name="viewport" content="width=device-width, initial-scale=1">` tag is present in the head

### Requirement: Hero section communicates 50-year legacy and certified products
The site SHALL present JL Correa's positioning, certification claim, family history anchor, and primary CTA in the first meaningful viewport.

#### Scenario: Visitor lands on home page
- **WHEN** a visitor opens the home page
- **THEN** the visitor can identify: (1) business name "JL Correa Madeiras", (2) tagline "Tradicao e Qualidade desde 1974", (3) certified wood claim, (4) service region "Grande Florianopolis", (5) a CTA to request a quote or contact via WhatsApp — all without scrolling on a 667px-tall mobile viewport

#### Scenario: Hero includes trust signals
- **WHEN** a visitor views the hero section
- **THEN** the hero includes at least two trust signals: "50+ anos de historia" and "madeiras certificadas" as text, not as image-only elements

### Requirement: Navigation supports all site sections
The site SHALL provide navigation to home, about/history, products, gallery, contact/quote — with responsive behavior.

#### Scenario: Mobile navigation
- **WHEN** a visitor opens the site on mobile
- **THEN** the navigation collapses into a hamburger/toggle menu that expands to show all section links

#### Scenario: Desktop navigation
- **WHEN** a visitor opens the site on desktop
- **THEN** all navigation links are visible in a horizontal bar without requiring a menu toggle

#### Scenario: Navigation includes quote CTA
- **WHEN** a visitor views the navigation bar
- **THEN** at least one navigation element links directly to the quote/contact section, visually distinguished as a CTA (button style, contrasting color)

### Requirement: About section preserves the 3-generation family narrative
The site SHALL display the company history with the family timeline (1974 founding, second generation, Joao Luiz Correa) and mission/vision/values, using proper semantic headings instead of the current 7-H1 structure.

#### Scenario: Visitor reads the about section
- **WHEN** a visitor navigates to the about section
- **THEN** the visitor sees: founding story (1974, Luiz Inacio Correa), generational transitions, current leadership, and mission/vision/values — all under a single H2 heading with H3 sub-headings, not multiple H1 tags

#### Scenario: Timeline is scannable
- **WHEN** a visitor glances at the history section
- **THEN** the 3-generation timeline is presented visually (timeline component, cards, or structured list) rather than as a wall of text

### Requirement: Product showcase organizes offerings by category
The site SHALL display products organized by the 3 business categories: Madeiras Certificadas, Vendas de Aberturas, and Atendimento Personalizado — each with description, available species/products, and a quote CTA.

#### Scenario: Visitor browses products
- **WHEN** a visitor scrolls to or navigates to the products section
- **THEN** the visitor sees cards or tiles for each category with: category name as heading, description, list of available products/species, representative image with alt text, and a "Solicite um Orcamento" CTA

#### Scenario: Product cards on mobile
- **WHEN** a visitor views products on a mobile viewport
- **THEN** product category cards stack in a single column with full-width layout, readable text, and tappable quote CTA per card

#### Scenario: Product cards on desktop
- **WHEN** a visitor views products on a desktop viewport
- **THEN** product category cards display in a 2-3 column grid layout

### Requirement: Gallery section displays all photos with descriptive alt text
The site SHALL display the existing 24+ product and installation photos in a responsive gallery grid, with every image having descriptive alt text (fixing the current 27/28 images without alt).

#### Scenario: Visitor browses gallery
- **WHEN** a visitor views the gallery section
- **THEN** all photos display in a responsive grid with descriptive alt text on every image (e.g., "Tabuas de Cambara empilhadas no deposito da JL Correa Madeiras" rather than empty alt)

#### Scenario: Gallery on mobile
- **WHEN** a visitor views the gallery on mobile
- **THEN** images display in a 1-2 column grid with tap-to-enlarge behavior

### Requirement: Footer displays complete contact information
The site SHALL display all business contact details in the footer: full address with CEP, phone, WhatsApp, social media links, and business hours.

#### Scenario: Visitor checks footer
- **WHEN** a visitor scrolls to the footer
- **THEN** the footer shows: R. Edeling Schutz, 135, Centro, Palhoca - SC, CEP 88131-340, phone (48) 3242-0186 as click-to-call, WhatsApp (48) 9 9697-3814, business hours, Instagram link, and copyright notice

#### Scenario: Footer on mobile
- **WHEN** a visitor views the footer on mobile
- **THEN** contact items stack vertically with adequate spacing and all links are tappable

### Requirement: Site preserves the existing clean visual identity
The site SHALL maintain the warm, clean aesthetic established by the current Elementor design — no radical color or typography changes.

#### Scenario: Visual continuity
- **WHEN** a visitor familiar with the current site opens the rebuilt version
- **THEN** the visual identity (colors, typography feel, spacing) is recognizably the same brand, even though the structure has improved

#### Scenario: Accessibility contrast requirements
- **WHEN** text is displayed on any background
- **THEN** the color combination meets WCAG AA contrast ratio (4.5:1 for body text, 3:1 for large text)
