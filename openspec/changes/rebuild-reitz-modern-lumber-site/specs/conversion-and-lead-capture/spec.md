## Purpose

Defines the quote request forms, CTAs, WhatsApp integration, click-to-call, and lead capture requirements for Reitz's rebuild. The current site has:

- **Zero forms** in the HTML returned to crawlers (PHP includes fail before form renders)
- **5 WhatsApp links** all pointing to the same number (5548999831254) with generic prefilled messages ("Ola, tudo bem?")
- **1 phone number** displayed but not as a clickable tel: link
- **1 email** displayed but not as a mailto: link
- **Zero visible CTAs** — the "ORCAMENTO" nav item exists but no prominent buttons in content
- **Contact form exists in PHP** but depends on broken server-side includes and a reCAPTCHA key that may be stale

The site has a floating WhatsApp button (bottom-left, green, with badge "1" and pulse animation) that works well when the page loads completely. Conversion score is 10.0/25.

## ADDED Requirements

### Requirement: Quote request form captures leads with esquadrias context
The site SHALL include at least one structured quote request form with fields specific to the esquadrias business — emphasizing the custom sizing capability.

#### Scenario: Visitor requests a quote for custom esquadrias
- **WHEN** a visitor fills out the quote form
- **THEN** the form captures: tipo de contato (Orcamento/Duvida — matching existing options), nome (required), telefone ou WhatsApp (required), email (optional), produto de interesse (select: Portas, Janelas, Rodapes/Batentes/Guarnicoes, Fechaduras/Dobradicas/Puxadores, Outro), medida (Padrao / Sob Medida — reflecting the "tamanhos padrao ou sob medida" differentiator), and mensagem

#### Scenario: Form validation
- **WHEN** a visitor submits the form with missing required fields
- **THEN** the form shows inline validation errors on nome and telefone fields and does not submit

#### Scenario: Form success state
- **WHEN** a visitor successfully submits the form
- **THEN** the form shows a visible success message: "Orcamento solicitado! Entraremos em contato em breve."

### Requirement: Primary CTAs are visible in hero and product sections
The site SHALL display prominent call-to-action buttons replacing the current zero-CTA state in the content area.

#### Scenario: Hero CTAs
- **WHEN** a visitor views the hero section
- **THEN** at least two CTAs are visible: "Solicite um Orcamento" (links to quote form) and "Fale pelo WhatsApp" (opens WhatsApp with context) — matching the current "Solicite orcamento" highlight but as proper buttons

#### Scenario: Product section CTA
- **WHEN** a visitor browses product cards
- **THEN** each product card includes a "Pedir Orcamento" or "Consultar" action that links to WhatsApp with the product name prefilled (e.g., "Ola, gostaria de um orcamento para Porta Pivotante")

#### Scenario: CTA button sizing
- **WHEN** CTAs are rendered on mobile
- **THEN** buttons have minimum 44px height, adequate padding, and are visually distinguished with contrasting color

### Requirement: WhatsApp integration preserves current placement with improved context
The site SHALL maintain the WhatsApp button in the bottom-left position (matching the current site) with improved contextual prefilled messages per product category.

#### Scenario: WhatsApp from home page
- **WHEN** a visitor clicks the WhatsApp button from the home page
- **THEN** the prefilled message includes: "Ola, vim pelo site da Reitz Esquadrias e gostaria de informacoes sobre portas e janelas de madeira."

#### Scenario: WhatsApp from product card
- **WHEN** a visitor clicks a WhatsApp link from a Porta Pivotante product card
- **THEN** the prefilled message includes: "Ola, vim pelo site e gostaria de um orcamento para Porta Pivotante."

#### Scenario: WhatsApp button position and style
- **WHEN** a visitor scrolls any page
- **THEN** a floating WhatsApp button remains visible in the bottom-left corner (matching the current site — NOT bottom-right like most sites) with the green (#25D366) background color, using the correct number 5548999831254

#### Scenario: WhatsApp badge removed
- **WHEN** the WhatsApp button is displayed
- **THEN** it does NOT show a fake notification badge with "1" (the current site shows a red badge with "1" which is misleading — it's not a real notification)

### Requirement: Phone number is a click-to-call link
The site SHALL render the phone number (48) 3246-0129 as a clickable `tel:` link everywhere it appears.

#### Scenario: Mobile visitor taps phone number
- **WHEN** a mobile visitor taps the phone number in the header or footer
- **THEN** the device initiates a phone call to (48) 3246-0129 (currently displayed but not clickable)

### Requirement: Email address is a clickable mailto link
The site SHALL render contato@esquadriasreitz.com.br as a `mailto:` link.

#### Scenario: Visitor clicks email
- **WHEN** a visitor clicks the email address
- **THEN** it opens the visitor's email client with the To field prefilled with contato@esquadriasreitz.com.br (currently displayed as plain text in the footer at reduced font-size 10.5px)

### Requirement: Contact section consolidates all channels
The site SHALL display all contact channels in a single, prominent contact section.

#### Scenario: Visitor looks for contact options
- **WHEN** a visitor navigates to the contact section
- **THEN** all channels are visible together: phone (click-to-call), WhatsApp (click-to-chat with context), email (mailto), full address with CEP 88117-001, and a map link or embed — currently split across separate Contato and Localizacao pages

### Requirement: Quote form captures product interest from catalog context
The site SHALL allow visitors to reach the quote form from a product card with the product name and category pre-selected.

#### Scenario: Quote from Porta Pivotante card
- **WHEN** a visitor clicks "Pedir Orcamento" on the Porta Pivotante product card
- **THEN** the quote form scrolls into view with "Portas" selected as the product category and "Porta Pivotante" mentioned in the message field

#### Scenario: Quote form accessible from Orcamento nav item
- **WHEN** a visitor clicks "ORCAMENTO" in the navigation
- **THEN** the page scrolls to the quote form section (matching the current nav structure where ORCAMENTO is a separate page)

### Requirement: Orcamento navigation item is visually distinguished
The site SHALL style the "ORCAMENTO" navigation item as a CTA button, not as a plain text link matching other nav items.

#### Scenario: Desktop navigation
- **WHEN** a visitor views the navigation bar on desktop
- **THEN** the "ORCAMENTO" item has a button-style appearance (background color, rounded corners, contrasting text) distinguishing it from the other 7 nav items

#### Scenario: Mobile navigation
- **WHEN** a visitor opens the mobile menu
- **THEN** the "ORCAMENTO" item is visually highlighted (different background or color) at the top or bottom of the menu list
