## Context

See `proposal.md` for motivation. Santa Isabel scores 23.1/100 — rated "Critico" in the benchmark. The Adobe Muse-generated site uses absolute positioning, has zero responsive behavior, zero semantic headings, 57 images without alt text, and a broken WhatsApp widget. The CMS was discontinued by Adobe in 2018 — the site is frozen and cannot be patched.

The business has been operating since 1945 (80+ years) with a compelling family succession story, specializes in pre-fabricated houses (wood and masonry), has a 1,200m2 facility, active reforestation program, and accepts multiple financing options. This heritage and specialization are completely buried in the current site's dated layout.

## Goals / Non-Goals

**Goals:**

- Build a mobile-first responsive site that works on all screen sizes (current site is completely broken on mobile with no viewport meta tag).
- Leverage the 80-year heritage (since 1945) as the primary trust signal — this is the oldest lumber yard in the benchmark.
- Create a project showcase for pre-fabricated houses (wood and masonry/concrete categories) with photo galleries.
- Add at least one quote/contact form to capture leads (currently zero forms, broken WhatsApp).
- Implement basic SEO: one H1 per page, H2 sections, meta descriptions, structured data, alt text on all images (currently zero on 57 images).
- Integrate sustainability/reforestation content as a differentiator (competitors don't have this).
- Present the business hours, financing options, and construction tips as value-add content.

**Non-Goals:**

- No e-commerce checkout, cart, or online payment.
- No customer accounts or login system.
- No real-time pricing (projects use quote-based pricing).
- No AI chatbot or advanced search functionality.
- No custom CMS — the prototype is a static HTML site.

## Decisions

### Decision: Full rebuild as static HTML prototype

The site will be rebuilt as a self-contained HTML/CSS/JS prototype, not patched from Adobe Muse output.

**Rationale:** Adobe Muse generates non-semantic div layouts with absolute positioning, CSS sprites for menu text (rendered as images, not text), and jQuery 1.8.3 dependencies. The markup is non-recoverable — every element position is hardcoded in pixels. There is no responsive behavior, no viewport meta, and menu items are literal PNG images instead of text.

**Alternative considered:** Extracting content and migrating to a CMS. Deferred to implementation phase; the prototype proves the design first.

### Decision: Heritage-first visual identity with warm wood tones

The site will lead with the 1945 founding story as the hero centerpiece, using a color palette of warm browns, dark wood tones, and forest greens. A timeline element (1945 -> 1980 -> 1994 -> today) should be prominent.

**Rationale:** Santa Isabel is the oldest lumber yard in the benchmark by a wide margin. This heritage is currently buried in a "credibilidade" sidebar blurb. The 80-year story of manual extraction, family succession, and expansion to Palhoca is a powerful differentiator that no competitor can match. The design should make this history the first thing visitors see.

**Alternative considered:** Leading with products/projects first (like most competitor sites). Rejected because heritage IS the differentiator — products are similar across competitors, but no one else has 80 years of history.

### Decision: Single-page prototype with anchor navigation

The prototype will be a single HTML file with sections (hero, heritage, projects, sustainability, contact, footer) navigable via anchor links, rather than multi-page.

**Rationale:** The prototype's purpose is to demonstrate the visual and structural improvement to the client. A single file is easier to share, review, and iterate on. The current site has 8+ pages; the multi-page architecture is defined in specs for the production build.

**Alternative considered:** Multi-page prototype mirroring the current 8-page structure. Unnecessary complexity for a client presentation artifact.

### Decision: Project showcase uses two categories with gallery approach

The showcase will organize projects into two categories matching the business offering: Casas de Madeira and Casas de Alvenaria/Concreto. Each category shows completed project photos from the show room with brief descriptions.

**Rationale:** The current site separates "Projetos" and "Show Room" but both show the same content — completed house projects. Merging them into a single project gallery with category filters is cleaner and more effective for conversion (see -> want -> quote).

### Decision: Sustainability section as competitive differentiator

The reforestation/sustainability content will be a dedicated section, not buried in a submenu. It will include the company's environmental commitment, reforestation photos, and a statement about sourcing practices.

**Rationale:** Among 20+ competitors in the benchmark, Santa Isabel is one of the very few with any sustainability content. In 2026, environmental responsibility is a purchasing factor. Elevating this from a hidden "Social" page to a visible section adds trust and differentiation.

### Decision: Construction tips as value-add content

The "Dicas" (tips) content will be included as a compact FAQ-style section near the contact area, providing practical construction advice.

**Rationale:** This content demonstrates expertise and helps with SEO (long-tail keywords). It also gives visitors a reason to spend more time on the page, building trust before they request a quote.

## Risks / Trade-offs

- **No real project photos in prototype** -> Use placeholder areas with clear "foto do projeto" labels sourced from the show room page descriptions. Block production launch until real photos are selected.
- **Single phone number** -> Only one phone number is listed ((48) 98454-1738). Confirm whether this is also the WhatsApp number and whether there are additional lines.
- **Heritage year calculation** -> The site says 1945. In 2026, that's 81 years. Use "Desde 1945" and "Mais de 80 anos" as the trust claim.
- **WhatsApp widget broken** -> The current widget (flsh.ws bundle) doesn't work. The prototype will use a direct WhatsApp API link instead of a third-party widget.
- **Business hours limited** -> Mon-Fri 9:00-12:00 and 14:00-18:00, Saturday by appointment only. Display these clearly to set expectations.
- **Financing options may have changed** -> The site mentions Construcard, Construshop, Visa, MasterCard. Confirm current options before production.

## Open Questions

- Is (48) 98454-1738 the WhatsApp number? Are there additional phone lines?
- Are Construcard/Construshop/credit card financing options still available?
- Does the business serve delivery/construction beyond Santa Catarina?
- Are the reforestation areas still active? Any recent photos or certifications?
- What is the current average number of houses built (site says ~350 as of writing)?
- Is the Sao Bonifacio original location still operational, or only the Palhoca facility?
