## Why

Madeireira Fontana scores 48.3/100 (Fraco) in the benchmark — mid-range but dragged down by the worst tech score in the study (3.3/10.5). The site runs WordPress 4.3.34 from 2015, with XML-RPC exposed (security risk), `lang="en-US"` on a Portuguese site, zero WhatsApp links, zero meta descriptions, and 100% of home images missing alt text. The contact page exists but has no visible form. Despite 30+ years in market, 17 wood species, testimonials with Schema.org/Review markup, and multiple payment options, the site fails to convert visitors.

Critical problems:

- **WordPress 4.3.34 (2015)** — severely outdated, XML-RPC enabled, security vulnerability
- **Zero WhatsApp** in the entire site — the most critical contact channel in the lumber industry is absent
- **Zero meta description** on any page — SEO penalty across all pages
- **Home page: 8/8 images without alt text** (100%) — worst accessibility on home
- **No H1 on home page** + `lang="en-US"` incorrect for pt-BR content
- **Contact page has no working form** — only a footer form exists, buried and easy to miss
- **17 wood species listed but no individual pages, no prices, no technical sheets**
- **Zero social media links** anywhere on the site

The business has strong assets worth preserving: founded 1985 (41 years), 4,000m2 facility with 5 warehouses, 17+ wood species with descriptions, quality certificate from Sao Jose (2015), customer testimonials, gallery with 65+ photos, and multiple payment options including Construcard and Losango 24x.

## What Changes

- Replace the WordPress 4.3 site with a modern, mobile-first responsive static site.
- Add a hero section with positioning, tagline ("Qualidade, variedade e estoque"), and primary CTAs (WhatsApp + quote form) in the first viewport.
- Rebuild the product catalog for 17 wood species with descriptions, applications, and photo areas — each species gets a card with a quote CTA.
- Add a prominent quote request form with product context, replacing the buried footer-only form.
- Add sticky WhatsApp button with contextual prefilled messages on every page.
- Fix all SEO: add meta descriptions, correct `lang="pt-BR"`, add H1 to home, fix all image alt text, add JSON-LD LocalBusiness.
- Preserve existing content: company history, testimonials, gallery photos, payment options.
- Add click-to-call on all phone numbers and mailto on email addresses.
- Keep e-commerce checkout, online payment, and customer accounts out of scope.

## Capabilities

### New Capabilities

- `modern-responsive-site`: Defines the responsive layout, mobile-first design, navigation, hero section, product showcase, footer, and overall site structure replacing the outdated WordPress theme.
- `seo-and-discoverability`: Defines semantic HTML, metadata, structured data, headings hierarchy, image alt text, lang attribute fix, and crawlability requirements to fix the 3.3/10.5 tech score and 8.0/19.5 SEO score.
- `conversion-and-lead-capture`: Defines quote forms, CTAs, WhatsApp integration, click-to-call, and lead capture flows to fix the 11.0/25 conversion score and add the missing WhatsApp channel.

### Modified Capabilities

- None.

## Impact

- Replaces the entire WordPress site — the WP 4.3 installation is too outdated and insecure to patch.
- Requires organizing the existing 65+ gallery photos by wood species for the product catalog.
- Requires confirmation of business hours and whether the phone (48) 3258-1500 accepts WhatsApp or if a separate number is needed.
- Does not require checkout, payment processing, inventory systems, or customer login.
- Expected score improvement: 48.3 -> 70+/100, with largest gains in Tech (+5), Conversion (+10), and SEO (+8).
