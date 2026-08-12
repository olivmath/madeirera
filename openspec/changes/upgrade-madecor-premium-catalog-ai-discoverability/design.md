## Context

See `proposal.md` for motivation. The current benchmark records Madecor at 41.2/100, with weak SEO, shallow product information, duplicated image gallery content, missing structured data, weak proof, and limited digital maturity. The future site should be treated as a quote-driven commercial channel, not as an e-commerce checkout project.

The repo currently contains benchmark artifacts only. This design therefore defines target behavior and architecture for the website to be built later.

## Goals / Non-Goals

**Goals:**

- Create a premium institutional experience that immediately communicates who Madecor is, where it serves, what it sells, and how to request a quote.
- Build a crawlable commercial catalog with category and product pages that support both buyers and search/AI crawlers.
- Make every important page useful without relying on client-side rendering for core content.
- Add structured data, `llms.txt`, sitemap, metadata, FAQs, and local intent pages so search engines and AI assistants can understand and cite the site.
- Improve benchmark readiness with explicit targets for SEO, UX, conversion, resources, and total score.

**Non-Goals:**

- No checkout, online payment, real-time stock, customer account, ERP sync, or logistics calculator in this version.
- No claim of prices, availability, certifications, reviews, or service capabilities unless Madecor can provide real source data.
- No AI chatbot is required for this change; the focus is making the site discoverable and understandable by AI systems.

## Decisions

### Decision: Quote-driven catalog instead of e-commerce

The catalog will use quote/contact CTAs as the primary commercial action. Product pages may show price policy or "sob consulta" explanations, but will not imply online purchase unless operations support it.

**Rationale:** Madecor's benchmark gap is not checkout; it is product clarity, SEO, trust, and lead capture. Quote-first behavior fits custom measurements, delivery, treatment, and product variability.

**Alternative considered:** Full e-commerce with cart and payment. Rejected for v1 because it adds inventory, pricing, payment, freight, and support complexity before the core commercial content is fixed.

### Decision: Content model centered on category, product, guide, proof, and local pages

The site should use explicit content types:

- Category: product family or application area.
- Product: specific product or material page.
- Guide/FAQ: educational content answering buying questions.
- Project/proof: real work, testimonial, review, or credibility asset.
- Local/service page: Palhoca and Grande Florianopolis buying intent.

**Rationale:** These content types map directly to the benchmark gaps and produce clean URLs for SEO and AI retrieval.

**Alternative considered:** One long landing page. Rejected because it would repeat the current weakness: shallow catalog, limited long-tail SEO, and poor crawlable depth.

### Decision: AI discoverability uses open web primitives

The AI discoverability layer will rely on semantic HTML, structured data, `llms.txt`, sitemap, robots, FAQ, and content that directly answers local buying questions.

**Rationale:** Assistants and search engines need stable, crawlable, non-image text. These primitives are measurable and do not require dependence on a specific AI vendor.

**Alternative considered:** Building a custom AI/chat feature. Rejected for v1 because it does not solve the site's discoverability foundation and would add maintenance burden.

### Decision: Trust signals must be content-backed

The site must display only verifiable trust signals: address, phone, service area, map, domain email, project images, real testimonials/reviews, years in market, CNPJ, certifications, or environmental claims when provided by Madecor.

**Rationale:** The benchmark methodology forbids inventing claims. Trust improvements must be defensible and visible to both users and crawlers.

**Alternative considered:** Generic premium copy and stock imagery. Rejected because it weakens credibility and gives crawlers little factual context.

### Decision: Performance and accessibility are acceptance criteria

The build should treat Core Web Vitals, mobile layout, alt text, headings, contrast, labels, and semantic structure as required outcomes, not polish.

**Rationale:** Madecor currently loses points in technical quality, accessibility, and image handling. These issues directly affect conversion, SEO, and benchmark re-score.

**Alternative considered:** Visual redesign first, technical optimization later. Rejected because retrofitting performance and semantics usually forces rework.

## Risks / Trade-offs

- **Missing product data** -> Use a minimal product schema with explicit "sob consulta" fields, but block publication of pages that lack name, category, description, at least one application, and quote path.
- **No real testimonials or project images** -> Launch with verifiable company/location proof and a structured placeholder-free proof section only when real assets exist.
- **Price expectations from catalog pages** -> Use clear quote-based copy and avoid cart language unless checkout is implemented later.
- **AI discoverability over-optimization** -> Keep content written for buyers first; structured data and `llms.txt` summarize factual content already visible on the site.
- **Local SEO claims become stale** -> Centralize NAP, hours, service region, and contact data so updates propagate to pages, schema, sitemap, and `llms.txt`.

## Migration Plan

1. Audit and confirm Madecor's business facts: preferred domain, address, hours, phones, WhatsApp, domain email, service region, product categories, and real trust assets.
2. Build the new information architecture and content model.
3. Implement templates for home, category, product, guide/FAQ, project/proof, quote, and contact pages.
4. Populate initial product/category content for the highest-intent searches first.
5. Add SEO/AI resources: metadata, canonical HTTPS URLs, JSON-LD, sitemap, robots, and `llms.txt`.
6. Run mobile UX checks, structured-data validation, crawl checks, accessibility checks, and performance checks.
7. Redirect old URLs where applicable and monitor 404s, search indexing, and quote events.

Rollback: keep the previous site deployable until the new site passes validation. If launch issues appear, restore the previous deployment and keep DNS/canonical changes reversible.

## Open Questions

- Exact product taxonomy, measurements, service capabilities, and quote fields must be confirmed with Madecor before implementation.
- Real testimonials, review sources, certifications, project images, and company identity data must be supplied or explicitly omitted.
