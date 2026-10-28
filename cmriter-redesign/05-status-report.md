# 05. Status report

Status as of 2026-10-28: Phases A (documents) and B (API changes) are done. Phase C (editor build) is with the site owner. Phase D (SEO tags for the remaining pages and the rest of the redirects) runs after the editor work is published.

## 1. Sitemap changes and reasons

| Change | Reason |
|---|---|
| Home stays at `/`, rebuilt | The brief requires the homepage URL to stay. It now leads with both offers at equal weight. |
| Services (`/blog`) becomes B2B Content Strategy and SEO (`/b2b-content-strategy-seo`) | A dedicated page for buyer segment 1. Fixes a slug that pointed at the wrong content. |
| New page: Executive and LinkedIn Thought Leadership (`/executive-linkedin-thought-leadership`) | A dedicated page for buyer segment 2, as a peer of the B2B page |
| About Us (`/services`) becomes About (`/about`) | Keeps the credibility page. Fixes the crossed slug. |
| Booking page (`/book-online`) becomes Contact (`/contact`) | Merges booking and contact into one conversion page |
| Free Courses (`/challenges`) removed | No courses are offered, and the page dilutes the positioning |
| Cart (`/cart-page`) removed | Nothing is for sale |
| Blog hidden, 3 template posts unpublished | Template posts implied articles Siddharth didn't write |
| Thank You kept, hidden, noindex | Needed for the brief form |

Full details: `02-sitemap-and-changes.md`.

## 2. Claims: sourced vs flagged

All figures on the site trace to `Profile (1).pdf` and carry the self-reported note. The table of sourced claims and flagged items is in `04-claims-register.md`. In summary:

- **Sourced and used:** 13 figures. Five from the CRO role, shown as "at a CRO", not named. Five career-wide figures from the profile summary, with no employer named because the profile gives none. Three from SANVI IT.
- **Flagged and adjusted:** "Veeda" next to figures and "global CRO". The profile doesn't call Veeda global, and the brief asks for the role to stay unnamed.
- **Sourced but left off:** 15% growth in new business engagements, and a 15% increase in quarterly sales revenue at SANVI IT. They're not in the brief's list. Can be added on request.
- **Removed:** the template blog posts, the template services, and the old homepage claim of "measurable growth".

## 3. Booking tool

**Wix Bookings**, with a **free 30-minute discovery call** held over **Microsoft Teams**.

Why: Bookings was already installed, it's native to the site (no added integration, no Velo), it puts the booking widget directly on `/contact`, and bookings land in the same dashboard as form leads. Teams has no native Wix integration, so the call uses a fixed custom Teams link that the owner adds in the Bookings settings (guide step C11).

Done through the API:
- "Content Strategy Consultation" (₹150, paid online, 60 minutes) became "Free 30-Minute Discovery Call" (no fee, 30 minutes, online booking on). The service slug is now `free-30-minute-discovery-call`.
- Writing Workshop and Content Review Session are hidden.

## 4. Existing site or new site

The account holds one **existing, published Premium site** ("Content Marketing", custom domain www.cmriter.com, editor type `ODEDITOR`, Velo disabled). No new site was created. The redesign happens in place, so the domain, the homepage URL, and the existing apps and data are kept.

## 5. Actions not completed, and why

| Action | Status | Why |
|---|---|---|
| Layout, theme, page copy, header and footer, menus | Owner, guide C1 to C10 | Wix has no API for editing editor-site pages. Wix also forbids custom Velo code here. |
| Create, rename, and delete pages and change slugs. Remove the Stores, Hotels, and Online Programs apps. | Owner, guide C2 | Editor-only actions |
| Business name "Content Marketing" to "Siddharth Baad" | Owner, guide C11 | The site-properties API call wasn't approved in this session |
| Teams link, availability hours, Bookings notifications | Owner, guide C11 | Dashboard-only. Teams has no native integration. |
| SEO tags for the B2B, Exec, About, Contact, and Thank You pages | Claude, Phase D | Page IDs and slugs change during the editor work. The Exec page doesn't exist yet. |
| Redirects for `/services`, `/blog`, `/book-online`, `/challenges`, `/cart-page`, and the service pages | Claude, Phase D | A redirect overrides a live page, so these wait until the old slugs stop serving pages |
| Live-page check of headings and 301s | Blocked | This cloud session's network policy blocks www.cmriter.com. Allowlist it in the environment's network settings, or check in a browser. |
| Read the current on-page copy | Blocked | Same network restriction. The audit used Wix APIs instead. |

## Changes made on the live site

| When | What | Result |
|---|---|---|
| 2026-10-28 | Bookings: updated and hid services | 3 of 3 succeeded |
| 2026-10-28 | Blog: reverted 3 posts to draft | 3 of 3 `UNPUBLISHED`, 0 published posts remain |
| 2026-10-28 | Home SEO tags (draft and published): new title, description, `og:description`, `twitter:description`, focus keyword "B2B content strategy consultant" | Live, source `TAG_SOURCE_HOST_PAGE` |
| 2026-10-28 | 3 redirects, `/post/...` to `/` | 3 of 3 created |
