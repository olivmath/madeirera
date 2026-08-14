## Purpose

Defines improvements to the existing responsive layout — hero section refinement, product showcase with proper image presentation, navigation fixes (broken 404 link), and footer consolidation. Unlike Baia Sul which required a full rebuild from a 2014 fixed-width layout, Ceratto already has a functional responsive site (WordPress + Astra + Elementor). The focus is on structural fixes, not a redesign.

## ADDED Requirements

### Requirement: Navigation links all resolve without errors
The site SHALL have all navigation items linking to functional pages — no 404 errors.

#### Scenario: Visitor clicks Moveis e Construcoes
- **WHEN** a visitor clicks "Moveis e Construcoes" in the navigation
- **THEN** the page loads with the product catalog showing priced items (Kit Tabuas, Tabua Churrasco, Petisqueiras) and category galleries (currently: returns 404 error)

#### Scenario: All menu items functional
- **WHEN** a visitor tests each menu item (Inicio, Moveis e Construcoes, Contato)
- **THEN** all three resolve to their respective content without errors or dead links

### Requirement: Hero section communicates business identity and next action
The site SHALL present Ceratto's positioning, service region, and primary CTA in the first viewport — refining the existing hero rather than rebuilding it.

#### Scenario: Visitor lands on home page
- **WHEN** a visitor opens the home page
- **THEN** the visitor can identify: (1) business name "Ceratto Madeiras", (2) location "Biguacu e Regiao", (3) value proposition "Madeiras de Qualidade Vindas do Norte do Pais", (4) a CTA to request a quote or contact via WhatsApp — all without scrolling on mobile (existing structure is close; needs a quote CTA button added)

#### Scenario: Hero includes trust signals
- **WHEN** a visitor views the hero section
- **THEN** the hero communicates quality positioning and product origin ("vindas do norte do pais") as text — the existing content is adequate but needs a form CTA added alongside the WhatsApp button

### Requirement: Product catalog displays all 8 wood species with proper labeling
The site SHALL display all 8 wood species currently shown on the home page with correct names, accurate descriptions, and descriptive images.

#### Scenario: Visitor browses wood species
- **WHEN** a visitor scrolls to the product catalog section
- **THEN** the visitor sees cards for all 8 species (Itauba, Cambara, Garapeira, Cedro, Tatajuba, Angelim Pedra, Roxinho, Longarina) with: species name as heading, accurate description, and product photo with alt text

#### Scenario: Tatajuba description is corrected
- **WHEN** the Tatajuba product card is displayed
- **THEN** the description reads "Madeira Tatajuba de alta qualidade" NOT "Madeira Eucalipto de alta qualidade" (current data error)

#### Scenario: Product cards on mobile
- **WHEN** a visitor views products on mobile
- **THEN** product cards stack vertically with readable text and tappable elements (existing Elementor grid already handles this; alt text and descriptions are the fix)

### Requirement: Priced products section showcases unique offerings
The site SHALL display the priced product line (cutting boards, BBQ boards, petisqueiras) with exact prices, materials, and dimensions — preserving this competitive advantage.

#### Scenario: Visitor views priced products
- **WHEN** a visitor navigates to the Moveis e Construcoes content
- **THEN** the visitor sees: Kit Tabuas de Cozinha R$450 (3 tabuas + suporte, angelim-pedra), Tabua de Churrasco R$200 (itauba ou roxinho, 28x47cm), Petisqueira Redondo R$150, Petisqueira Hexagonal R$150 — all with photos and material details

### Requirement: Footer displays complete contact information
The site SHALL display all business contact details in the footer: address, phone (click-to-call), WhatsApp (click-to-chat), email, business hours, and service area.

#### Scenario: Visitor checks footer
- **WHEN** a visitor scrolls to the footer/contact section
- **THEN** the footer shows: Rua Sebastiao Lara, 300, Universitario - Biguacu - SC, phone (48) 3285-3293 as click-to-call, WhatsApp (48) 99961-1658 as click-to-chat, email cerattomadeiras@gmail.com as mailto, hours Mon-Fri 08:00-12:00 / 13:30-18:00, and service area listing (existing content is mostly correct; needs click-to-call and mailto links verified)

### Requirement: Site uses correct language declaration
The site SHALL declare `lang="pt-BR"` on the HTML element.

#### Scenario: Language attribute
- **WHEN** the HTML source is inspected
- **THEN** the html element has `lang="pt-BR"` (currently: `lang="en-US"` which is incorrect for Portuguese content)
