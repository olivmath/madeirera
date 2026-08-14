## Purpose

Defines the quote request forms, CTAs, WhatsApp integration, click-to-call, financing visibility, and lead capture requirements to replace Santa Isabel's current zero-conversion state. The existing site has: zero working forms (the contact page has fields but the form handler is unknown/broken), a WhatsApp widget that does not function (flsh.ws bundle), zero visible CTAs, and no mechanism to request a quote for pre-fabricated houses. Conversion score: 2.8/25.

## ADDED Requirements

### Requirement: Quote request form captures leads with project type context
The site SHALL include at least one structured quote request form with fields that capture the visitor's project interest and contact information.

#### Scenario: Visitor requests a house quote
- **WHEN** a visitor fills out the quote form
- **THEN** the form captures: tipo de projeto (Casa de Madeira / Casa de Alvenaria / Kit de Materiais / Outro), nome (required), telefone ou WhatsApp (required), cidade/estado, tamanho aproximado do terreno (optional), and mensagem (currently: contact form exists on contato.html with Nome/Email/Cidade UF/Telefone/Mensagem but is non-functional)

#### Scenario: Form validation
- **WHEN** a visitor submits the form with missing required fields
- **THEN** the form shows inline validation errors on the specific fields and does not submit

#### Scenario: Form success state
- **WHEN** a visitor successfully submits the form
- **THEN** the form shows a visible success message confirming the submission and mentioning the business hours (Mon-Fri 9-12/14-18) as expected response window

### Requirement: Primary CTAs are visible in hero and project sections
The site SHALL display prominent call-to-action buttons in the hero section and after the project showcase, replacing the current zero-CTA state.

#### Scenario: Hero CTA
- **WHEN** a visitor views the hero section
- **THEN** at least two CTAs are visible: one for WhatsApp contact and one for the quote form (e.g., "Solicite um Orcamento" and "Fale pelo WhatsApp")

#### Scenario: Project section CTA
- **WHEN** a visitor browses project categories
- **THEN** each project category (Casas de Madeira, Casas de Alvenaria) includes a "Pedir Orcamento" or "Consultar" action that links to the quote form or opens WhatsApp with the project type prefilled

#### Scenario: CTA button sizing
- **WHEN** CTAs are rendered on mobile
- **THEN** buttons have minimum 44px height, adequate padding, and are visually distinguished from surrounding content with contrasting color

### Requirement: WhatsApp integration replaces broken widget with direct API links
The site SHALL replace the non-functional flsh.ws WhatsApp widget with direct WhatsApp API links that include page and project context in prefilled messages.

#### Scenario: WhatsApp from home page
- **WHEN** a visitor clicks the WhatsApp button from the home page
- **THEN** the prefilled message includes the business context, e.g., "Ola, vim pelo site da Madeireira Santa Isabel e gostaria de informacoes sobre casas pre-fabricadas."

#### Scenario: WhatsApp from project category
- **WHEN** a visitor clicks a WhatsApp link from a specific project category (e.g., Casas de Madeira)
- **THEN** the prefilled message includes the project type, e.g., "Ola, vim pelo site e gostaria de um orcamento para uma casa pre-fabricada de madeira."

#### Scenario: WhatsApp button visibility
- **WHEN** a visitor scrolls any page
- **THEN** a floating WhatsApp button remains visible in the bottom-right corner with the correct number (48) 98454-1738 — replacing the current broken flsh.ws widget

#### Scenario: WhatsApp link uses correct format
- **WHEN** the WhatsApp link is inspected
- **THEN** it uses the format `https://wa.me/5548984541738?text=...` with proper URL encoding (not the broken third-party bundle)

### Requirement: Phone number is a click-to-call link
The site SHALL render the phone number as a clickable `tel:` link so mobile visitors can call with one tap.

#### Scenario: Mobile visitor taps phone number
- **WHEN** a mobile visitor taps the displayed phone number
- **THEN** the device initiates a phone call to (48) 98454-1738 (currently: phone is displayed as plain text in a paragraph)

#### Scenario: Phone number appears in multiple locations
- **WHEN** the hero, contact section, and footer are viewed
- **THEN** the phone number (48) 98454-1738 appears in at least the contact section and footer as a tappable tel: link

### Requirement: Email address is a clickable mailto link
The site SHALL render the email address as a `mailto:` link.

#### Scenario: Visitor clicks email
- **WHEN** a visitor clicks the email address
- **THEN** it opens the visitor's email client with the To field prefilled with contato@madeireirasantaisabel.com.br

### Requirement: Financing options are prominently displayed
The site SHALL display the available financing options near project CTAs to reduce friction in the quote decision.

#### Scenario: Visitor sees financing options
- **WHEN** a visitor views the projects section or quote form area
- **THEN** financing badges or a callout clearly show: "Aceitamos Construcard (Caixa), Construshop (Itau), Visa e MasterCard" — making it clear that financing is available for pre-fabricated house projects

### Requirement: Business hours set response expectations
The site SHALL display business hours prominently in the contact section and footer.

#### Scenario: Visitor checks availability
- **WHEN** a visitor views the contact section or footer
- **THEN** business hours are clearly displayed: "Segunda a Sexta: 9:00 - 12:00 e 14:00 - 18:00" and "Sabados: somente com agendamento" — setting expectations for when to expect a response

### Requirement: Contact section consolidates all channels
The site SHALL display all contact channels in a single contact section, replacing the current minimal contact page.

#### Scenario: Visitor looks for contact options
- **WHEN** a visitor navigates to the contact section
- **THEN** all channels are visible together: phone (click-to-call), WhatsApp (click-to-chat), email (mailto), full address (BR 101 - Km 217 - Pachecos - Palhoca-SC), business hours, social media links (Facebook, YouTube, Instagram), and a map link — without needing to visit a separate page

### Requirement: Social media links are functional and visible
The site SHALL display links to the company's active social media profiles (Facebook, YouTube, Instagram) in both the contact section and footer.

#### Scenario: Visitor clicks social media link
- **WHEN** a visitor clicks the Instagram icon
- **THEN** it opens https://www.instagram.com/casasprefabricadassantaisabel in a new tab (the current site has these links and they work — preserve this behavior)

### Requirement: Form captures project type from showcase context
The site SHALL allow visitors to reach the quote form from a project category with the type pre-selected.

#### Scenario: Quote from project showcase
- **WHEN** a visitor clicks "Pedir Orcamento" on the "Casas de Madeira" category
- **THEN** the quote form scrolls into view with "Casa de Madeira" pre-selected in the project type field
