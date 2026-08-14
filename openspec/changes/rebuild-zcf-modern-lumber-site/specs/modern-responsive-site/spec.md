## Purpose

Defines the responsive layout, mobile-first design, navigation, hero section, product showcase, service area section, footer, and overall site structure for ZCF Madeireira's first standalone web presence. Currently, ZCF exists only as a card listing on a third-party directory (madeiratratada.floripa.br) with no independent site, no product pages, and no form-based lead capture.

## ADDED Requirements

### Requirement: Site uses mobile-first responsive layout
The site SHALL render correctly on all viewport widths from 320px to 1920px+ without horizontal scrolling, text overflow, or layout breakage.

#### Scenario: Mobile visitor opens the site
- **WHEN** a visitor opens the site on a 375px-wide mobile screen
- **THEN** the layout adapts to the viewport width, text is readable without zooming, and all interactive elements are tappable (minimum 44x44px touch targets)

#### Scenario: Desktop visitor opens the site
- **WHEN** a visitor opens the site on a 1440px desktop screen
- **THEN** the layout uses the available width with a max-width container, product cards display in a multi-column grid, and navigation is fully visible

#### Scenario: Viewport meta tag is present
- **WHEN** the HTML source is inspected
- **THEN** a `<meta name="viewport" content="width=device-width, initial-scale=1">` tag is present in the head

### Requirement: Hero section positions ZCF as a treated-wood specialist
The site SHALL present ZCF's positioning as a treated-wood specialist with autoclave treatment, 25+ years in market, service region, and primary CTA in the first meaningful viewport.

#### Scenario: Visitor lands on home page
- **WHEN** a visitor opens the home page
- **THEN** the visitor can identify: (1) business name "ZCF Madeireira", (2) specialization "Madeira Tratada em Autoclave", (3) service region "Palhoca, Florianopolis e Grande Florianopolis", (4) a CTA to request a quote or contact via WhatsApp — all without scrolling on a 667px-tall mobile viewport

#### Scenario: Hero includes trust signals
- **WHEN** a visitor views the hero section
- **THEN** the hero includes at least two trust signals: years in market ("Mais de 25 anos") and treatment quality ("Tratamento industrial certificado em autoclave") as text, not as image-only elements

#### Scenario: Hero differentiates from generic lumber yards
- **WHEN** a visitor views the hero section
- **THEN** the messaging clearly communicates treated wood specialization (protection against termites, fungi, moisture, rot) rather than generic "madeireira" positioning

### Requirement: Navigation supports all site sections
The site SHALL provide navigation to products, about/company, service areas, contact/quote, and social links.

#### Scenario: Mobile navigation
- **WHEN** a visitor opens the site on mobile
- **THEN** the navigation collapses into a hamburger/toggle menu that expands to show all section links

#### Scenario: Desktop navigation
- **WHEN** a visitor opens the site on desktop
- **THEN** all navigation links are visible in a horizontal bar without requiring a menu toggle

#### Scenario: Navigation includes quote CTA
- **WHEN** a visitor views the navigation bar
- **THEN** at least one navigation element links directly to the quote/contact section, visually distinguished as a CTA (button style, contrasting color)

### Requirement: Product catalog displays treated wood applications
The site SHALL display treated wood product categories organized by application (not by wood species), each with name, description, use cases, benefits, and a photo area.

#### Scenario: Visitor browses products
- **WHEN** a visitor scrolls to or navigates to the products section
- **THEN** the visitor sees cards or tiles for at least 6 application categories: casas de madeira, decks, pergolados, cercas, estruturas rurais, estruturas urbanas — each with application name as heading, description, benefits of treated wood for that use, and a designated image area

#### Scenario: Product cards on mobile
- **WHEN** a visitor views products on a mobile viewport
- **THEN** product cards stack in a single column with full-width layout, readable text, and tappable quote CTA per card

#### Scenario: Product cards on desktop
- **WHEN** a visitor views products on a desktop viewport
- **THEN** product cards display in a 2-3 column grid layout

#### Scenario: Each product card shows autoclave treatment badge
- **WHEN** a product card is displayed
- **THEN** it includes a visual indicator (badge, icon, or label) confirming the product uses autoclave-treated wood

### Requirement: Service area section organizes geographic coverage by city
The site SHALL display ZCF's service coverage across 5 cities and 100+ bairros in a structured, SEO-friendly format.

#### Scenario: Visitor checks service area
- **WHEN** a visitor navigates to the service area section
- **THEN** the section displays 5 city groups (Florianopolis, Sao Jose, Palhoca, Biguacu, Santo Amaro da Imperatriz) with bairros listed under each city

#### Scenario: Service area on mobile
- **WHEN** a visitor views the service area on mobile
- **THEN** cities are displayed as expandable/collapsible groups (accordion) to avoid excessive scrolling

#### Scenario: Service area headings are semantic
- **WHEN** the service area section is inspected
- **THEN** each city name is an H3 heading under the section's H2, creating a scannable document outline for crawlers

### Requirement: Footer displays complete contact information
The site SHALL display all business contact details in the footer: full address with CEP, phone number, WhatsApp link, Instagram link, and map link.

#### Scenario: Visitor checks footer
- **WHEN** a visitor scrolls to the footer
- **THEN** the footer shows: R. Alvaro Joao Ferreira, 04 - Guarda do Cubatao - Palhoca - SC - CEP 88135-349, phone as click-to-call, WhatsApp as click-to-chat, Instagram link, and a "ver no mapa" link

#### Scenario: Footer on mobile
- **WHEN** a visitor views the footer on mobile
- **THEN** contact items stack vertically with adequate spacing and all links are tappable

### Requirement: Site uses a warm, lumber-appropriate visual identity
The site SHALL use a color palette with warm wood tones (browns, creams) and forest green accent that communicates "treated wood specialist."

#### Scenario: Visual identity communicates product category
- **WHEN** a visitor opens the site
- **THEN** the color scheme, imagery, and typography create an immediate visual association with wood/lumber rather than a generic corporate or tech identity

#### Scenario: Green accent conveys preservation/treatment
- **WHEN** green is used as accent color
- **THEN** it reinforces the "treated/preserved wood" positioning (green = durability, protection, nature)

#### Scenario: Accessibility contrast requirements
- **WHEN** text is displayed on any background
- **THEN** the color combination meets WCAG AA contrast ratio (4.5:1 for body text, 3:1 for large text)
