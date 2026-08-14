## Purpose

Defines the quote request forms, CTAs, WhatsApp integration, click-to-call, and lead capture requirements for ZCF Madeireira's standalone site. The current directory listing has: zero forms anywhere, a single WhatsApp button per listing card with a generic prefilled message, and a phone link. Conversion score is 12.8/25 — the WhatsApp buttons work well but there are no forms, no contextual CTAs, and no product-specific conversion paths.

## ADDED Requirements

### Requirement: Quote request form captures leads with product context
The site SHALL include at least one structured quote request form with fields that capture the visitor's intent and contact information.

#### Scenario: Visitor requests a quote
- **WHEN** a visitor fills out the quote form
- **THEN** the form captures: nome (required), telefone ou WhatsApp (required), cidade/bairro, produto de interesse (optional dropdown with treated wood categories: Decks, Pergolados, Cercas, Casas de Madeira, Estruturas Rurais, Estruturas Urbanas, Outro), and mensagem

#### Scenario: Form validation
- **WHEN** a visitor submits the form with missing required fields
- **THEN** the form shows inline validation errors on the specific fields and does not submit

#### Scenario: Form success state
- **WHEN** a visitor successfully submits the form
- **THEN** the form shows a visible success message confirming the submission and expected response time

### Requirement: Primary CTAs are visible in hero and product sections
The site SHALL display prominent call-to-action buttons in the hero section and after the product catalog.

#### Scenario: Hero CTA
- **WHEN** a visitor views the hero section
- **THEN** at least two CTAs are visible: one for WhatsApp contact and one for the quote form (e.g., "Solicite um Orcamento" and "Fale pelo WhatsApp")

#### Scenario: Product section CTA
- **WHEN** a visitor browses product cards
- **THEN** each product card includes a "Pedir Orcamento" or "Consultar" action that links to the quote form or opens WhatsApp with the product category prefilled

#### Scenario: CTA button sizing
- **WHEN** CTAs are rendered on mobile
- **THEN** buttons have minimum 44px height, adequate padding, and are visually distinguished from surrounding content with contrasting color

### Requirement: WhatsApp integration includes product context
The site SHALL provide WhatsApp links that prefill messages with context about which page or product the visitor was viewing, improving upon the directory's generic "achei sua empresa no Google" message.

#### Scenario: WhatsApp from home page
- **WHEN** a visitor clicks the WhatsApp button from the home page
- **THEN** the prefilled message includes: "Ola, vim pelo site da ZCF Madeireira e gostaria de informacoes sobre madeira tratada."

#### Scenario: WhatsApp from product card
- **WHEN** a visitor clicks a WhatsApp link from a specific product card (e.g., Decks)
- **THEN** the prefilled message includes the product category: "Ola, vim pelo site da ZCF Madeireira e gostaria de um orcamento de Deck de Madeira Tratada."

#### Scenario: WhatsApp button visibility
- **WHEN** a visitor scrolls any page
- **THEN** a floating WhatsApp button remains visible in the bottom-right corner with the correct number (48) 99604-1469

#### Scenario: WhatsApp number is ZCF's own
- **WHEN** the WhatsApp link is inspected
- **THEN** it uses ZCF's WhatsApp number 5548996041469, NOT the directory's number 5548999919242

### Requirement: Phone number is click-to-call
The site SHALL render the phone number as a clickable `tel:` link so mobile visitors can call with one tap.

#### Scenario: Mobile visitor taps phone number
- **WHEN** a mobile visitor taps the displayed phone number
- **THEN** the device initiates a phone call to (48) 3058-5898

#### Scenario: Phone number in footer and contact section
- **WHEN** the footer or contact section is viewed
- **THEN** the phone number (48) 3058-5898 is tappable as a tel: link

### Requirement: Instagram link is prominently displayed
The site SHALL link to ZCF's Instagram (@zcfmadeireira) as a social proof and portfolio channel.

#### Scenario: Instagram in footer
- **WHEN** a visitor views the footer
- **THEN** an Instagram icon/link is visible pointing to instagram.com/zcfmadeireira

#### Scenario: Instagram in contact section
- **WHEN** a visitor views the contact section
- **THEN** Instagram is listed alongside WhatsApp and phone as a contact/follow channel

### Requirement: Contact section consolidates all channels
The site SHALL display all contact channels (WhatsApp, phone, Instagram, address, map) in a single contact section.

#### Scenario: Visitor looks for contact options
- **WHEN** a visitor navigates to the contact section
- **THEN** all channels are visible together: phone (click-to-call), WhatsApp (click-to-chat with prefilled message), Instagram (external link), full address with CEP, and a map link or embed — all in one section without separate pages

### Requirement: Form captures product interest from catalog context
The site SHALL allow visitors to reach the quote form from a product card with the product category pre-selected.

#### Scenario: Quote from product card
- **WHEN** a visitor clicks "Pedir Orcamento" on the Decks product card
- **THEN** the quote form scrolls into view (or opens) with "Decks" pre-selected in the product interest dropdown
