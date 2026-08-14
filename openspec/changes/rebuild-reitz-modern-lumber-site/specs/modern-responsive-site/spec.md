## Purpose

Defines the responsive layout, mobile-first design, navigation, hero section, esquadrias product showcase, footer, and overall site structure that replaces Reitz's broken PHP/TAGX site. The current site uses a modified "Nevada" theme with IE8/IE9 conditional comments, references discontinued HTTP scripts, and has a critical SSL mismatch (cert belongs to uni5.net). While the site has a viewport meta tag and mobile menu trigger, the underlying infrastructure failures prevent the site from rendering for many visitors.

The rebuild preserves the strong product content (20 images with excellent alt text, 4 product categories) while fixing every structural and infrastructure deficiency.

## ADDED Requirements

### Requirement: Site uses mobile-first responsive layout
The site SHALL render correctly on all viewport widths from 320px to 1920px+ without horizontal scrolling, text overflow, or layout breakage.

#### Scenario: Mobile visitor opens the site
- **WHEN** a visitor opens the site on a 375px-wide mobile screen
- **THEN** the layout adapts to the viewport width, text is readable without zooming, and all interactive elements are tappable (minimum 44x44px touch targets)

#### Scenario: Desktop visitor opens the site
- **WHEN** a visitor opens the site on a 1440px desktop screen
- **THEN** the layout uses the available width with a max-width container, product cards display in a multi-column grid, and navigation is fully visible

#### Scenario: Viewport meta tag is present
- **WHEN** the HTML source is inspected
- **THEN** a `<meta name="viewport" content="width=device-width, initial-scale=1">` tag is present (the current site has this but with `maximum-scale=1` which blocks pinch-to-zoom — remove the restriction)

### Requirement: Hero section showcases esquadrias specialization and manufacturing
The site SHALL present Reitz's esquadrias niche, manufacturing capability, years in market, and primary CTA in the first viewport — replacing the current slider-only approach that depends on external image loading.

#### Scenario: Visitor lands on home page
- **WHEN** a visitor opens the home page
- **THEN** the visitor can identify: (1) business name "Reitz Esquadrias e Madeiras", (2) core offering "portas, janelas e esquadrias de madeira", (3) differentiator "fabricacao propria" and "sob medida", (4) a CTA to request a quote or contact via WhatsApp — all without scrolling on a 667px-tall mobile viewport

#### Scenario: Hero includes trust signals
- **WHEN** a visitor views the hero section
- **THEN** the hero includes at least two trust signals: years in market ("Desde 1993" / "Mais de 30 anos") and manufacturing capability ("fabricacao propria") as text, not as image-only elements

#### Scenario: Hero does not depend on external image servers
- **WHEN** the hero section loads
- **THEN** the hero content (text, CTAs, trust signals) renders even if product images fail to load — the current site depends on images from solucao782.tagx.com.br which may be unavailable

### Requirement: Navigation matches existing site architecture
The site SHALL provide navigation to all current sections: Home, Empresa, Produtos (with sub-menu for Portas, Janelas, Batentes/Guarnicoes, Fechaduras/Dobradicas/Puxadores), Servicos, Portfolio, Localizacao, Contato, Orcamento — with responsive behavior.

#### Scenario: Mobile navigation
- **WHEN** a visitor opens the site on mobile
- **THEN** the navigation collapses into a hamburger/toggle menu (the current site has a "Menu Site" trigger — improve to a standard hamburger icon)

#### Scenario: Desktop navigation
- **WHEN** a visitor opens the site on desktop
- **THEN** all navigation links are visible in a horizontal bar, with the Produtos dropdown accessible on hover/click

#### Scenario: Navigation includes quote CTA
- **WHEN** a visitor views the navigation bar
- **THEN** the "ORCAMENTO" item is visually distinguished as a CTA (button style, contrasting color) — currently it's styled the same as all other nav items

### Requirement: Product showcase displays all products organized by category
The site SHALL display products organized by the 4 existing categories, preserving the excellent alt text on each product image.

#### Scenario: Visitor browses Portas
- **WHEN** a visitor scrolls to or navigates to the Portas section
- **THEN** the visitor sees cards for: Porta Pivotante, Porta Estilo Mineiro, Porta Georgia, Porta Windsor — each with image placeholder (preserving the original alt text), product name, and a quote CTA

#### Scenario: Visitor browses Janelas
- **WHEN** a visitor navigates to the Janelas section
- **THEN** the visitor sees cards for: Janela Bay Window de Madeira, Janela Maxim-Ar de Madeira, Janela Basculante de Madeira, Janela de Correr de Madeira

#### Scenario: Visitor browses Batentes/Guarnicoes
- **WHEN** a visitor navigates to the Rodapes/Batentes/Guarnicoes section
- **THEN** the visitor sees cards for: Batentes de Madeira, Rodapes de Madeira, Filetes de Madeira, Vistas de Madeira

#### Scenario: Product cards on mobile
- **WHEN** a visitor views products on a mobile viewport
- **THEN** product cards stack in a single column or 2-column grid with readable text and tappable quote CTA per card

#### Scenario: Product cards on desktop
- **WHEN** a visitor views products on a desktop viewport
- **THEN** product cards display in a 3-4 column grid layout (the current site uses a 4-column layout)

### Requirement: Footer displays complete contact information and product links
The site SHALL display all business details in the footer, matching the current 4-column footer structure: About, Products, Payment Methods, Address/Contact.

#### Scenario: Visitor checks footer
- **WHEN** a visitor scrolls to the footer
- **THEN** the footer shows: (1) Company description with founding year, (2) Product category links, (3) Payment methods indication, (4) Full address Av. Leoberto Leal, 699 - Barreiros, Sao Jose/SC, 88117-001, phone as click-to-call, WhatsApp as click-to-chat, email as mailto link

#### Scenario: Footer on mobile
- **WHEN** a visitor views the footer on mobile
- **THEN** the 4 columns stack vertically with adequate spacing and all links are tappable

### Requirement: Site uses a warm, wood-craft visual identity
The site SHALL use a color palette and typography that communicates "wood craftsman / esquadrias manufacturer" — warm wood browns, craft tones — replacing the current gray (#666666) and teal (#2C97C3) palette.

#### Scenario: Visual identity communicates esquadrias specialization
- **WHEN** a visitor opens the site
- **THEN** the color scheme, imagery, and typography create an immediate visual association with wood craftsmanship and esquadrias, not a generic corporate page

#### Scenario: Accessibility contrast requirements
- **WHEN** text is displayed on any background
- **THEN** the color combination meets WCAG AA contrast ratio (4.5:1 for body text, 3:1 for large text)

### Requirement: Site does not reference discontinued or insecure resources
The site SHALL NOT reference any HTTP-only resources, discontinued services (Google Code), or IE-specific conditional comments.

#### Scenario: No IE conditional comments
- **WHEN** the HTML source is inspected
- **THEN** there are zero `<!--[if IE]>` or `<!--[if lte IE 8]>` blocks (the current site has 3 such blocks)

#### Scenario: No HTTP resource references
- **WHEN** the HTML source is inspected
- **THEN** all external resource references (scripts, stylesheets, images, fonts) use HTTPS or protocol-relative URLs — no `http://` prefixed resources (the current site references jQuery, Google Fonts, and product images via HTTP)
