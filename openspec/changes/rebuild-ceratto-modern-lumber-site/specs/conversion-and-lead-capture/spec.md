## Purpose

Defines the quote request form, enhanced CTAs, WhatsApp contextual messages, and lead capture requirements to fix Ceratto's zero-form baseline. The site currently has zero forms anywhere — the only conversion path is WhatsApp buttons ("Enviar WhatsApp") scattered across the page. Conversion score is 11.6/25, penalized primarily by the complete absence of forms.

## ADDED Requirements

### Requirement: Quote request form captures leads with product context
The site SHALL include at least one structured quote request form that captures visitor intent and contact information.

#### Scenario: Visitor requests a quote
- **WHEN** a visitor fills out the quote form
- **THEN** the form captures: nome (required), telefone ou WhatsApp (required), tipo de madeira (dropdown with options: Itauba, Cambara, Garapeira, Cedro, Tatajuba, Angelim Pedra, Roxinho, Longarina, Kit Tabuas, Tabua de Churrasco, Petisqueira, Outro), and mensagem (optional) — currently: zero forms exist on the entire site

#### Scenario: Form validation
- **WHEN** a visitor submits the form with missing required fields
- **THEN** the form shows inline validation errors on nome and telefone fields

#### Scenario: Form success state
- **WHEN** a visitor successfully submits the form
- **THEN** the form shows a success message: "Orcamento enviado! Retornaremos em ate 24 horas uteis."

### Requirement: Primary CTAs are visible in hero and product sections
The site SHALL display prominent call-to-action buttons for both form-based and WhatsApp-based contact.

#### Scenario: Hero CTA
- **WHEN** a visitor views the hero section
- **THEN** at least two CTAs are visible: "Solicite um Orcamento" (links to form) and "Enviar WhatsApp" (existing button — keep as-is) — currently: only WhatsApp CTA exists in the hero

#### Scenario: Product section CTA
- **WHEN** a visitor views a wood species card
- **THEN** each card includes a "Pedir Orcamento" or "Consultar" action that links to the form with the species pre-selected in the dropdown, OR opens WhatsApp with the species name prefilled

#### Scenario: Priced product CTA
- **WHEN** a visitor views a priced product (Kit Tabuas R$450, Tabua Churrasco R$200)
- **THEN** a "Comprar via WhatsApp" or "Reservar" button opens WhatsApp with the product name and price prefilled

### Requirement: WhatsApp integration includes product context
The site SHALL provide WhatsApp links that prefill messages with the specific product the visitor was viewing.

#### Scenario: WhatsApp from home page
- **WHEN** a visitor clicks the WhatsApp button from the home page
- **THEN** the prefilled message is: "Ola, vim pelo site da Ceratto Madeiras e gostaria de informacoes sobre madeiras." (replacing the current generic/empty prefill)

#### Scenario: WhatsApp from product card
- **WHEN** a visitor clicks a WhatsApp link from the Itauba card
- **THEN** the prefilled message is: "Ola, vim pelo site da Ceratto Madeiras e gostaria de um orcamento de Itauba."

#### Scenario: WhatsApp from priced product
- **WHEN** a visitor clicks a WhatsApp link from the Kit Tabuas (R$450)
- **THEN** the prefilled message is: "Ola, vim pelo site e gostaria de comprar o Kit Tabuas de Cozinha (R$450). Como faco?"

#### Scenario: WhatsApp button visibility
- **WHEN** a visitor scrolls any page
- **THEN** the floating WhatsApp button (JoinChat plugin) remains visible in the bottom-right corner with number (48) 99961-1658 (existing behavior — preserve it)

### Requirement: Phone number is click-to-call
The site SHALL render the phone number as a clickable `tel:` link.

#### Scenario: Mobile visitor taps phone number
- **WHEN** a mobile visitor taps (48) 3285-3293
- **THEN** the device initiates a phone call (the existing site already has `<a href="tel:554832853293">` — verify this works correctly and is present in all phone displays)

### Requirement: Email address is a clickable mailto link
The site SHALL render the email as a `mailto:` link.

#### Scenario: Visitor clicks email
- **WHEN** a visitor clicks cerattomadeiras@gmail.com
- **THEN** it opens the email client with To field prefilled (currently: email appears as plain text without mailto link)

### Requirement: Form captures product interest from catalog context
The site SHALL allow visitors to reach the quote form from a product card with the product pre-selected.

#### Scenario: Quote from wood species card
- **WHEN** a visitor clicks "Pedir Orcamento" on the Angelim Pedra card
- **THEN** the quote form scrolls into view with "Angelim Pedra" pre-selected in the tipo de madeira dropdown

#### Scenario: Quote from priced product
- **WHEN** a visitor clicks "Pedir Orcamento" on the Kit Tabuas de Cozinha
- **THEN** the quote form scrolls into view with "Kit Tabuas" pre-selected in the dropdown

### Requirement: Contact section consolidates all channels
The site SHALL display all contact channels together in the "Fale Conosco" section.

#### Scenario: Visitor looks for contact options
- **WHEN** a visitor navigates to the contact/Fale Conosco section
- **THEN** all channels are visible: phone (click-to-call), WhatsApp (click-to-chat), email (mailto), quote form, address, business hours, Google Maps embed, and service area — the existing section already shows most of these but lacks the form
