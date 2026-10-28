# 02. New sitemap and planned changes

This is the change list I agreed before touching anything live.

## New sitemap

| Page | URL | Built from | Reason |
|---|---|---|---|
| Home | `/` (unchanged) | Home (c1dmp) | The brief requires this URL to stay. It now leads with both offers at equal weight. |
| B2B Content Strategy and SEO | `/b2b-content-strategy-seo` | Services (r1ham), renamed | Landing page for buyer segment 1 (B2B SaaS and tech marketers). The slug matches search intent. |
| Executive and LinkedIn Thought Leadership | `/executive-linkedin-thought-leadership` | New page (duplicate of the B2B page) | Landing page for buyer segment 2 (healthcare and biotech executives). |
| About | `/about` | About Us (pvy9e), renamed | Credibility page. Fixes the old `/services` slug that pointed at About content. |
| Contact (Book a Call) | `/contact` | Blog page at `/book-online` (dbr96), renamed | Merges booking and contact into one conversion page: the Bookings widget plus a short brief form. |
| Thank You | `/thank-you-page` | Thank You (ft3yc) | Form confirmation. Hidden from menus, noindex. |
| Free Courses | removed | ml1ix | No courses are offered, and the page dilutes the positioning. |
| Cart | removed | jv9vt | Nothing is for sale. |
| Blog | hidden, posts unpublished | Wix Blog | The template posts imply articles Siddharth didn't write. The app stays for future real articles. |

### Hierarchy

```
Home (/)
├── B2B Content Strategy and SEO (/b2b-content-strategy-seo)
├── Executive and LinkedIn Thought Leadership (/executive-linkedin-thought-leadership)
├── About (/about)
└── Contact / Book a Call (/contact)
    └── Thank You (/thank-you-page, hidden)
```

## Navigation

- **Header:** logo text "Siddharth Baad" (links to `/`), then B2B Content and SEO · Executive Thought Leadership · About · **[Book a Call]** button (links to `/contact`). The two service links come first, side by side, with the same style, giving equal weight.
- **Mobile:** hamburger menu with the same items. Keep the Book a Call button visible in the mobile header.
- **Footer:** the same four links, a LinkedIn link, the self-reported figures note, and © 2026 Siddharth Baad.

## Redirects (301)

Created through the Wix SEO Redirects API after the slugs change.

| From | To | Why |
|---|---|---|
| `/services` | `/about` | The old URL held About content |
| `/blog` | `/b2b-content-strategy-seo` | The old URL held Services content |
| `/book-online` | `/contact` | The old booking URL |
| `/challenges` | `/` | Page removed |
| `/cart-page` | `/` | Page removed |
| `/post/maximize-roi-with-strategic-content-marketing-solutions` | `/` | Post unpublished. **Live since 2026-10-28.** |
| `/post/transform-your-business-with-purpose-driven-content-strategies` | `/` | Post unpublished. **Live since 2026-10-28.** |
| `/post/how-quality-content-drives-customer-engagement-and-growth` | `/` | Post unpublished. **Live since 2026-10-28.** |
| Writing Workshop and Content Review Session service pages | `/contact` | Services hidden. Path checked after publish. |
| Old service page slug `content-strategy-consultation` | the new `free-30-minute-discovery-call` service page | Service renamed. Path checked after publish. |

## Visual identity

| Token | Value | Use |
|---|---|---|
| Ink navy | `#14213D` | Headings, body text, header and footer background |
| Off-white | `#F7F5F0` | Page background |
| White | `#FFFFFF` | Cards, alternating sections |
| Teal | `#0F766E` | Links, icons, eyebrow text, accents |
| Burnt amber | `#B45309` | Primary CTA buttons only (white bold text, 16px or larger) |
| Slate | `#475569` | Secondary text, notes |

- **Headings:** DM Serif Display. **Body and buttons:** Wix Madefor Text. Both are in the Wix font library, so nothing gets uploaded.
- **Type scale (desktop / mobile):** H1 48/32, H2 32/24, H3 22/20, body 18/16, notes 14/13.
- **Layout:** wide margins, generous spacing, a maximum text width of about 720px, two equal service cards on desktop that stack on mobile, and rounded 8px buttons.
- **Imagery:** one professional headshot of Siddharth (About and Home hero) plus simple line icons. No stock "team" photos and no client logos.

## API changes (done by Claude)

1. Bookings: rename "Content Strategy Consultation" to "Free 30-Minute Discovery Call", make it free, set it to 30 minutes, and hide Writing Workshop and Content Review Session.
2. Blog: unpublish the 3 template posts.
3. Home SEO tags: new title, meta, and social tags, and replace the focus keyword.
4. After the editor work: SEO tags for every page, noindex on Thank You, and all redirects.

## Editor changes (done by the site owner)

See `03-editor-build-guide.md`.
