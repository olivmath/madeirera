## Purpose

Defines the quote request forms, financing inquiry, CTAs, WhatsApp enhancement, and lead capture requirements to fix Palhoca Casas de Madeira's form-less conversion state. The current site has: zero forms of any kind, complete dependency on WhatsApp links for all lead capture, good WhatsApp placement (header, hero, footer) but with a generic prefilled message, and no mechanism to capture interest in specific house models or financing. Conversion score is 13.8/25 — relatively high only because of the strong WhatsApp presence.

## ADDED Requirements

### Requirement: Quote request form captures leads with house model context
The site SHALL include at least one structured quote request form that captures the visitor's interest type and contact information — currently zero forms exist on the entire site.

#### Scenario: Visitor requests a quote for a house model
- **WHEN** a visitor fills out the quote form
- **THEN** the form captures: tipo de interesse (Casa Pre-Fabricada / Madeira Avulsa / Projeto Personalizado), modelo de interesse (dropdown with house model names from catalog, plus "Outro"), nome (required), telefone ou WhatsApp (required), cidade, and mensagem

#### Scenario: Form pre-selects house model from catalog
- **WHEN** a visitor clicks "Solicitar Orcamento" on a specific house model card
- **THEN** the quote form scrolls into view with that model pre-selected in the "modelo de interesse" field

#### Scenario: Form validation
- **WHEN** a visitor submits the form with missing required fields (nome, telefone)
- **THEN** the form shows inline validation errors on the specific fields and does not submit

#### Scenario: Form success state
- **WHEN** a visitor successfully submits the form
- **THEN** the form shows a visible success message confirming the submission and expected response time (e.g., "Recebemos sua solicitacao! Entraremos em contato em ate 24 horas.")

### Requirement: Financing inquiry is a prominent conversion path
The site SHALL provide a dedicated path for visitors interested in Caixa financing, connecting the trust signal to lead capture — currently the Caixa badge exists but has no associated form or CTA.

#### Scenario: Financing CTA in hero
- **WHEN** a visitor sees the Caixa financing badge in the hero
- **THEN** a nearby CTA (e.g., "Simule seu Financiamento" or "Consulte Financiamento") links to the quote form with "Financiamento Caixa" context pre-filled or highlighted

#### Scenario: Financing section
- **WHEN** a visitor scrolls to a financing information area
- **THEN** they see a brief explanation of how Caixa financing works for pre-fab houses, with a CTA to the quote form

### Requirement: Primary CTAs are visible in hero and model sections
The site SHALL display prominent call-to-action buttons in the hero section and after the house model catalog — improving on the current WhatsApp-only CTA approach.

#### Scenario: Hero dual CTA
- **WHEN** a visitor views the hero section
- **THEN** at least two CTAs are visible: one for the quote form (e.g., "Solicite seu Orcamento") and one for WhatsApp (e.g., "Fale pelo WhatsApp") — the current site has only a WhatsApp button in the hero

#### Scenario: Model card CTA
- **WHEN** a visitor browses house model cards
- **THEN** each model card includes a "Solicitar Orcamento" action that links to the quote form with the model name pre-selected, AND a WhatsApp icon that opens WhatsApp with the model name prefilled

#### Scenario: CTA button sizing
- **WHEN** CTAs are rendered on mobile
- **THEN** buttons have minimum 44px height, adequate padding, and are visually distinguished from surrounding content with contrasting color

### Requirement: WhatsApp integration includes page and model context
The site SHALL enhance the existing WhatsApp links to prefill messages with context about which section or house model the visitor was viewing — the current prefill is generic ("Ola! Gostaria de mais informacoes sobre Palhoca casas de madeira.").

#### Scenario: WhatsApp from home page
- **WHEN** a visitor clicks the WhatsApp button from the home page hero
- **THEN** the prefilled message is: "Ola! Vi o site da Palhoca Casas de Madeira e gostaria de informacoes sobre casas pre-fabricadas."

#### Scenario: WhatsApp from house model card
- **WHEN** a visitor clicks a WhatsApp link from a specific model card (e.g., "Casa Araucaria - 45m2")
- **THEN** the prefilled message includes the model name: "Ola! Gostaria de um orcamento para o modelo Casa Araucaria - 45m2."

#### Scenario: WhatsApp from financing section
- **WHEN** a visitor clicks WhatsApp from the financing section
- **THEN** the prefilled message is: "Ola! Gostaria de informacoes sobre financiamento pela Caixa para casas de madeira."

#### Scenario: WhatsApp floating button visibility
- **WHEN** a visitor scrolls any section
- **THEN** a floating WhatsApp button remains visible in the bottom-right corner with the correct number (48) 99108-8224 (preserving the current good placement pattern)

### Requirement: Phone number is a click-to-call link
The site SHALL render the phone/WhatsApp number as a clickable `tel:` link so mobile visitors can call with one tap.

#### Scenario: Mobile visitor taps phone number
- **WHEN** a mobile visitor taps the displayed phone number
- **THEN** the device initiates a phone call to (48) 99108-8224

### Requirement: Contact section consolidates all channels
The site SHALL display all contact channels (WhatsApp, phone, address, hours, map) in a single contact section with the quote form.

#### Scenario: Visitor looks for contact options
- **WHEN** a visitor navigates to the contact section
- **THEN** all channels are visible together: WhatsApp (click-to-chat), phone (click-to-call), full address, operating hours (08:00-22:00 todos os dias), map link or embed, and the quote form — without needing to visit a separate page

### Requirement: Extended hours are a conversion element
The site SHALL present the 08:00-22:00 7-day schedule as a conversion-supporting element, not just informational text.

#### Scenario: Hours create urgency/convenience
- **WHEN** a visitor sees the operating hours
- **THEN** they are presented with a contextual message like "Estamos abertos agora" or "Atendemos ate as 22h — ligue agora!" near a CTA, leveraging the extended hours as a reason to act immediately
