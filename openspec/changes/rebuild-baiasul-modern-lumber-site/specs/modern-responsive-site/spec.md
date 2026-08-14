## Purpose

Defines the responsive layout, mobile-first design, navigation, hero section, product showcase, footer, and overall site structure that replaces Baia Sul's 2014 fixed-width (1021px) WebAcappella layout. The current site has no viewport meta tag and is completely broken on mobile devices.

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
- **THEN** a `<meta name="viewport" content="width=device-width, initial-scale=1">` tag is present in the head (currently missing entirely)

### Requirement: Hero section communicates business identity and next action
The site SHALL present Baia Sul's positioning, service region, years in market, and primary CTA in the first meaningful viewport — replacing the current empty content area below the GIF header.

#### Scenario: Visitor lands on home page
- **WHEN** a visitor opens the home page
- **THEN** the visitor can identify: (1) business name "Madeireira Baia Sul", (2) service region "Sao Jose, Florianopolis e Palhoca", (3) a CTA to request a quote or contact via WhatsApp — all without scrolling on a 667px-tall mobile viewport

#### Scenario: Hero includes trust signal
- **WHEN** a visitor views the hero section
- **THEN** the hero includes at least one trust signal (years in market, location reference, or stock diversity) as text, not as an image-only element

### Requirement: Navigation supports all site sections
The site SHALL provide navigation to products, about/company, contact/quote, and location — matching the current 6-section structure but with responsive behavior.

#### Scenario: Mobile navigation
- **WHEN** a visitor opens the site on mobile
- **THEN** the navigation collapses into a hamburger/toggle menu that expands to show all section links

#### Scenario: Desktop navigation
- **WHEN** a visitor opens the site on desktop
- **THEN** all navigation links are visible in a horizontal bar without requiring a menu toggle

#### Scenario: Navigation includes quote CTA
- **WHEN** a visitor views the navigation bar
- **THEN** at least one navigation element links directly to the quote/contact section, visually distinguished as a CTA (button style, contrasting color)

### Requirement: Product catalog displays all 13 wood species
The site SHALL display all 13 wood species currently listed on the products page, each with name, color/appearance description, key applications, and a photo area.

#### Scenario: Visitor browses products
- **WHEN** a visitor scrolls to or navigates to the products section
- **THEN** the visitor sees cards or tiles for all 13 species with: species name as a heading, appearance description, application tags or list, and a designated image area

#### Scenario: Product cards on mobile
- **WHEN** a visitor views products on a mobile viewport
- **THEN** product cards stack in a single column with full-width layout, readable text, and tappable quote CTA per card

#### Scenario: Product cards on desktop
- **WHEN** a visitor views products on a desktop viewport
- **THEN** product cards display in a 2-3 column grid layout

### Requirement: Footer displays complete contact information
The site SHALL display all business contact details in the footer: full address with CEP, all 3 phone numbers, domain email, WhatsApp link, and map link — replacing the current minimal footer.

#### Scenario: Visitor checks footer
- **WHEN** a visitor scrolls to the footer
- **THEN** the footer shows: Rua Francisco Pedro Cunha, 567 - Rocado - Sao Jose - SC - CEP 88108-140, all 3 phone numbers as click-to-call links, domain email as mailto link, WhatsApp link, and a "ver no mapa" link

#### Scenario: Footer on mobile
- **WHEN** a visitor views the footer on mobile
- **THEN** contact items stack vertically with adequate spacing and all links are tappable

### Requirement: Site uses a warm, lumber-appropriate visual identity
The site SHALL use a color palette and typography that communicates "lumber yard" — warm wood tones, earth colors — replacing the current cold navy/blue corporate palette (#01163f, #0d7eca).

#### Scenario: Visual identity communicates product category
- **WHEN** a visitor opens the site
- **THEN** the color scheme, imagery, and typography create an immediate visual association with wood/lumber rather than a generic corporate or tech identity

#### Scenario: Accessibility contrast requirements
- **WHEN** text is displayed on any background
- **THEN** the color combination meets WCAG AA contrast ratio (4.5:1 for body text, 3:1 for large text)
