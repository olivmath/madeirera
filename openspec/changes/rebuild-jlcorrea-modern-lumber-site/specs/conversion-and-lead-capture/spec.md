## Purpose

Defines the quote request form, CTAs, WhatsApp integration with context, click-to-call, and lead capture requirements to fix JL Correa's 10.0/25 Conversion score. The current site has: ZERO forms (captacao 100% WhatsApp), 3 WhatsApp instances in hero/footer/contact, but no structured lead capture mechanism. While WhatsApp presence is strong (8 references with clear CTAs), the complete absence of forms means visitors who prefer form-based contact have no option.

## ADDED Requirements

### Requirement: Quote request form captures leads with product context
The site SHALL include at least one structured quote request form that captures visitor intent and contact information.

#### Scenario: Visitor requests a quote
- **WHEN** a visitor fills out the quote form
- **THEN** the form captures: nome (required), telefone ou WhatsApp (required), produto de interesse (dropdown: Madeiras Certificadas, Aberturas, Pinus Tratado, Outro), quantidade ou dimensoes (optional text), uso pretendido (optional: Construcao, Reforma, Projeto Personalizado, Outro), and mensagem (optional) — currently: ZERO forms on the entire site

#### Scenario: Form validation
- **WHEN** a visitor submits the form with missing required fields
- **THEN** the form shows inline validation errors on nome and telefone fields and does not submit

#### Scenario: Form success state
- **WHEN** a visitor successfully submits the form
- **THEN** the form shows a visible success message: "Orcamento solicitado! Retornaremos em ate 24 horas uteis."

### Requirement: Primary CTAs are visible in hero and product sections
The site SHALL display prominent call-to-action buttons in the hero section and after the product showcase.

#### Scenario: Hero CTA
- **WHEN** a visitor views the hero section
- **THEN** at least two CTAs are visible: "Solicite um Orcamento" (scrolls to form) and "Fale pelo WhatsApp" (opens chat) — preserving the current dual-CTA pattern but adding the form destination

#### Scenario: Product section CTA
- **WHEN** a visitor browses product category cards
- **THEN** each category card includes a "Pedir Orcamento" action that links to the quote form with the category pre-selected or opens WhatsApp with the category name prefilled

#### Scenario: CTA button sizing
- **WHEN** CTAs are rendered on mobile
- **THEN** buttons have minimum 44px height, adequate padding, and are visually distinguished from surrounding content

### Requirement: WhatsApp integration includes product context
The site SHALL enhance the existing WhatsApp links with contextual prefilled messages, building on the current 3 instances (hero, footer, contact).

#### Scenario: WhatsApp from home page
- **WHEN** a visitor clicks the WhatsApp button from the hero section
- **THEN** the prefilled message includes: "Ola, vim pelo site da JL Correa Madeiras e gostaria de informacoes sobre madeiras certificadas."

#### Scenario: WhatsApp from product card
- **WHEN** a visitor clicks a WhatsApp link from a product category (e.g., Aberturas)
- **THEN** the prefilled message includes the category: "Ola, vim pelo site e gostaria de um orcamento de Aberturas sob medida."

#### Scenario: WhatsApp button visibility
- **WHEN** a visitor scrolls any section of the page
- **THEN** a floating WhatsApp button remains visible in the bottom-right corner with the correct number (48) 9 9697-3814

#### Scenario: WhatsApp number format
- **WHEN** a WhatsApp link is clicked
- **THEN** the link uses the correct format: `https://wa.me/5548996973814?text=...` with country code and no spaces

### Requirement: Phone number is click-to-call
The site SHALL render the phone number as a clickable `tel:` link so mobile visitors can call with one tap.

#### Scenario: Mobile visitor taps phone number
- **WHEN** a mobile visitor taps the phone number
- **THEN** the device initiates a phone call to (48) 3242-0186

#### Scenario: Phone number in header and footer
- **WHEN** the header or footer is viewed
- **THEN** the phone number (48) 3242-0186 is rendered as a `tel:+554832420186` link

### Requirement: Contact section consolidates all channels
The site SHALL display all contact channels in a single section: form, WhatsApp, phone, address, business hours, and map.

#### Scenario: Visitor looks for contact options
- **WHEN** a visitor navigates to the contact section
- **THEN** all channels are visible together: quote form, WhatsApp click-to-chat, phone click-to-call, full address with CEP 88131-340, business hours (7:15-12:00, 13:00-18:00, Mon-Fri), and Google Maps embed — replacing the fragmented contact information currently spread across decorative H2 headings

### Requirement: Form captures product interest from catalog context
The site SHALL allow visitors to reach the quote form from a product card with the category pre-selected.

#### Scenario: Quote from product card
- **WHEN** a visitor clicks "Pedir Orcamento" on the Madeiras Certificadas card
- **THEN** the quote form scrolls into view with "Madeiras Certificadas" pre-selected in the product interest dropdown

### Requirement: CTA after gallery section
The site SHALL include a conversion CTA after the gallery section, capitalizing on the visual impact of product photos.

#### Scenario: Post-gallery CTA
- **WHEN** a visitor finishes browsing the gallery
- **THEN** a CTA section appears below the gallery with text like "Pronto para transformar sua obra?" and buttons for quote form and WhatsApp — mirroring the existing CTA text from the current site

### Requirement: Business hours are prominently displayed
The site SHALL display business hours in the contact section and footer, formatted clearly.

#### Scenario: Visitor checks hours
- **WHEN** a visitor looks for business hours
- **THEN** they find: "Segunda a Sexta: 7:15 - 12:00 | 13:00 - 18:00" and "Nao abrimos aos sabados" — rendered as text in the contact section and footer, not as H2 headings (currently "Segunda a Sexta" is an H2)
