## Context

See `proposal.md` for motivation. Reitz scores 38.7/100 — in the "Critico" tier. The PHP/TAGX site uses a "Nevada" theme with IE8/IE9 conditional comments, has a critical SSL hostname mismatch (cert belongs to uni5.net), and the server returns incomplete HTML to crawlers. Despite the infrastructure failures, the site has strong product content: 20 images with excellent alt text, clear product categories (portas, janelas, batentes, guarnicoes, fechaduras), and a specialized niche in wood esquadrias since 1993.

The rebuild must fix the critical infrastructure issues while preserving the strong product content and esquadrias specialization.

## Goals / Non-Goals

**Goals:**

- Fix SSL and server rendering so the site is actually accessible to visitors and crawlers.
- Build a mobile-first responsive site showcasing the esquadrias specialization (doors, windows, frames).
- Organize products by category: Portas, Janelas, Rodapes/Batentes/Guarnicoes, Fechaduras/Dobradicas/Puxadores.
- Add at least one quote/contact form for custom esquadrias (currently zero forms).
- Implement proper SEO: fix lang tag, add H1, meta description, structured data.
- Preserve the excellent alt text practice already present on all 20 images.
- Present Reitz as a specialized manufacturer with 33+ years of experience.

**Non-Goals:**

- No e-commerce checkout, cart, or online payment.
- No customer accounts or login system.
- No real-time inventory or pricing (esquadrias use quote-based pricing, especially custom sizes).
- No AI chatbot or advanced search.
- No custom CMS — the prototype is a static HTML site.

## Decisions

### Decision: Full rebuild as static HTML prototype

The site will be rebuilt as a self-contained HTML/CSS/JS prototype, not patched from the PHP/TAGX codebase.

**Rationale:** The current site has two critical infrastructure failures (SSL mismatch, broken PHP includes) plus a codebase referencing IE8/IE9 with conditional comments. The "Nevada" theme CSS is heavily customized with inline styles across 4000+ lines. There is no recoverable template or content model. Everything must be rewritten.

**Alternative considered:** Fixing the PHP includes and SSL. The PHP code depends on TAGX's proprietary CMS (solucao782.tagx.com.br), making server-side fixes impractical without the original developer.

### Decision: Wood and craft-focused visual identity

The site will use a warm color palette inspired by wood craft and carpentry: rich wood browns, warm creams, and accent green (from the existing WhatsApp green #25D366 as interaction cue). This replaces the current gray/blue corporate palette (#666666 theme color, #2C97C3 phone highlight).

**Rationale:** Reitz is a manufacturer/factory, not a retailer. The visual identity should communicate craftsmanship and wood expertise. The current site uses generic corporate colors that don't convey the esquadrias/woodworking identity. Competitors with higher scores use wood-toned palettes.

**Alternative considered:** Keeping the existing gray/teal palette. Rejected — it communicates "generic business" rather than "wood craftsman."

### Decision: Single-page prototype with anchor navigation

The prototype will be a single HTML file with sections (hero, about, products by category, services, quote form, contact, footer) navigable via anchor links.

**Rationale:** The current site has 8 navigation items (Home, Empresa, Produtos with 4 sub-items, Servicos, Portfolio, Localizacao, Contato, Orcamento). A single-page prototype demonstrates the visual and structural improvement for the client presentation. Multi-page architecture is defined in specs for production.

### Decision: Product showcase organized by existing categories

The product showcase will display items organized by the 4 categories already on the site: Portas (4 products shown), Janelas (4 products), Rodapes/Batentes/Guarnicoes (4 products), and Fechaduras/Dobradicas/Puxadores. Each product card includes a photo placeholder, the product name, and a quote CTA.

**Rationale:** The current site already has well-organized product categories with excellent alt text on every image. This structure works and should be preserved. The prototype shows the visual improvement while maintaining the information architecture.

### Decision: Preserve and enhance the existing alt text standard

All images in the prototype will have descriptive alt text matching or improving the current site's pattern (e.g., "Porta Pivotante", "Janela Bay Window de Madeira", "Batentes de Madeira").

**Rationale:** Reitz has the best image accessibility in the entire benchmark — all 20 images have proper alt text. This is a competitive advantage that must be preserved in the rebuild. The SEO spec will define standards to maintain this.

### Decision: Quote form emphasizes custom sizing capability

The quote form will prominently feature "padrao ou sob medida" (standard or custom size) as a key field, reflecting Reitz's manufacturing capability for custom esquadrias.

**Rationale:** The meta description says "tamanhos padrao ou sob medida" — custom sizing is a core differentiator for a manufacturer vs. a retailer. The form should capture this intent directly.

## Risks / Trade-offs

- **SSL fix requires hosting action** -> The prototype assumes HTTPS works. Production launch is blocked until the hosting provider installs a valid certificate (Let's Encrypt recommended). The current cert belongs to uni5.net (the hosting platform).
- **PHP/TAGX dependency** -> The current CMS is proprietary (TAGX). If the business wants CMS capabilities post-prototype, they'll need migration to WordPress, a headless CMS, or similar.
- **Product photos exist but are hosted externally** -> Images are served from `solucao782.tagx.com.br` and `esquadriasreitz.com.br`. The prototype uses placeholder areas. Production needs these images downloaded and self-hosted.
- **Founded 1993 claim** -> Footer says "Fundada em 1993" — that makes 33 years in 2026. Use "Mais de 30 anos" unless the client confirms the exact year.
- **Google Analytics UA present but deprecated** -> The current site uses UA-153094183-1 (Universal Analytics, sunset July 2023). Production must migrate to GA4.
- **reCAPTCHA key may be stale** -> The contact form uses reCAPTCHA v2 with a specific site key. A new key will be needed for the new domain setup.

## Open Questions

- Is the WhatsApp number (48) 99983-1254 still active and preferred?
- Current business hours and days of operation.
- Does the business still accept the payment methods shown in the footer image (credit cards, boleto)?
- Is there a preference for the production CMS (WordPress, custom, static)?
- Exact scope of "Servicos" — does Reitz offer installation, maintenance, restoration?
- Are the product photos on the current site available in higher resolution?
