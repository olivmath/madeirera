## Purpose

Defines the responsive layout, mobile-first design, navigation, heritage-focused hero section, project showcase, sustainability section, footer, and overall site structure that replaces Santa Isabel's Adobe Muse fixed-width layout with absolute positioning. The current site has no viewport meta tag, uses CSS sprites for menu text (PNG images instead of real text), and is completely broken on mobile devices. UI score: 3.4/15, UX score: 5.4/20.

## ADDED Requirements

### Requirement: Site uses mobile-first responsive layout
The site SHALL render correctly on all viewport widths from 320px to 1920px+ without horizontal scrolling, text overflow, or layout breakage.

#### Scenario: Mobile visitor opens the site
- **WHEN** a visitor opens the site on a 375px-wide mobile screen
- **THEN** the layout adapts to the viewport width, text is readable without zooming, and all interactive elements are tappable (minimum 44x44px touch targets)

#### Scenario: Desktop visitor opens the site
- **WHEN** a visitor opens the site on a 1440px desktop screen
- **THEN** the layout uses the available width with a max-width container, project cards display in a multi-column grid, and navigation is fully visible

#### Scenario: Viewport meta tag is present
- **WHEN** the HTML source is inspected
- **THEN** a `<meta name="viewport" content="width=device-width, initial-scale=1">` tag is present in the head (currently missing entirely — the Adobe Muse output has no viewport meta)

### Requirement: Hero section leads with 80-year heritage and business identity
The site SHALL present Santa Isabel's 1945 founding, pre-fabricated house specialization, and primary CTAs in the first meaningful viewport — replacing the current dated slideshow with PNG-text overlays.

#### Scenario: Visitor lands on home page
- **WHEN** a visitor opens the home page
- **THEN** the visitor can identify: (1) business name "Madeireira Santa Isabel", (2) heritage claim "Desde 1945", (3) specialization "Casas Pre-Fabricadas em Madeira e Alvenaria", (4) a CTA to request a quote or contact via WhatsApp — all without scrolling on a 667px-tall mobile viewport

#### Scenario: Hero includes heritage trust signal
- **WHEN** a visitor views the hero section
- **THEN** the hero includes at least one heritage trust signal ("Desde 1945", "Mais de 80 anos de experiencia", or "Mais de 350 casas construidas") as text, not as a rasterized image (the current site renders section titles as PNG images)

#### Scenario: Hero differentiates from competitors
- **WHEN** a visitor compares the hero with competitor sites
- **THEN** the heritage timeline (1945 founding) is visually prominent, making it immediately clear this is the oldest lumber yard in the region

### Requirement: Heritage timeline section tells the company story
The site SHALL include a visual timeline section showing the three key milestones: 1945 (founding in Sao Bonifacio), 1980 (family succession), 1994 (Palhoca expansion).

#### Scenario: Visitor scrolls to heritage section
- **WHEN** a visitor scrolls to the heritage/about section
- **THEN** the visitor sees a visual timeline with at least three dated milestones (1945, 1980, 1994) with brief descriptions of each era, telling the story from manual extraction to modern pre-fabricated houses

#### Scenario: Heritage section on mobile
- **WHEN** a visitor views the heritage section on a mobile viewport
- **THEN** the timeline displays vertically with dates, descriptions, and optional imagery stacked in chronological order, fully readable without horizontal scrolling

### Requirement: Navigation supports all site sections
The site SHALL provide navigation to heritage, projects, sustainability, construction tips, and contact — consolidating the current 8+ page structure into clear sections with responsive behavior.

#### Scenario: Mobile navigation
- **WHEN** a visitor opens the site on mobile
- **THEN** the navigation collapses into a hamburger/toggle menu that expands to show all section links (replacing the current PNG-sprite menu items that are unreadable on mobile)

#### Scenario: Desktop navigation
- **WHEN** a visitor opens the site on desktop
- **THEN** all navigation links are visible in a horizontal bar without requiring a menu toggle

