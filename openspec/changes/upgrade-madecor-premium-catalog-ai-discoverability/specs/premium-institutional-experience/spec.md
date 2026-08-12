## Purpose

Defines the externally visible website experience that makes Madecor feel trustworthy, premium, local, and commercially easy to contact from desktop and mobile.

## ADDED Requirements

### Requirement: Premium home page communicates position and next action
The site SHALL present Madecor's main positioning, service region, product categories, trust signals, and primary quote/contact actions in the first meaningful viewport.

#### Scenario: Visitor lands on home
- **WHEN** a visitor opens the home page
- **THEN** the visitor can identify Madecor's business, location, main product/service categories, and how to request a quote without opening a menu

#### Scenario: Mobile visitor lands on home
- **WHEN** a visitor opens the home page on a mobile viewport
- **THEN** the primary quote or WhatsApp action remains visible or reachable without layout overlap, horizontal scrolling, or hidden text

### Requirement: Navigation supports buying and trust tasks
The site SHALL provide predictable navigation to products, quote request, projects or proof, company information, and contact/location details.

#### Scenario: User searches for product information
- **WHEN** a visitor wants to find a product category
- **THEN** the visitor can reach the product catalog from the main navigation in one action

#### Scenario: User checks company credibility
- **WHEN** a visitor wants to verify that Madecor is a real local business
- **THEN** the visitor can reach address, hours, phone, map, company identifiers, and service region from navigation or footer links

### Requirement: Trust signals are visible and verifiable
The site SHALL display trust signals including company identity, local address, map/location, business contact channels, service region, testimonials or review excerpts, and project/gallery evidence.

#### Scenario: Visitor evaluates credibility
- **WHEN** a visitor reviews the home page or footer
- **THEN** the visitor sees at least three trust signals without depending on image-only text

#### Scenario: Visitor opens a project or proof section
- **WHEN** a visitor opens projects, testimonials, or reviews
- **THEN** the content identifies the type of work or customer proof clearly enough to support a buying decision

### Requirement: Contact channels are professional and contextual
The site SHALL expose professional contact options including WhatsApp, phone, address, map, and a domain-based email address.

#### Scenario: Visitor chooses WhatsApp
- **WHEN** a visitor clicks a WhatsApp action from a page context
- **THEN** the generated message includes the relevant page or product context when available

#### Scenario: Visitor checks email
- **WHEN** a visitor views contact details
- **THEN** the email address uses a Madecor-controlled domain rather than a generic personal email provider

### Requirement: Mobile experience satisfies benchmark UX tasks
The site SHALL support the benchmark UX tasks on mobile without broken layouts, unreadable text, or hidden controls.

#### Scenario: Benchmark contact task
- **WHEN** a mobile visitor attempts to find WhatsApp or phone
- **THEN** the visitor can find a working contact path within 30 seconds

#### Scenario: Benchmark location task
- **WHEN** a mobile visitor attempts to find address and hours
- **THEN** the visitor can find location and hours within 45 seconds
