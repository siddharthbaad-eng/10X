# 01. Site audit: www.cmriter.com (baseline)

Audit date: 2026-10-28. Method: read-only Wix API calls (site context, Editor URLs, Item SEO Tags, Site SEO Tags, Redirects, Blog, Bookings Services). The live domain was blocked by the cloud session's network policy (proxy 403), so on-page headings and body copy could not be captured. Step C0 of the build guide covers that gap.

## Site

| Item | Value |
|---|---|
| Wix site name | Content Marketing |
| Site ID | `04ad84b8-c68d-421d-b3fd-92193cef490f` |
| Domain | https://www.cmriter.com (custom domain) |
| Status | Published, Premium plan |
| Editor type | `ODEDITOR` (editor URL `editor.wix.com/edit/od/...`). Not Wix Studio. |
| Velo (custom code) | Disabled |
| Created | Sep 28, 2026 (AI-generated template content) |
| Region | Language en, locale IN, timezone Asia/Kolkata, currency INR |
| Installed apps | Promote SEO, Wix Blog, Wix Bookings, Wix Forms, Wix Hotels, Wix Invoices (V2), Wix Members Area, Wix Online Programs, Wix Stores (V3) |
| Existing redirects | None |
| Site-wide SEO tags | Empty `description`, `keywords`, `fb_admins_meta_tag` |

**Verdict:** an existing site, so no new site is needed. The redesign happens on this site, keeping the domain and homepage URL.

## Static pages

Page names come from the default SEO title pattern (`{page name} | Content Marketing`). URLs come from each page's canonical tag. Several pairings look crossed, for example "About Us" at `/services`. Confirm in the editor's Pages panel (build guide step C0) before redirects are created.

| Page ID | Page name | URL | Title tag | Meta description | Focus keyword | Verdict |
|---|---|---|---|---|---|---|
| c1dmp | Home | `/` | Marketing Content Marketing for Growth \| Content Marketing Online | "Content Marketing offers marketing content marketing to turn your messaging into measurable growth, with strategic support available online." | marketing content marketing | Keep URL, rebuild |
| pvy9e | About Us | `/services` | About Us \| Content Marketing (default) | none | none | Becomes About at `/about` |
| r1ham | Services | `/blog` | Services \| Content Marketing (default) | none | none | Becomes the B2B service page |
| dbr96 | Blog | `/book-online` | Blog \| Content Marketing (default) | none | none | Becomes Contact / Book a Call |
| ml1ix | Free Courses | `/challenges` | Free Courses \| Content Marketing (default) | none | none | Remove |
| jv9vt | Cart Page | `/cart-page` | Cart Page \| Content Marketing (default) | none | none | Remove |
| ft3yc | Thank You Page | `/thank-you-page` | Thank You Page \| Content Marketing (default) | none | none | Keep, noindex |

Home also carries custom `og:description` and `twitter:description`: "Discover expert marketing content marketing strategies tailored for your business. Elevate your brand with our content marketing expertise today!"

### SEO problems found

1. Home title and meta are keyword-stuffed ("marketing content marketing") and never name Siddharth or the services.
2. Every other page uses the default pattern with the generic brand "Content Marketing" and has no meta description.
3. Page names and slugs don't match (About at `/services`, Services at `/blog`, Blog at `/book-online`), which confuses visitors and search engines.
4. Cart and Free Courses pages are indexable but serve no purpose for a consulting site.

## Blog (Wix Blog)

Published (all created within one minute on Sep 28, 2026, i.e. template filler):

| Title | URL |
|---|---|
| Maximize ROI with Strategic Content Marketing Solutions | `/post/maximize-roi-with-strategic-content-marketing-solutions` |
| Transform Your Business with Purpose-Driven Content Strategies | `/post/transform-your-business-with-purpose-driven-content-strategies` |
| How Quality Content Drives Customer Engagement and Growth | `/post/how-quality-content-drives-customer-engagement-and-growth` |

Unpublished drafts (6): "Optimizing Marketing Content Marketing Strategies...", "Crafting Effective Engaging Marketing Content Creation", "Marketing with Effective Content...", "The True Definition of Strategic Content Marketing...", "Key Content Foundations for Marketing Success", "Understanding the Core Content Strategy Elements".

## Bookings services

| Service | Type | ID | Slug |
|---|---|---|---|
| Writing Workshop | Class | `15955307-cdd0-4c21-8861-2134a4081415` | writing-workshop |
| Content Review Session | Appointment | `160d67c5-4880-4f74-b5ae-6ee263b87edb` | content-review-session |
| Content Strategy Consultation | Appointment | `1b6858a5-1e6e-4f11-887c-b421a9ef485d` | content-strategy-consultation |

## Source file

`Profile (1).pdf` (LinkedIn profile export, 7 pages) was uploaded during the session and checked line by line. Every claim on the new site traces to a page in it (see `04-claims-register.md`).
