## Why

Reitz Esquadrias e Madeiras scores 38.7/100 in the benchmark — in the "Critico" tier. The site was built with a custom PHP CMS by TAGX using a modified "Nevada" theme with conditional comments for IE8/IE9. Two critical infrastructure failures make the site effectively broken:

- **CRITICAL: SSL certificate belongs to uni5.net** — hostname mismatch causes browsers to block the site with security warnings. Visitors see a certificate error before any content loads.
- **CRITICAL: Server returns incomplete HTML** — PHP includes fail, sending only ~1023 bytes to crawlers, resulting in zero indexable content for search engines.
- **Zero forms on the crawled page** — all conversion depends on WhatsApp links and a phone number
- **`lang="en-US"` on a 100% Portuguese site** — hurts SEO language targeting
- **Scripts reference discontinued HTTP URLs** — html5shiv and css3-mediaqueries from Google Code (shut down 2016)
- **Zero analytics, zero social media links** — no tracking, no social proof
- **Zero schema.org markup** — no structured data for local business or products

Despite these problems, the business has strong content worth preserving: specialized niche in esquadrias (doors, windows, frames), own manufacturing since 1993 (33+ years), excellent alt text on ALL 20 product images (best in the benchmark), detailed product categories (portas, janelas, batentes, guarnicoes, fechaduras), WhatsApp integration with 5 links, and a clear service address in Barreiros, Sao Jose.

## What Changes

- Fix the SSL crisis — the prototype assumes a valid certificate (Let's Encrypt or equivalent).
- Replace the broken PHP/TAGX site with a modern, mobile-first responsive site.
- Build a hero section showcasing the esquadrias specialization with CTAs in the first viewport.
- Build a product showcase organized by category: Portas, Janelas, Rodapes/Batentes/Guarnicoes, Fechaduras/Dobradicas/Puxadores.
- Add a quote request form for custom esquadrias (currently zero forms).
- Add semantic HTML: proper H1, H2, H3 hierarchy (currently H1 is misused on every product title).
- Fix `lang="pt-BR"` on the html element.
- Add JSON-LD LocalBusiness and Product structured data.
- Preserve and enhance the existing excellent alt text practice on all product images.
- Add a sticky WhatsApp button with contextual prefilled messages per product category.
- Keep the existing contact info (phone, WhatsApp, email, address) visible in header/footer.
- Keep e-commerce checkout, payment processing, and customer accounts out of scope.

## Capabilities

### New Capabilities

- `modern-responsive-site`: Defines the responsive layout, mobile-first design, navigation, hero section, esquadrias product showcase, footer, and overall site structure replacing the broken PHP/TAGX site.
- `seo-and-discoverability`: Defines semantic HTML, metadata, structured data, heading hierarchy, lang tag fix, image alt text preservation, and crawlability requirements.
- `conversion-and-lead-capture`: Defines quote forms for custom esquadrias, CTAs, WhatsApp integration with product context, phone click-to-call, and lead capture flows.

### Modified Capabilities

- None.

## Impact

- Replaces the entire existing site — the PHP/TAGX codebase cannot be incrementally fixed.
- SSL must be resolved at the hosting level before the new site can function (the current cert belongs to uni5.net).
- Requires confirmation that the WhatsApp number (48) 99983-1254 is still active.
- Product photos already exist on the live site (20 images with alt text) — the prototype uses placeholder areas matching these.
- Does not require checkout, payment, inventory, or customer login.
- Expected score improvement: 38.7 -> 70+/100, with gains across all 6 benchmark pillars.
