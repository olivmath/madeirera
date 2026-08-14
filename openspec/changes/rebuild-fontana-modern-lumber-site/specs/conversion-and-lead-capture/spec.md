## Purpose

Defines the quote request forms, CTAs, WhatsApp integration, click-to-call, and lead capture requirements to fix Fontana's conversion deficiencies. The current site has: zero WhatsApp links anywhere (the most critical channel in the lumber industry is completely absent), a contact form only in the footer (easy to miss), no prominent CTAs, and no per-product quote mechanism. The contact page exists but shows no visible form — only the footer form across all pages. Conversion score is 11.0/25.

## ADDED Requirements

### Requirement: WhatsApp integration on every page
The site SHALL include WhatsApp click-to-chat links as the primary contact channel, which is currently 100% absent from the site.

#### Scenario: Sticky WhatsApp button
- **WHEN** a visitor scrolls any page
- **THEN** a floating WhatsApp button remains visible in the bottom-right corner with the business WhatsApp number (to be confirmed — currently only landline (48) 3258-1500 is listed)

#### Scenario: WhatsApp from home page
- **WHEN** a visitor clicks the WhatsApp button from the home page
- **THEN** the prefilled message includes business context, e.g., "Ola, vim pelo site da Madeireira Fontana e gostaria de informacoes sobre madeiras."

#### Scenario: WhatsApp from product card
- **WHEN** a visitor clicks a WhatsApp link from a specific product card (e.g., Cumaru)
- **THEN** the prefilled message includes the product name, e.g., "Ola, vim pelo site da Fontana e gostaria de um orcamento de Cumaru."

#### Scenario: WhatsApp in hero section
- **WHEN** a visitor views the hero section
- **THEN** a WhatsApp CTA button is visible alongside the quote form CTA — not hidden behind scrolling

### Requirement: Prominent quote request form above the fold or easily accessible
The site SHALL include a structured quote request form that is prominently placed and accessible, not buried in the footer.

#### Scenario: Visitor requests a quote
- **WHEN** a visitor fills out the quote form
- **THEN** the form captures: nome (required), email (required), telefone/WhatsApp (required), produto de interesse (optional dropdown with 17 species + "Moveis Rusticos" + "Outro"), and mensagem (optional)

#### Scenario: Form is accessible from multiple points
- **WHEN** a visitor wants to request a quote
- **THEN** the form is reachable from: hero CTA, navigation CTA, per-product "Pedir Orcamento" buttons, and a dedicated contact section — not only from the footer

#### Scenario: Form validation
- **WHEN** a visitor submits the form with missing required fields
- **THEN** the form shows inline validation errors on the specific fields and does not submit

#### Scenario: Form success state
- **WHEN** a visitor successfully submits the form
- **THEN** the form shows a visible success message confirming the submission and expected response time

### Requirement: Primary CTAs visible in hero and throughout the site
The site SHALL display prominent call-to-action buttons replacing the current "Entre em contato" slider buttons that link to an empty contact page.

#### Scenario: Hero CTAs
- **WHEN** a visitor views the hero section
- **THEN** at least two CTAs are visible: one for WhatsApp ("Fale pelo WhatsApp") and one for the quote form ("Solicite um Orcamento") — using contrasting colors (#C69453 gold or #bf0310 red)

#### Scenario: Product section CTA
- **WHEN** a visitor browses product cards
- **THEN** each product card includes a "Pedir Orcamento" action that either scrolls to the quote form with the product pre-selected or opens WhatsApp with the product name prefilled

#### Scenario: CTA button sizing
- **WHEN** CTAs are rendered on mobile
- **THEN** buttons have minimum 44px height, adequate padding, and are visually distinguished from surrounding content

### Requirement: Phone number is click-to-call
The site SHALL render the phone number as a clickable `tel:` link so mobile visitors can call with one tap.

#### Scenario: Mobile visitor taps phone number
- **WHEN** a mobile visitor taps the phone number
- **THEN** the device initiates a phone call to (48) 3258-1500 (currently: phone is displayed as text in the header bar but not as a tappable link on mobile)

#### Scenario: Phone visible in header and footer
- **WHEN** the header or footer is viewed
- **THEN** the phone number (48) 3258-1500 is displayed as a `tel:` link in both locations

### Requirement: Email address is clickable mailto link
The site SHALL render the email address as a `mailto:` link.

#### Scenario: Visitor clicks email
- **WHEN** a visitor clicks the email address
- **THEN** it opens the visitor's email client with the To field prefilled with vendas@fontanamadeireira.com.br (currently: email is a mailto link in the header bar — preserve this behavior)

### Requirement: Contact section consolidates all channels
The site SHALL display all contact channels in a single, prominent contact section.

#### Scenario: Visitor looks for contact options
- **WHEN** a visitor navigates to the contact section
- **THEN** all channels are visible together: phone (click-to-call), WhatsApp (click-to-chat), email (mailto), full address with CEP, quote form, and a map embed or link — all in one section, not split across separate pages

### Requirement: Form captures product interest from catalog context
The site SHALL allow visitors to reach the quote form from a product card with the product name pre-selected.

#### Scenario: Quote from product card
- **WHEN** a visitor clicks "Pedir Orcamento" on the Pinus Autoclave product card
- **THEN** the quote form scrolls into view with "Pinus Autoclave" pre-selected in the product interest dropdown

### Requirement: Payment options displayed as trust signal
The site SHALL display accepted payment methods in a visible section to reduce friction for potential customers.

#### Scenario: Visitor checks payment options
- **WHEN** a visitor looks for payment information
- **THEN** they find a section or footer element listing: Visa, Mastercard, Hipercard, Diners Club, Construcard Caixa, cheque, boleto (PJ), and Losango 24x — with card brand icons where possible (currently: payment info is only in slider text and about page, easy to miss)

#### Scenario: Delivery payment note
- **WHEN** payment options are displayed
- **THEN** the note "Solicite a maquina para cartao e realize o pagamento na entrega" is included as a convenience highlight
