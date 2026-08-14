## Purpose

Defines the improved responsive layout, product showcase with individual cards, navigation with quote CTA, and overall site structure that replaces Cambirela's current flat product list and disjointed conversion flow. The current site has a working responsive layout (Elementor + OceanWP) but presents 35+ products as a single `<ul>` with no photos, no per-product CTAs, and no visual hierarchy. UI score is 9.3/15 and UX score is 10.8/20.

## ADDED Requirements

### Requirement: Product catalog uses individual cards instead of flat list
The site SHALL display each product as a distinct card with photo, name, description, applications, and a quote CTA — replacing the current single `<ul>` list of 35+ bold items.

#### Scenario: Visitor browses products
- **WHEN** a visitor scrolls to or navigates to the products section
- **THEN** the visitor sees cards for all 17 unique products with: product name as heading, short description, a designated image area, and a "Solicite Orcamento" CTA

#### Scenario: Product cards on mobile
- **WHEN** a visitor views products on a mobile viewport
- **THEN** product cards stack in a single column with full-width layout, readable text, and tappable quote CTA per card (minimum 44x44px touch targets)

#### Scenario: Product cards on desktop
- **WHEN** a visitor views products on a desktop viewport
- **THEN** product cards display in a 3-4 column grid layout with consistent heights

### Requirement: Hero section includes business location and primary CTA
The site SHALL present Cambirela's positioning, city (Palhoca), and primary CTA in the first meaningful viewport — enhancing the current hero which has generic text without location context.

#### Scenario: Visitor lands on home page
- **WHEN** a visitor opens the home page
- **THEN** the visitor can identify: (1) business name "Madeireira Cambirela", (2) city "Palhoca" or "Grande Florianopolis", (3) a CTA to request a quote — all without scrolling on a 667px-tall mobile viewport

#### Scenario: Hero includes trust signal
- **WHEN** a visitor views the hero section
- **THEN** the hero includes at least one trust signal ("20+ anos de experiencia", customer count, or product diversity) as text, not as an image-only element

### Requirement: Navigation includes visible quote CTA on all viewports
The site SHALL display a quote/contact CTA in the navigation bar on both desktop and mobile — the current "SOLICITE ORCAMENTO" button is hidden on mobile.

#### Scenario: Mobile navigation CTA
- **WHEN** a visitor opens the site on mobile
- **THEN** a quote CTA is visible without opening the hamburger menu (e.g., a WhatsApp icon or "Orcamento" button in the header bar)

#### Scenario: Desktop navigation CTA
- **WHEN** a visitor opens the site on desktop
- **THEN** the "SOLICITE ORCAMENTO" button is visible in the navigation bar, visually distinguished as a CTA

### Requirement: Gallery section has descriptive image labels
The site SHALL enhance the existing 25-image gallery with descriptive alt text and optional category labels, replacing the current gallery where all images have empty alt attributes.

#### Scenario: Gallery images
- **WHEN** a visitor browses the gallery
- **THEN** each image has a descriptive alt text (e.g., "Deck de pinus tratado instalado — Madeireira Cambirela") and optionally a visible caption

### Requirement: Footer consolidates contact information with correct links
The site SHALL display all contact channels in the footer with working links, fixing the currently broken Instagram URL.

#### Scenario: Footer links
- **WHEN** a visitor views the footer
- **THEN** the footer shows: phone (click-to-call), 3 WhatsApp contacts with names (click-to-chat), email (mailto), Instagram (correct URL: `https://instagram.com/madeireiracambirela`), and social media links with valid URLs

#### Scenario: Footer on mobile
- **WHEN** a visitor views the footer on mobile
- **THEN** contact items stack vertically with adequate spacing and all links are tappable
