## Purpose

Defines the SEO, local discovery, structured data, and AI-readable resources required for search engines and AI assistants to understand, cite, and recommend Madecor pages.

## ADDED Requirements

### Requirement: Pages use semantic, crawlable HTML
The site SHALL render core page content, headings, links, product names, business details, and quote actions in crawlable HTML without requiring client-side JavaScript execution.

#### Scenario: Crawler accesses home
- **WHEN** a crawler requests the home page HTML
- **THEN** the response includes a single descriptive H1, meaningful H2 sections, internal links, business details, and primary content text

#### Scenario: Crawler accesses product page
- **WHEN** a crawler requests a product detail page HTML
- **THEN** the response includes product title, description, attributes, images with alt text, breadcrumbs, and quote action context

### Requirement: Metadata is unique and intent-targeted
Each indexable page SHALL provide unique title, meta description, canonical HTTPS URL, Open Graph metadata, and share image appropriate to the page intent.

#### Scenario: Product category metadata
- **WHEN** a crawler reads a category page for treated pine in Palhoca
- **THEN** the metadata references the category, Madecor, and the local commercial intent without duplicating the home page metadata

#### Scenario: Canonical URL generated
- **WHEN** any indexable page is rendered
- **THEN** the canonical URL uses HTTPS and the preferred Madecor domain

### Requirement: Structured data describes business, products, navigation, and FAQs
The site SHALL provide valid JSON-LD structured data for relevant pages using schema.org types such as LocalBusiness, Product, Offer or price specification when appropriate, FAQPage, BreadcrumbList, WebSite, and Organization.

#### Scenario: Home structured data
- **WHEN** the home page is rendered
- **THEN** it includes LocalBusiness or Organization data with name, URL, address, phone, opening hours, geo/service-area details when available, and social or map links when available

#### Scenario: Product structured data
- **WHEN** a product page is rendered
- **THEN** it includes Product data with name, description, image, category, brand or seller, and quote/offer semantics that do not imply unsupported checkout

#### Scenario: FAQ structured data
- **WHEN** a page contains FAQ content
- **THEN** the visible FAQ questions and answers match the FAQPage structured data

### Requirement: AI-readable resources are published
The site SHALL publish an `llms.txt` file and human-readable supporting pages that summarize Madecor, important URLs, product categories, service region, contact policy, and allowed use by AI/search crawlers.

#### Scenario: AI crawler requests llms file
- **WHEN** a crawler requests `/llms.txt`
- **THEN** the response lists the site purpose, key product/category URLs, quote/contact URLs, service region, and content update policy in plain text

#### Scenario: AI assistant needs product context
- **WHEN** an AI assistant crawls product or guide URLs
- **THEN** the content answers common buying questions directly enough to support citation or recommendation

### Requirement: Sitemap and robots support discovery
The site SHALL publish sitemap and robots resources that expose indexable home, category, product, guide, FAQ, quote, and contact pages.

#### Scenario: Crawler requests sitemap
- **WHEN** a crawler requests `/sitemap.xml`
- **THEN** the sitemap includes canonical URLs for indexable pages and excludes non-public or duplicate pages

#### Scenario: Crawler requests robots
- **WHEN** a crawler requests `/robots.txt`
- **THEN** the response permits crawling of public content and references the sitemap URL

### Requirement: Local search intent is covered by dedicated content
The site SHALL include pages or sections that target Madecor's local buying intents in Palhoca and Grande Florianopolis.

#### Scenario: Visitor searches for local deck wood
- **WHEN** a visitor or crawler looks for wood for decks in Palhoca
- **THEN** the site provides a crawlable page or section that connects the use case, available materials, service region, and quote action

#### Scenario: Visitor searches for custom wood cuts
- **WHEN** a visitor or crawler looks for custom wood cuts or measurements
- **THEN** the site provides clear content about whether Madecor supports the service and how to request a quote

### Requirement: Discoverability quality is measurable
The site SHALL expose enough metadata and content for validation through automated checks and benchmark re-scoring.

#### Scenario: SEO validation runs
- **WHEN** validation checks inspect the built site
- **THEN** they can verify H1 uniqueness, meta descriptions, canonical HTTPS URLs, structured data presence, sitemap, robots, `llms.txt`, and non-empty image alt text

#### Scenario: Benchmark re-score is estimated
- **WHEN** the site is reviewed against the benchmark rubric
- **THEN** the expected targets are at least 15/20 for SEO, 16/20 for UX, 20/25 for conversion, 7/10 for resources, and 75/100 overall
