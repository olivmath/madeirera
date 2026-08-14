## Purpose

Defines the quote request forms, unified WhatsApp strategy, CTAs, and lead capture flows to close Cambirela's conversion gap. The current site has: ZERO forms (100% WhatsApp-dependent), 3 different WhatsApp numbers scattered confusingly, and a "SOLICITE ORCAMENTO" button hidden on mobile. Conversion score is 10.7/25 despite the business having the highest recommendation score (8.0/10) in its tier — the site wastes the trust customers already have.

## ADDED Requirements

### Requirement: Quote request form captures leads with product context
The site SHALL include at least one structured quote request form — replacing the current zero-form state where the only conversion path is WhatsApp.

#### Scenario: Visitor requests a quote
- **WHEN** a visitor fills out the quote form
- **THEN** the form captures: nome (required), telefone ou WhatsApp (required), produto de interesse (optional dropdown with the 17 products), and mensagem (optional)

#### Scenario: Form validation
- **WHEN** a visitor submits the form with missing required fields
- **THEN** the form shows inline validation errors on the specific fields and does not submit

#### Scenario: Form success state
- **WHEN** a visitor successfully submits the form
- **THEN** the form shows a visible success message confirming the submission and expected response time

### Requirement: WhatsApp numbers are unified with clear routing
The site SHALL present 1 primary WhatsApp number in prominent positions (header, floating button, hero CTA), with all 3 named contacts visible only in the footer/contact section — replacing the current confusing 3-number scatter.

#### Scenario: Primary WhatsApp in header
- **WHEN** a visitor views the header bar
- **THEN** only 1 WhatsApp number is displayed (primary: (48) 99205-8040) rather than the current 2+ numbers

#### Scenario: Floating WhatsApp button
- **WHEN** a visitor scrolls any part of the page
- **THEN** a floating WhatsApp button remains visible in the bottom-right corner using the primary number with a contextual prefilled message

#### Scenario: Named contacts in footer
- **WHEN** a visitor views the contact section or footer
- **THEN** all 3 WhatsApp contacts are visible with names (Denise, Amanda, Adriana) for direct routing, each with their own click-to-chat link

### Requirement: CTAs are visible on all viewports including mobile
The site SHALL display prominent call-to-action buttons in the hero section and after the product catalog on all viewport sizes — fixing the current state where the "SOLICITE ORCAMENTO" button is hidden on mobile (elementor-hidden-mobile class).

#### Scenario: Hero CTA on mobile
- **WHEN** a visitor views the hero section on a mobile device
- **THEN** at least two CTAs are visible: one for the quote form and one for WhatsApp contact — NOT hidden by responsive rules

#### Scenario: Product section CTA
- **WHEN** a visitor browses product cards
- **THEN** each product card includes a "Pedir Orcamento" action that either links to the quote form with the product pre-selected or opens WhatsApp with the product name prefilled

#### Scenario: CTA button sizing
- **WHEN** CTAs are rendered on mobile
- **THEN** buttons have minimum 44px height, full-width layout on mobile, and are visually distinguished with contrasting color

### Requirement: WhatsApp integration includes product context
The site SHALL provide WhatsApp links that prefill messages with context about which product the visitor was viewing — replacing the current generic "Ola, achei sua empresa no Google e gostaria de um orcamento" used everywhere.

#### Scenario: WhatsApp from home page
- **WHEN** a visitor clicks the WhatsApp button from the home page
- **THEN** the prefilled message includes business context, e.g., "Ola, vim pelo site da Madeireira Cambirela e gostaria de informacoes sobre..."

#### Scenario: WhatsApp from product card
- **WHEN** a visitor clicks a WhatsApp link from a specific product card (e.g., Deck de Pinus)
- **THEN** the prefilled message includes the product name, e.g., "Ola, vim pelo site e gostaria de um orcamento de Deck de Pinus Tratado."

### Requirement: Phone numbers are click-to-call links
The site SHALL render all phone numbers as clickable `tel:` links — the current site partially does this (footer phone is `tel:` but some instances are plain text).

#### Scenario: Mobile visitor taps phone number
- **WHEN** a mobile visitor taps any displayed phone number
- **THEN** the device initiates a phone call to that number

#### Scenario: All numbers are callable
- **WHEN** the footer or contact section is viewed
- **THEN** the landline (48) 3242-3534 and all WhatsApp numbers are individually tappable as tel: or wa.me links

### Requirement: Form captures product interest from catalog context
The site SHALL allow visitors to reach the quote form from a product card with the product name pre-selected in the dropdown.

#### Scenario: Quote from product card
- **WHEN** a visitor clicks "Pedir Orcamento" on the Deck de Pinus Tratado product card
- **THEN** the quote form scrolls into view with "Deck de Pinus Tratado" pre-selected in the product interest dropdown

### Requirement: Contact section consolidates all channels
The site SHALL display all contact channels in a single visible section — phone, WhatsApp (3 named contacts), email, address, map, and Instagram.

#### Scenario: Visitor looks for contact options
- **WHEN** a visitor navigates to the contact section
- **THEN** all channels are visible together: landline (click-to-call), 3 named WhatsApp contacts (click-to-chat), email (mailto), address with map embed, and Instagram link (correct URL)
