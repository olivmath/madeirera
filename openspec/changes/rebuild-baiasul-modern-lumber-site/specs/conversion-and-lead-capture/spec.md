## Purpose

Defines the quote request forms, CTAs, WhatsApp integration, click-to-call, and lead capture requirements to replace Baia Sul's current zero-conversion state. The existing site has: zero visible CTAs, zero working forms (the contact page form is WebAcappella-generated and non-functional), and only a floating WhatsApp button with a generic prefilled message. Conversion score is 3.0/25.

## ADDED Requirements

### Requirement: Quote request form captures leads with product context
The site SHALL include at least one structured quote request form with fields that capture the visitor's intent and contact information.

#### Scenario: Visitor requests a quote
- **WHEN** a visitor fills out the quote form
- **THEN** the form captures: assunto (Orcamento/Duvida/Sugestao — matching the current contact form options), nome (required), telefone ou WhatsApp (required), cidade/estado, produto de interesse (optional, with the 13 species as options), and mensagem (currently: form exists on Contato page but is non-functional WebAcappella output)

#### Scenario: Form validation
- **WHEN** a visitor submits the form with missing required fields
- **THEN** the form shows inline validation errors on the specific fields and does not submit

#### Scenario: Form success state
- **WHEN** a visitor successfully submits the form
- **THEN** the form shows a visible success message confirming the submission and expected response time

### Requirement: Primary CTAs are visible in hero and product sections
The site SHALL display prominent call-to-action buttons in the hero section and after the product catalog, replacing the current zero-CTA state.

#### Scenario: Hero CTA
- **WHEN** a visitor views the hero section
- **THEN** at least two CTAs are visible: one for WhatsApp contact and one for the quote form (e.g., "Solicite um Orcamento" and "Fale pelo WhatsApp")

#### Scenario: Product section CTA
- **WHEN** a visitor browses product cards
- **THEN** each product card includes a "Pedir Orcamento" or "Consultar" action that links to the quote form or opens WhatsApp with the product name prefilled

#### Scenario: CTA button sizing
- **WHEN** CTAs are rendered on mobile
- **THEN** buttons have minimum 44px height, adequate padding, and are visually distinguished from surrounding content with contrasting color

### Requirement: WhatsApp integration includes page and product context
The site SHALL provide WhatsApp links that prefill messages with context about which page or product the visitor was viewing, replacing the current generic "Texto aqui" prefill.

#### Scenario: WhatsApp from home page
- **WHEN** a visitor clicks the WhatsApp button from the home page
- **THEN** the prefilled message includes the business context, e.g., "Ola, vim pelo site da Madeireira Baia Sul e gostaria de informacoes sobre..."

#### Scenario: WhatsApp from product card
- **WHEN** a visitor clicks a WhatsApp link from a specific product card (e.g., Jatoba)
- **THEN** the prefilled message includes the product name, e.g., "Ola, vim pelo site e gostaria de um orcamento de Jatoba."

#### Scenario: WhatsApp button visibility
- **WHEN** a visitor scrolls any page
- **THEN** a floating WhatsApp button remains visible in the bottom-right corner (preserving the current working behavior) with the correct number (48) 99122-8781

### Requirement: Phone numbers are click-to-call links
The site SHALL render all phone numbers as clickable `tel:` links so mobile visitors can call with one tap.

#### Scenario: Mobile visitor taps phone number
- **WHEN** a mobile visitor taps any displayed phone number
- **THEN** the device initiates a phone call to that number (currently: phone numbers are displayed as plain text in a span element)

#### Scenario: All three numbers are callable
- **WHEN** the footer or contact section is viewed
- **THEN** all three numbers — (48) 3247-1377, (48) 99122-8781, (48) 98834-0719 — are individually tappable as tel: links

### Requirement: Email addresses are clickable mailto links
The site SHALL render domain email addresses as `mailto:` links.

#### Scenario: Visitor clicks email
- **WHEN** a visitor clicks the email address
- **THEN** it opens the visitor's email client with the To field prefilled with contato@madeireirabaiasul.com.br (currently: email is displayed as cloudflare-obfuscated text)

### Requirement: Contact section consolidates all channels
The site SHALL display all contact channels (WhatsApp, phone, email, address, map) in a single contact section, replacing the current split across separate Contato and Localizacao pages.

#### Scenario: Visitor looks for contact options
- **WHEN** a visitor navigates to the contact section
- **THEN** all channels are visible together: 3 phone numbers (click-to-call), WhatsApp (click-to-chat), email (mailto), full address with CEP, and a map link or embed — without needing to visit a separate page

### Requirement: Form captures product interest from catalog context
The site SHALL allow visitors to reach the quote form from a product card with the product name pre-selected.

#### Scenario: Quote from product card
- **WHEN** a visitor clicks "Pedir Orcamento" on the Angelim Pedra product card
- **THEN** the quote form scrolls into view (or opens) with "Angelim Pedra" pre-selected in the product interest field
