## Purpose

Defines the catalog, product, filtering, product education, and quote behavior required to turn Madecor's website into a useful commercial channel without requiring checkout.

## ADDED Requirements

### Requirement: Catalog exposes category pages
The site SHALL provide crawlable category pages for Madecor's main commercial product groups and applications.

#### Scenario: Visitor opens products
- **WHEN** a visitor opens the products area
- **THEN** the visitor sees clear categories for major product groups and use cases such as construction wood, decks, roofing, doors/windows, boards, treated wood, and custom cuts when applicable

#### Scenario: Search engine crawls category
- **WHEN** a crawler accesses a category URL directly
- **THEN** the page returns indexable HTML with category title, description, product links, and quote action

### Requirement: Catalog supports commercial filtering
The catalog SHALL allow visitors to narrow products by commercially meaningful attributes.

#### Scenario: Visitor filters by use case
- **WHEN** a visitor filters products by application
- **THEN** the catalog shows matching products or categories and keeps a path to request a quote for the filtered interest

#### Scenario: Visitor filters by product attributes
- **WHEN** a visitor filters by species, treatment, dimensions, or availability state
- **THEN** the catalog updates the visible result set without losing the visitor's current intent

### Requirement: Product pages include decision-grade information
Each product detail page SHALL include product name, images, description, applications, species or material, treatment, dimensions or available formats, availability/pricing policy, delivery or service-area notes, and quote actions.

#### Scenario: Visitor reviews a product page
- **WHEN** a visitor opens a product detail page
- **THEN** the visitor can understand what the product is, where it is used, what technical options exist, and how to ask for a quote

#### Scenario: Product has no fixed price
- **WHEN** a product is sold by quote rather than fixed price
- **THEN** the page explains that pricing depends on measurements, quantity, treatment, delivery, or other relevant variables

### Requirement: Quote flow captures product intent
The quote flow SHALL capture enough context to make a sales response useful while keeping the form short.

#### Scenario: Visitor requests quote from product page
- **WHEN** a visitor starts a quote from a product page
- **THEN** the quote request includes product/category context and asks for name, phone or WhatsApp, city, quantity or measurements, and optional notes

#### Scenario: Visitor requests quote without specific product
- **WHEN** a visitor starts a general quote
- **THEN** the form allows the visitor to describe the project and optionally select a category or application

### Requirement: Product education supports buying decisions
The catalog SHALL include practical guidance that helps visitors choose materials by application, treatment, durability, maintenance, and local use cases.

#### Scenario: Visitor compares materials
- **WHEN** a visitor reads category or guide content
- **THEN** the content explains relevant differences such as treated vs untreated wood, deck suitability, outdoor use, roofing use, and measurement considerations

#### Scenario: Visitor needs help choosing
- **WHEN** a visitor is unsure which product fits the project
- **THEN** the site offers a path to request help with the application or project details

### Requirement: Catalog avoids false e-commerce expectations
The catalog SHALL not present checkout, payment, or real-time stock behavior unless those operational capabilities exist.

#### Scenario: Visitor sees quote-based product
- **WHEN** a product does not support online purchase
- **THEN** the primary action is quote/contact rather than add-to-cart or checkout