#### Scenario: Navigation includes quote CTA
- **WHEN** a visitor views the navigation bar
- **THEN** at least one navigation element links directly to the quote/contact section, visually distinguished as a CTA (button style, contrasting color)

### Requirement: Project showcase displays house categories with galleries
The site SHALL display projects organized by construction type (wood and masonry/concrete), each with photo galleries and descriptions, replacing the current separated "Projetos" and "Show Room" pages.

#### Scenario: Visitor browses projects
- **WHEN** a visitor scrolls to or navigates to the projects section
- **THEN** the visitor sees two main categories: "Casas de Madeira" and "Casas de Alvenaria e Concreto", each with: category description, photo gallery area, and a quote CTA

#### Scenario: Project cards on mobile
- **WHEN** a visitor views projects on a mobile viewport
- **THEN** project categories stack vertically with full-width photos and readable descriptions

#### Scenario: Project cards on desktop
- **WHEN** a visitor views projects on a desktop viewport
- **THEN** project categories display side-by-side or in a 2-column grid with larger photo galleries

#### Scenario: Financing information is visible
- **WHEN** a visitor views the projects section
- **THEN** the financing options (Construcard, Construshop, Visa, MasterCard) are displayed as badges or a callout near the project CTAs

### Requirement: Sustainability section showcases reforestation commitment
The site SHALL include a dedicated sustainability section highlighting the company's reforestation program and environmental practices, elevated from the current hidden "Social" submenu page.

#### Scenario: Visitor sees sustainability content
- **WHEN** a visitor scrolls to the sustainability section
- **THEN** the visitor sees: a statement about the company's environmental commitment, reference to reforestation activities, and a photo area for reforestation imagery

#### Scenario: Sustainability as differentiator
- **WHEN** a visitor evaluates the business
- **THEN** the sustainability section is visible in the main page flow (not hidden in a submenu), positioned as a trust signal alongside the heritage timeline

### Requirement: Construction tips section adds value
The site SHALL include a compact section with practical construction tips from the existing "Dicas" content, presented as an FAQ or accordion.

#### Scenario: Visitor reads construction tips
- **WHEN** a visitor navigates to the tips section
- **THEN** tips are organized in three categories (Antes de Construir, Durante a Construcao, Apos a Construcao) with expandable/collapsible items

### Requirement: Footer displays complete contact information and business hours
The site SHALL display all business contact details in the footer: full address, phone, email, WhatsApp link, social media links, and business hours — replacing the current minimal footer that only shows a copyright line.

#### Scenario: Visitor checks footer
- **WHEN** a visitor scrolls to the footer
- **THEN** the footer shows: BR 101 - Km 217 - Pachecos - Palhoca-SC, phone (48) 98454-1738 as click-to-call, email as mailto link, WhatsApp link, social media icons (Facebook, YouTube, Instagram), business hours (Mon-Fri 9-12/14-18, Sat by appointment), and a "ver no mapa" link

#### Scenario: Footer on mobile
- **WHEN** a visitor views the footer on mobile
- **THEN** contact items stack vertically with adequate spacing and all links are tappable

### Requirement: Site uses a warm, heritage-appropriate visual identity
The site SHALL use a color palette and typography that communicates "established lumber yard with decades of history" — warm wood tones, earth colors, forest greens — replacing the current generic Adobe Muse styling.

#### Scenario: Visual identity communicates heritage and product
- **WHEN** a visitor opens the site
- **THEN** the color scheme, imagery, and typography create an immediate visual association with wood/lumber and heritage rather than a generic corporate identity

#### Scenario: Accessibility contrast requirements
- **WHEN** text is displayed on any background
- **THEN** the color combination meets WCAG AA contrast ratio (4.5:1 for body text, 3:1 for large text)

### Requirement: Facility details are visible
The site SHALL include the company's infrastructure details (1,200m2 yard, 525m2 built area, modern equipment) as supporting trust content.

#### Scenario: Visitor wants to assess business scale
- **WHEN** a visitor looks for business credibility indicators
- **THEN** the site displays facility size (1,200m2 yard, 525m2 built), equipment capabilities, and BR-101 show room location within the heritage or about section
