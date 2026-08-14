## Purpose

Defines the responsive layout, mobile-first design, navigation, hero section, product showcase, testimonials, footer, and overall site structure that replaces Fontana's outdated WordPress 4.3.34 site with the tm-wood-worker theme. The current site has a functional desktop layout but relies on a 2015 WordPress installation with discontinued plugins (Visual Composer 4.6.2, Revolution Slider 5.0.4.1). UI score is 10.0/15, UX is 12.0/20.

## ADDED Requirements

### Requirement: Site uses mobile-first responsive layout
The site SHALL render correctly on all viewport widths from 320px to 1920px+ without horizontal scrolling, text overflow, or layout breakage.

#### Scenario: Mobile visitor opens the site
- **WHEN** a visitor opens the site on a 375px-wide mobile screen
- **THEN** the layout adapts to the viewport width, text is readable without zooming, and all interactive elements are tappable (minimum 44x44px touch targets)

#### Scenario: Desktop visitor opens the site
- **WHEN** a visitor opens the site on a 1440px desktop screen
- **THEN** the layout uses the available width with a max-width container (1200px), product cards display in a multi-column grid, and navigation is fully visible

#### Scenario: Viewport meta tag is present
- **WHEN** the HTML source is inspected
- **THEN** a `<meta name="viewport" content="width=device-width, initial-scale=1">` tag is present in the head

### Requirement: Hero section communicates business identity and next action
The site SHALL present Fontana's positioning, tagline, years in market, and primary CTAs in the first meaningful viewport — replacing the current Revolution Slider carousel.

#### Scenario: Visitor lands on home page
- **WHEN** a visitor opens the home page
- **THEN** the visitor can identify: (1) business name "Madeireira Fontana", (2) tagline "Qualidade, variedade e estoque", (3) trust signal "Mais de 40 anos em Sao Jose, SC", (4) dual CTAs — WhatsApp and quote form — all without scrolling on a 667px-tall mobile viewport

#### Scenario: Hero replaces heavy slider
- **WHEN** the site loads
- **THEN** the hero section is a static or CSS-animated section, not a JavaScript slider plugin (Revolution Slider 5.0 is 300KB+ of JS and causes layout shift on load)

#### Scenario: Hero includes product highlight
- **WHEN** a visitor views the hero section
- **THEN** at least one featured product is referenced (e.g., "Pinus Autoclave — pecas de ate 6m em estoque") with a link to the products section

### Requirement: Navigation supports all site sections
The site SHALL provide navigation to Home, A Fontana, Produtos, Galeria, Contato — matching the current 5-page structure with responsive behavior.

#### Scenario: Mobile navigation
- **WHEN** a visitor opens the site on mobile
- **THEN** the navigation collapses into a hamburger/toggle menu that expands to show all section links

#### Scenario: Desktop navigation
- **WHEN** a visitor opens the site on desktop
- **THEN** all navigation links are visible in a horizontal bar without requiring a menu toggle

#### Scenario: Navigation includes contact CTA
- **WHEN** a visitor views the navigation bar
- **THEN** at least one navigation element links directly to the contact/quote section, visually distinguished as a CTA (button style, contrasting color using #C69453 gold or #bf0310 red)

#### Scenario: Header displays contact info
- **WHEN** a visitor views the header area on desktop
- **THEN** the phone number (48) 3258-1500 and email are visible above or alongside the navigation (matching current top bar behavior)

### Requirement: Product catalog displays all 17 wood species
The site SHALL display all 17 wood species currently documented, each with name, characteristics, applications, and a photo.

#### Scenario: Visitor browses products
- **WHEN** a visitor scrolls to or navigates to the products section
- **THEN** the visitor sees cards for all 17 species with: species name as a heading, key characteristics (density, texture, surface), applications list, designated image, and a "Pedir Orcamento" CTA

#### Scenario: Pinus Autoclave featured prominently
- **WHEN** a visitor views the products section
- **THEN** Pinus Autoclave appears first or in a featured position with its unique selling points: anti-cupim treatment, 12-year guarantee, pieces up to 6m

#### Scenario: Product cards on mobile
- **WHEN** a visitor views products on a mobile viewport
- **THEN** product cards stack in a single column with full-width layout, readable text, and tappable quote CTA per card

#### Scenario: Product cards on desktop
- **WHEN** a visitor views products on a desktop viewport
- **THEN** product cards display in a 2-3 column grid layout

### Requirement: Testimonials section with Schema.org markup
The site SHALL display the existing customer testimonials with Schema.org/Review structured data, preserving the markup already present on the current site.

#### Scenario: Visitor reads testimonials
- **WHEN** a visitor scrolls to the testimonials section
- **THEN** they see at least the 2 existing testimonials with author name, company/role, and city

#### Scenario: Schema.org Review markup
- **WHEN** a search engine crawls the testimonials
- **THEN** each testimonial includes valid Schema.org/Review markup with reviewBody and author fields

### Requirement: Footer displays complete contact and business information
The site SHALL display all business details in the footer: address, phone, email, WhatsApp, payment options, and a brief about text.

#### Scenario: Visitor checks footer
- **WHEN** a visitor scrolls to the footer
- **THEN** the footer shows: Rua Italia n200, Serraria, Sao Jose, SC 88115-360, phone (48) 3258-1500 as click-to-call, email as mailto, WhatsApp link, and accepted payment methods

#### Scenario: Footer on mobile
- **WHEN** a visitor views the footer on mobile
- **THEN** footer sections stack vertically with adequate spacing and all links are tappable

### Requirement: Site preserves Fontana's warm visual identity
The site SHALL use Fontana's existing brand colors and typography: #bf0310 (red accent), #C69453 (gold/warm wood), #594431 (dark brown), Montserrat font family, with white/cream backgrounds for readability.

#### Scenario: Visual identity is consistent with existing brand
- **WHEN** a visitor opens the new site
- **THEN** the color scheme and typography are recognizable as "Fontana Madeireira" — not a generic template swap

#### Scenario: Accessibility contrast requirements
- **WHEN** text is displayed on any background
- **THEN** the color combination meets WCAG AA contrast ratio (4.5:1 for body text, 3:1 for large text)

### Requirement: Gallery section showcases projects and products
The site SHALL include a gallery section with photos organized by category (Madeiras, Moveis), using images from the existing 65+ photo library.

#### Scenario: Visitor browses gallery
- **WHEN** a visitor navigates to the gallery section
- **THEN** they see a filterable or categorized photo grid with thumbnail previews and lightbox/modal for full-size viewing

#### Scenario: Gallery images have alt text
- **WHEN** gallery images are rendered
- **THEN** each image has descriptive alt text including the wood species or furniture type shown
