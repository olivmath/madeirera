## Purpose

Defines the quote request form, CTAs, WhatsApp integration, and lead capture requirements to fix Silva's zero-form conversion state. The current site has: zero forms anywhere, WhatsApp as the only conversion channel (scattered across 3 entry points: nav, hero, contact section), and no structured way to capture visitor intent. Conversion score is 11.2/25.

## ADDED Requirements

### Requirement: Quote request form captures leads with product context
The site SHALL include a structured quote request form that captures visitor intent and contact information.

#### Scenario: Visitor requests a quote
- **WHEN** a visitor fills out the quote form
- **THEN** the form captures: nome (required), telefone ou WhatsApp (required), produto de interesse (select from: Kit Casa, Deck/Pergolado, Aberturas, Madeiras em Geral, Eucalipto, Outro), and mensagem (optional) — (currently: zero forms exist on the site)

#### Scenario: Form validation
- **WHEN** a visitor submits the form with missing required fields
- **THEN** the form shows inline validation errors on the specific fields and does not submit

#### Scenario: Form success state
- **WHEN** a visitor successfully submits the form
- **THEN** the form shows a visible success message confirming the submission and expected response time

#### Scenario: Form is accessible from multiple entry points
- **WHEN** a visitor wants to request a quote
- **THEN** the form is reachable from: (1) the main navigation CTA, (2) the hero section CTA, (3) individual product page CTAs, (4) the contact section

### Requirement: Primary CTAs are visible in hero and product sections
The site SHALL display prominent call-to-action buttons in the hero section and on each product page.

#### Scenario: Hero CTA
- **WHEN** a visitor views the hero section
- **THEN** at least two CTAs are visible: one for WhatsApp contact and one for the quote form (e.g., "Solicite um Orcamento" and "Fale pelo WhatsApp")

#### Scenario: Product page CTA
- **WHEN** a visitor views a product page
- **THEN** the page includes a "Pedir Orcamento" button that links to the quote form with the product name pre-selected, and a "WhatsApp" button with the product name prefilled in the message

#### Scenario: CTA button sizing
- **WHEN** CTAs are rendered on mobile
- **THEN** buttons have minimum 44px height, adequate padding, and are visually distinguished with contrasting color

### Requirement: WhatsApp integration is consolidated with contextual messages
The site SHALL provide WhatsApp links with contextual prefilled messages, consolidating the current 3 scattered entry points into a consistent pattern.

#### Scenario: WhatsApp from home page
- **WHEN** a visitor clicks the WhatsApp button from the home page
- **THEN** the prefilled message is: "Ola! Estou entrando em contato atraves do site e gostaria de mais informacoes."

#### Scenario: WhatsApp from product page
- **WHEN** a visitor clicks the WhatsApp button from the Deck/Pergolado product page
- **THEN** the prefilled message includes the product name: "Ola! Estou entrando em contato atraves do site e gostaria de mais informacoes sobre Deck e Pergolado."

#### Scenario: WhatsApp from blog article
- **WHEN** a visitor clicks the WhatsApp CTA from a blog article (e.g., Pinus vs Eucalipto)
- **THEN** the prefilled message references the article: "Ola! Li o artigo sobre Pinus vs Eucalipto e gostaria de saber mais..."

#### Scenario: Floating WhatsApp button
- **WHEN** a visitor scrolls any page
- **THEN** a floating WhatsApp button remains visible in the bottom-right corner with the number (48) 99858-5524

#### Scenario: Single WhatsApp number
- **WHEN** any WhatsApp link is clicked anywhere on the site
- **THEN** it always uses the same number +55 48 98585524 (currently: site uses this number consistently, which should be preserved)

### Requirement: Phone number is click-to-call
The site SHALL render the phone number as a clickable `tel:` link.

#### Scenario: Mobile visitor taps phone number
- **WHEN** a mobile visitor taps the phone number
- **THEN** the device initiates a call to (48) 99858-5524

#### Scenario: Phone number in all contact areas
- **WHEN** the header, footer, or contact section displays the phone number
- **THEN** it is wrapped in a `<a href="tel:+5548998585524">` link

### Requirement: Email address is a clickable mailto link
The site SHALL render the email as a `mailto:` link.

#### Scenario: Visitor clicks email
- **WHEN** a visitor clicks contato@madeireirasilva.ind.br
- **THEN** it opens the visitor's email client with the To field prefilled

### Requirement: Contact section consolidates all channels
The site SHALL display all contact channels in a single contact section with both locations.

#### Scenario: Visitor looks for contact options
- **WHEN** a visitor navigates to the contact section
- **THEN** all channels are visible: phone/WhatsApp (click-to-call/chat), email (mailto), both addresses with map links, business hours (Seg-Qui 07:30-18:00, Sex 07:30-17:00), and social links (Instagram, YouTube)

### Requirement: Form captures product interest from product page context
The site SHALL allow visitors to reach the quote form from a product page with the product pre-selected.

#### Scenario: Quote from product page
- **WHEN** a visitor clicks "Pedir Orcamento" on the Deck/Pergolado page
- **THEN** the quote form opens with "Deck/Pergolado" pre-selected in the product interest field

#### Scenario: Quote from blog article
- **WHEN** a visitor reads a blog article about Pinus and clicks the CTA
- **THEN** the form opens with "Madeiras em Geral" pre-selected or the WhatsApp opens with the article-specific prefill

### Requirement: Partnership inquiry path exists
The site SHALL provide a way for potential partners to make contact, preserving the existing partnership prefill.

#### Scenario: Partner inquiry
- **WHEN** a potential business partner wants to contact Silva
- **THEN** the form includes a "Parceria" option in the subject field, or the WhatsApp prefill "Tenho interesse em ser parceiro da Madeireira Silva" is accessible from the contact page
