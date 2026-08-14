## Purpose

Defines the responsive layout, mobile-first design, house model showcase, photo gallery, navigation, hero section, footer, and overall site structure that enhances Palhoca Casas de Madeira's current minimal single-page Elementor layout. The current site has a viewport meta tag but wastes it on a single page with only 5 images, 2 nav items, and no house model catalog despite being a pre-fabricated house specialist. UI score is 7.0/15, UX score is 9.0/20.

## ADDED Requirements

### Requirement: Site uses mobile-first responsive layout
The site SHALL render correctly on all viewport widths from 320px to 1920px+ without horizontal scrolling, text overflow, or layout breakage.

#### Scenario: Mobile visitor opens the site
- **WHEN** a visitor opens the site on a 375px-wide mobile screen
- **THEN** the layout adapts to the viewport width, text is readable without zooming, and all interactive elements are tappable (minimum 44x44px touch targets)

#### Scenario: Desktop visitor opens the site
- **WHEN** a visitor opens the site on a 1440px desktop screen
- **THEN** the layout uses the available width with a max-width container, house model cards display in a multi-column grid, and navigation is fully visible

### Requirement: Hero section communicates pre-fab house identity and trust signals
The site SHALL present the pre-fabricated wooden house positioning, Caixa financing badge, extended hours, and primary CTA in the first meaningful viewport — replacing the current sparse hero that buries differentiators.

#### Scenario: Visitor lands on home page
- **WHEN** a visitor opens the home page
- **THEN** the visitor can identify: (1) "Casas de Madeira Pre-Fabricadas em Palhoca", (2) Caixa Economica financing badge, (3) extended hours indicator (08:00-22:00), (4) a CTA to request a quote or contact via WhatsApp — all without scrolling on a 667px-tall mobile viewport

#### Scenario: Hero includes Caixa financing trust signal
- **WHEN** a visitor views the hero section
- **THEN** the Caixa Economica financing acceptance is displayed as a visible badge or banner element, not buried in body text (currently: Caixa logo shown in hero column but without prominent badge styling)

#### Scenario: Hero includes extended hours differentiator
- **WHEN** a visitor views the hero or header area
- **THEN** the operating hours "08:00-22:00 | 7 dias" are visible as a distinguishing element, communicating availability beyond standard business hours

### Requirement: Navigation supports all site sections
The site SHALL provide navigation to house models, about, gallery, contact/quote — expanding the current 2-item menu (Sobre Nos, Fotos).

#### Scenario: Mobile navigation
- **WHEN** a visitor opens the site on mobile
- **THEN** the navigation collapses into a hamburger/toggle menu that expands to show all section links: Inicio, Modelos, Sobre, Galeria, Contato

#### Scenario: Desktop navigation
- **WHEN** a visitor opens the site on desktop
- **THEN** all navigation links are visible in a horizontal bar without requiring a menu toggle

#### Scenario: Navigation includes quote CTA
- **WHEN** a visitor views the navigation bar
- **THEN** at least one navigation element links directly to the quote/contact section, visually distinguished as a CTA (button style, contrasting color)

### Requirement: House model catalog displays pre-fabricated house options
The site SHALL display at least 4-6 pre-fabricated house models with name, size, room count, photo area, price indicator, and quote CTA — replacing the current zero-model state despite the business offering "diversos modelos de casas."

#### Scenario: Visitor browses house models
- **WHEN** a visitor scrolls to or navigates to the models section
- **THEN** the visitor sees cards for house models with: model name, size in m2, number of rooms/bathrooms, a designated photo area, price indicator ("A partir de R$ XX.000" or "Sob consulta"), and a "Solicitar Orcamento" CTA

#### Scenario: House model cards on mobile
- **WHEN** a visitor views models on a mobile viewport
- **THEN** model cards stack in a single column with full-width layout, readable specs, and tappable quote CTA per card

#### Scenario: House model cards on desktop
- **WHEN** a visitor views models on a desktop viewport
- **THEN** model cards display in a 2-3 column grid layout

#### Scenario: Custom project option
- **WHEN** a visitor doesn't find a suitable pre-built model
- **THEN** a "Projeto Personalizado" card or section explains that the business offers architect-designed custom houses and links to the quote form

### Requirement: About section highlights company differentiators
The site SHALL present the company story, experience, autoclave treatment quality, and family tradition — organizing the currently scattered about text into a structured section.

#### Scenario: Visitor reads about section
- **WHEN** a visitor scrolls to the about section
- **THEN** they see: years of experience (20+), family tradition since the 80s, autoclave-treated pinus durability explanation, own lumber yard ("madeireira propria"), and architect service availability — organized with headings and icons, not as a single text block

#### Scenario: Durability feature highlight
- **WHEN** a visitor views the about or product section
- **THEN** the autoclave treatment benefit is explained with a clear statement: pinus treated in autoclave for resistance to sun, rain, and humidity — styled as a feature card or callout, not buried in prose

### Requirement: Photo gallery showcases completed projects
The site SHALL display a gallery of completed house projects with multiple images — expanding beyond the current single project photo.

#### Scenario: Visitor views gallery
- **WHEN** a visitor navigates to or scrolls to the gallery section
- **THEN** they see at least 6 project images in a responsive grid with lightbox or modal zoom capability

#### Scenario: Gallery on mobile
- **WHEN** a visitor views the gallery on mobile
- **THEN** images display in a 1-2 column grid with tap-to-expand functionality

### Requirement: Footer displays complete contact information and hours
The site SHALL display all business contact details and hours in the footer, replacing the current minimal footer.

#### Scenario: Visitor checks footer
- **WHEN** a visitor scrolls to the footer
- **THEN** the footer shows: Rua Capitao Pedro Egydio Hoffmann, 107 - Palhoca/SC, WhatsApp (48) 99108-8224 as click-to-call, operating hours (08:00-22:00 todos os dias), and a "ver no mapa" link

#### Scenario: Footer on mobile
- **WHEN** a visitor views the footer on mobile
- **THEN** contact items stack vertically with adequate spacing and all links are tappable

### Requirement: Site uses a warm, wooden-house visual identity
The site SHALL use a color palette and typography that communicates "casas de madeira" — warm wood tones, cabin warmth, natural materials — evoking the finished product rather than raw lumber.

#### Scenario: Visual identity communicates product category
- **WHEN** a visitor opens the site
- **THEN** the color scheme, imagery, and typography create an immediate visual association with wooden houses and natural construction, not a generic corporate or tech identity

#### Scenario: Accessibility contrast requirements
- **WHEN** text is displayed on any background
- **THEN** the color combination meets WCAG AA contrast ratio (4.5:1 for body text, 3:1 for large text)
