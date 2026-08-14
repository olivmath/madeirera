## Purpose

Defines the server-rendered site structure, navigation, hero section, product showcase, and footer that replaces Silva's Lovable-generated React SPA. The current site renders all content via an 870KB JavaScript bundle — crawlers that do not execute JS see only an empty `<div id="root"></div>`. The visual design is adequate (UI: 10.4/15) but the delivery mechanism blocks SEO indexing and increases load time.

## ADDED Requirements

### Requirement: All content is present in the initial HTML response
The site SHALL deliver all visible text, headings, images, and structured data in the HTML document without requiring JavaScript execution.

#### Scenario: Crawler fetches the page
- **WHEN** a crawler (Googlebot, social media scraper) fetches any page with JavaScript disabled
- **THEN** all text content, headings, images, navigation, and structured data are present in the HTML source (currently: only `<div id="root"></div>` is visible without JS)

#### Scenario: Page load without JavaScript
- **WHEN** a visitor with JavaScript disabled opens the site
- **THEN** all content is readable, navigation links work, images display, and contact information is visible

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

### Requirement: Hero section preserves brand identity and drives action
The site SHALL present Silva's tagline, trust signals, and primary CTAs in the first viewport — preserving the existing hero slider imagery.

#### Scenario: Visitor lands on home page
- **WHEN** a visitor opens the home page
- **THEN** the visitor sees: (1) "Transformando lares com madeira sustentavel" tagline, (2) trust signals — "57 anos", "3a geracao", "100% reflorestamento", (3) primary CTAs for WhatsApp and quote form — all without scrolling on a 667px mobile viewport

#### Scenario: Hero image slider works without React
- **WHEN** a visitor views the hero section
- **THEN** the 4 hero images cycle with CSS transitions or vanilla JS, not requiring React hydration

### Requirement: Navigation matches existing sections with responsive behavior
The site SHALL provide navigation to: Inicio, Produtos, Sobre Nos, Blog, Contato — matching the current structure.

#### Scenario: Mobile navigation
- **WHEN** a visitor opens the site on mobile
- **THEN** the navigation collapses into a hamburger/toggle menu that expands to show all section links

#### Scenario: Desktop navigation
- **WHEN** a visitor opens the site on desktop
- **THEN** all navigation links are visible in a horizontal bar

#### Scenario: Navigation includes quote CTA
- **WHEN** a visitor views the navigation bar
- **THEN** at least one navigation element links to the quote/contact section, visually distinguished as a CTA button

### Requirement: Product catalog has individual pages per category
The site SHALL create separate pages for each product category: Kit Casa, Deck/Pergolado, Aberturas, Madeiras em Geral, Eucalipto.

#### Scenario: Visitor browses products
- **WHEN** a visitor navigates to a specific product page (e.g., /produtos/deck-pergolado)
- **THEN** the page displays: product name as H1, all associated images with alt text, description, specifications, and a quote CTA specific to that product

#### Scenario: Product listing page
- **WHEN** a visitor navigates to /produtos
- **THEN** the page displays cards for all 5 product categories with: category name, representative image, brief description, and link to the individual page

#### Scenario: Product pages on mobile
- **WHEN** a visitor views a product page on mobile
- **THEN** images stack vertically, text is readable, and the quote CTA is prominent and tappable

### Requirement: Deep Fitting technology section is preserved
The site SHALL include a dedicated section showcasing the exclusive "Encaixe Deep Fitting" technology.

#### Scenario: Deep Fitting showcase
- **WHEN** a visitor views the about or products section
- **THEN** the Deep Fitting section is visible with: the technology name, explanation of how it eliminates gaps caused by climate variation, and the "Exclusivo da Madeireira Silva" differentiator

### Requirement: Footer displays complete contact information for both locations
The site SHALL display all business contact details in the footer: both addresses, phone/WhatsApp, email, CNPJ, business hours, social links, and map links.

#### Scenario: Visitor checks footer
- **WHEN** a visitor scrolls to the footer
- **THEN** the footer shows: both addresses (Alto Aririu + Jardim Eldorado), phone (48) 99858-5524 as click-to-call, contato@madeireirasilva.ind.br as mailto, CNPJ 06.308.663/0001-54, business hours (Seg-Qui 07:30-18:00, Sex 07:30-17:00), Instagram link, YouTube link, and Google Maps links for both locations

#### Scenario: Footer on mobile
- **WHEN** a visitor views the footer on mobile
- **THEN** contact items stack vertically with adequate spacing and all links are tappable

### Requirement: Testimonials section displays Google reviews
The site SHALL display the existing Google reviews with ratings, names, and review text.

#### Scenario: Visitor views testimonials
- **WHEN** a visitor scrolls to the testimonials section
- **THEN** at least 5 reviews are visible with: reviewer name, star rating (all 5/5), review text, and the aggregate "4.9/5 com 70 avaliacoes" badge

### Requirement: Site uses the existing warm visual identity
The site SHALL preserve the current nature-inspired palette: forest greens, warm wood tones, cream backgrounds.

#### Scenario: Visual continuity
- **WHEN** a visitor familiar with the current site opens the new version
- **THEN** the color scheme, typography, and overall aesthetic feel consistent with the existing brand

#### Scenario: Accessibility contrast
- **WHEN** text is displayed on any background
- **THEN** the color combination meets WCAG AA contrast ratio (4.5:1 for body text, 3:1 for large text)
