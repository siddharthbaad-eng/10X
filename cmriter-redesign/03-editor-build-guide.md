# 03. Editor build guide

Follow this guide in the Wix editor for cmriter.com. Claude handles SEO tags, redirects, Bookings, and the blog through the API, so skip those here. Everything below needs the editor because Wix has no API for layout, text, or menus.

Editor link: https://editor.wix.com/edit/od/01143bef-8e26-4237-a6ad-909b3d5b4128?metaSiteId=04ad84b8-c68d-421d-b3fd-92193cef490f

Estimated time: 3 to 4 hours.

## Rules for every page

- **One H1 per page.** For each text element, set the HTML tag in the text element's SEO or accessibility settings. The tag shown in brackets below, such as `[H1]`, `[H2]`, `[H3]` or `[P]`, is the tag to set. A text theme that only looks like a heading isn't enough.
- **Copy:** paste it exactly as written. It has been checked for no em-dashes, no formal transitions, no hedge words, and no banned buzzwords. If you edit it, keep to those rules.
- **Figures:** every block of figures keeps the self-reported note directly under it.
- **Buttons:** primary buttons are amber `#B45309` with white bold text. Secondary links are teal `#0F766E`.
- **Images:** give every image alt text. A suggestion is listed with each image.

---

## C0. Confirm the current pages (5 minutes, do this first)

Open **Pages and Menu**. For each page, note its name and its URL slug (Page settings, SEO basics, or URL). Compare with this table from the API audit:

| Page name | Slug the API reports |
|---|---|
| Home | `/` |
| About Us | `services` |
| Services | `blog` |
| Blog | `book-online` |
| Free Courses | `challenges` |
| Cart Page | `cart-page` |
| Thank You Page | `thank-you-page` |

Tell Claude about any mismatch before you rename slugs, because the redirect map depends on these.

---

## C1. Theme and site styles

Open **Site Design** (Theme). Set:

**Colors**

| Role | Hex |
|---|---|
| Background | `#F7F5F0` |
| Secondary background (cards, alternating sections) | `#FFFFFF` |
| Main text and headings | `#14213D` |
| Secondary text | `#475569` |
| Links and accent | `#0F766E` |
| Primary button | `#B45309`, text `#FFFFFF` |

**Text themes**

| Theme | Font | Desktop / mobile size | Weight |
|---|---|---|---|
| Heading 1 | DM Serif Display | 48 / 32 px | Regular |
| Heading 2 | DM Serif Display | 32 / 24 px | Regular |
| Heading 3 | Wix Madefor Text | 22 / 20 px | Semibold |
| Paragraph 1 (body) | Wix Madefor Text | 18 / 16 px | Regular, line height 1.6 |
| Paragraph 2 (eyebrow, notes) | Wix Madefor Text | 14 / 13 px | Medium. Eyebrows in teal and uppercase, notes in slate. |

**Buttons:** 8px corner radius, about 14px by 28px padding, Wix Madefor Text 16px Semibold.

**Spacing:** keep section padding at about 96px top and bottom on desktop and 56px on mobile. Keep text blocks no wider than about 720px.

---

## C2. Pages: rename, add, delete

In **Pages and Menu**:

1. **Services** page: rename to `B2B Content Strategy and SEO`. Set the slug to `b2b-content-strategy-seo`.
2. Duplicate that page. Rename the copy to `Executive and LinkedIn Thought Leadership` and set its slug to `executive-linkedin-thought-leadership`.
3. **About Us** page: rename to `About`. Set the slug to `about`.
4. **Blog** page (slug `book-online`): rename to `Contact`. Set the slug to `contact`. If this page turns out to be the blog feed rather than the booking page, add a new blank page called `Contact` with slug `contact` instead, and hide the blog page from the menu.
5. Hide the **Blog** feed page from the menu. Don't delete the Blog app, so Siddharth can publish real articles later.
6. Delete **Free Courses** and **Cart Page**.
7. Remove the apps that owned them: **Wix Online Programs**, **Wix Stores**, and **Wix Hotels** (Apps panel, Manage, Remove). Keep Bookings, Forms, Blog, Members Area, and Invoices.
8. **Thank You Page**: rename to `Thank You`, keep the slug `thank-you-page`, and hide it from the menu.

---

## C3. Header and menu

**Desktop header** (sticky, background `#F7F5F0`, a thin bottom border in `#14213D` at 10% opacity):

- Left: text logo `Siddharth Baad` (DM Serif Display, 24px, navy), linked to Home. Tag `[P]`, not a heading.
- Menu, in this order: `B2B Content and SEO` (links to the B2B page) · `Executive Thought Leadership` (links to the Exec page) · `About`.
- Right: button `Book a Call`, linked to the Contact page.

Both service menu items use the same style. Don't highlight one over the other.

**Mobile header:** text logo on the left, a small `Book a Call` button, and the hamburger menu with the same three items plus `Book a Call`.

---

## C4. Footer

Background `#14213D`, text `#F7F5F0`.

- `[P]` `Siddharth Baad`
- `[P]` `Content strategy and SEO for B2B teams. LinkedIn thought leadership for healthcare and biotech leaders.`
- Links: B2B Content and SEO · Executive Thought Leadership · About · Book a Call · LinkedIn (https://www.linkedin.com/in/chintujagadish, opens in a new tab)
- `[P]` (14px) `Figures on this site are self-reported in Siddharth's professional profile and have not been independently verified.`
- `[P]` (14px) `© 2026 Siddharth Baad`

---

## C5. Home page (`/`)

Delete all existing template sections, then build these in order.

### Section 1: Hero (background `#F7F5F0`)

Desktop: two columns, text 60% and photo 40%. Mobile: text first, photo below.

- `[P]` eyebrow: `CONTENT MARKETING AND COMMUNICATIONS STRATEGIST`
- `[H1]` `Content strategy for B2B growth. Thought leadership for senior leaders.`
- `[P]` `I'm Siddharth Baad. For 21+ years I've led content marketing and communications across pharmaceuticals, CROs, biotech, technology, and education. I help B2B teams build content that brings in qualified buyers, and I help executives build a voice their industry listens to.`
- Button (primary): `Book a free call`, linked to Contact
- Text link (teal): `See how I can help`, anchored to Section 2
- Image: a professional headshot of Siddharth. Alt text: `Siddharth Baad, content marketing and communications strategist`

### Section 2: Two services (background `#FFFFFF`, anchor name "services")

- `[H2]` `Two ways I can help`
- Two cards side by side on desktop, stacked on mobile. Give them the same width, height, and style.

**Card A**
- `[H3]` `Content strategy and SEO for B2B teams`
- `[P]` `For B2B SaaS and technology marketers who need content that ranks, earns trust, and feeds the pipeline. I build the strategy, the SEO plan, and the workflows that keep it running.`
- `[P]` bullet list:
  - `Content strategy and editorial calendars`
  - `SEO and conversion rate optimization`
  - `Demand generation and HubSpot nurture workflows`
  - `Reporting tied to qualified leads`
- Button (secondary, teal outline): `Explore B2B content and SEO`, linked to the B2B page

**Card B**
- `[H3]` `Executive and LinkedIn thought leadership`
- `[P]` `For healthcare and biotech leaders who want a clear, consistent voice on LinkedIn and in the media. I build the framework, write the content, and keep it on schedule.`
- `[P]` bullet list:
  - `LinkedIn strategy built on content pillars`
  - `Posts and executive bylines in your voice`
  - `Media relations and investor communications`
  - `Regulatory briefs for leadership teams`
- Button (secondary, teal outline): `Explore executive thought leadership`, linked to the Exec page

### Section 3: Proof (background `#F7F5F0`)

- `[H2]` `Proof from the work`
- Three blocks in a row on desktop, stacked on mobile:
  - `[H3]` `A 96-post CEO LinkedIn campaign`
    `[P]` `For the Group CEO of a CRO with four business units, I conceived and ran a 12-month LinkedIn thought-leadership campaign of 96 posts, built on a 10-pillar content framework.`
  - `[H3]` `Monthly regulatory briefs for the C-suite`
    `[P]` `At the same CRO, I built a regulatory intelligence function from scratch: monthly CDSCO, EMA, and USFDA briefs with strategic impact analysis for each business unit.`
  - `[H3]` `Full-funnel B2B marketing today`
    `[P]` `As Digital Marketing Lead at InoRx, a CRO serving India and the US, I run B2B demand generation, LinkedIn thought leadership for the CEO and CMO, HubSpot CRM and nurture workflows, SEO, and performance reporting.`

### Section 4: Reported results (background `#14213D`, light text)

- `[H2]` `Reported results`
- Four stat tiles. The big number is `[P]` styled at 40px DM Serif Display, and the label is `[P]`. Don't tag the numbers as headings.
  - `30+` / `publications covering a CRO's leadership and news`
  - `40%` / `increase in positive media sentiment at the same CRO`
  - `30%` / `increase in qualified leads at SANVI IT`
  - `30%` / `improvement in organic search rankings from SEO-driven content`
- `[P]` (14px) `Figures are self-reported in Siddharth's professional profile and have not been independently verified.`

### Section 5: Experience (background `#FFFFFF`)

- `[H2]` `Where I've worked`
- `[P]` `Digital Marketing Lead at InoRx. Senior Manager, Corporate Communications and Marketing at a CRO. Senior Marketing Manager at SANVI IT. Communications and marketing roles at Ahmedabad University, Biocon, Heubach Colour, Anil, Intas, and Torrent. Reporting at Indian Express and The Asian Age.`
- Show the names as text only. No company logos.

### Section 6: Closing CTA (background `#F7F5F0`, centered)

- `[H2]` `Have a project in mind?`
- `[P]` `Book a free 30-minute call. We'll talk through your goals and whether I'm the right fit. If I'm not, I'll say so.`
- Button (primary): `Book a free call`, linked to Contact

---

## C6. B2B Content Strategy and SEO page (`/b2b-content-strategy-seo`)

### Hero
- `[P]` eyebrow: `FOR B2B SAAS AND TECHNOLOGY MARKETERS`
- `[H1]` `B2B content strategy and SEO that supports pipeline`
- `[P]` `A lot of B2B content gets published and forgotten. I build content programs that rank, answer real buyer questions, and move qualified leads toward sales.`
- Button (primary): `Book a free call`, linked to Contact

### Who this is for
- `[H2]` `Who this is for`
- `[P]` bullets:
  - `Marketing leaders at B2B SaaS and technology companies`
  - `Teams producing content without a clear strategy behind it`
  - `Companies that need SEO, email, and CRM working together`
  - `Founders who need a senior content lead without a full-time hire`

### What I do (two-column grid on desktop)
- `[H2]` `What I do`
- `[H3]` `Content strategy` / `[P]` `Audience research, messaging, editorial calendars, and content for each stage of the buying journey.`
- `[H3]` `SEO and conversion rate optimization` / `[P]` `SEO audits, keyword strategy, SEO content assets, and conversion improvements on the pages that capture leads.`
- `[H3]` `Demand generation` / `[P]` `Integrated B2B campaigns across LinkedIn, email, and search that build awareness and bring in qualified leads.`
- `[H3]` `CRM and marketing automation` / `[P]` `HubSpot CRM setup, lead nurture workflows, and segmented email that supports sales and business development.`
- `[H3]` `Performance reporting` / `[P]` `Dashboards that track qualified leads, cost per lead, and funnel velocity, so you know what to keep and what to cut.`
- `[H3]` `AI-assisted content workflows` / `[P]` `Faster research, drafting, and repurposing, with human editing and fact-checking on everything that ships.`

### How we'd work together (numbered steps)
- `[H2]` `How we'd work together`
- `[H3]` `1. Discovery call` / `[P]` `A free 30-minute call about your goals, audience, and current content.`
- `[H3]` `2. Audit` / `[P]` `A review of your content, SEO, and funnel to find the biggest gaps.`
- `[H3]` `3. Plan` / `[P]` `A prioritized content and SEO plan with clear owners and metrics.`
- `[H3]` `4. Execution or advisory` / `[P]` `I run the plan with your team, or I guide your in-house writers.`

### Relevant experience
- `[H2]` `Relevant experience`
- `[P]` `At InoRx, I'm building the digital marketing function from the ground up for a CRO serving India and the US, with ownership of demand generation, HubSpot CRM and automation, SEO and CRO, and analytics. At SANVI IT, an IT services company, I led lead generation, SEO, email, and social media across digital platforms.`

### Reported results
- `[H2]` `Reported results`
- Stat tiles (`[P]` only):
  - `30%` / `improvement in organic search rankings from SEO-driven content`
  - `60+` / `SEO-optimized content assets across blogs, web copy, and multimedia`
  - `25%` / `uplift in email open rates from segmented nurture content`
  - `20%` / `increase in lead conversion from segmented nurture content`
  - `30%` / `increase in qualified leads at SANVI IT`
  - `80,000+` / `users added to audience reach at SANVI IT`
- `[P]` (14px) `Figures are self-reported in Siddharth's professional profile and have not been independently verified.`

### CTA
- `[H2]` `Let's look at your content together`
- `[P]` `Book a free 30-minute call and bring your biggest content or SEO question.`
- Button (primary): `Book a free call`, linked to Contact

---

## C7. Executive and LinkedIn Thought Leadership page (`/executive-linkedin-thought-leadership`)

Start from the duplicated B2B page and replace all of the copy.

### Hero
- `[P]` eyebrow: `FOR HEALTHCARE AND BIOTECH EXECUTIVES`
- `[H1]` `LinkedIn thought leadership for healthcare and biotech executives`
- `[P]` `Your expertise should be visible to the partners, investors, and talent who matter to your business. I turn what you know into a steady, credible presence on LinkedIn and in the media.`
- Button (primary): `Book a free call`, linked to Contact

### Who this is for
- `[H2]` `Who this is for`
- `[P]` bullets:
  - `CEOs and senior leaders at pharma, CRO, biotech, and healthcare companies`
  - `Leaders heading into fundraising, partnerships, or a market launch`
  - `Executives with strong ideas and no time to write`
  - `Communications teams who need a senior partner for executive content`

### What I do
- `[H2]` `What I do`
- `[H3]` `LinkedIn strategy and pillar frameworks` / `[P]` `A clear set of content pillars that reflect your expertise and your company's goals, so every post has a job to do.`
- `[H3]` `Posts, bylines, and content calendars` / `[P]` `Posts and executive bylines written in your voice, planned months ahead and reviewed with you.`
- `[H3]` `Media relations` / `[P]` `Press releases, spokesperson interactions, and positioning at conferences and symposiums.`
- `[H3]` `Investor and crisis communications` / `[P]` `AGM, IPO, and ESG communications, plus clear, fast content when an incident puts your reputation under pressure.`
- `[H3]` `Regulatory intelligence` / `[P]` `Monthly briefs on CDSCO, EMA, and USFDA developments, with analysis of what they mean for each part of your business.`

### Flagship example
- `[H2]` `Flagship example: a 96-post CEO LinkedIn campaign`
- `[P]` `For the Group CEO of a CRO, I conceived and ran a 12-month LinkedIn thought-leadership campaign of 96 posts, built on a 10-pillar content framework. In the same role I led content strategy and executive communications across four business units: Clinical Trials, Biopharma Services, Healthy Volunteer Services, and Preclinical Testing. I also built the company's monthly regulatory briefs for the C-suite.`
- `[P]` (14px, slate) `The company and the executive are not named here.`

### Reported results
- `[H2]` `Reported results from the CRO role`
- Stat tiles (`[P]` only):
  - `30%` / `increase in audience engagement`
  - `30+` / `regional and international publications covering the company`
  - `40%` / `increase in positive media sentiment`
  - `25%` / `increase in partnership inquiries`
  - `20%` / `increase in investor engagement`
- `[P]` (14px) `Figures are self-reported in Siddharth's professional profile and have not been independently verified.`

### CTA
- `[H2]` `Plan the next 12 months of your voice`
- `[P]` `Book a free 30-minute call. We'll talk about your goals, your audience, and what a realistic posting plan looks like.`
- Button (primary): `Book a free call`, linked to Contact

---

## C8. About page (`/about`)

### Intro (two columns: photo and text)
- `[H1]` `About Siddharth Baad`
- `[P]` `I'm a content marketing and communications strategist with 21+ years of experience across pharmaceuticals, CROs, biotechnology, technology, and education. I'm based in Trenton, New Jersey, and most of my work is with teams in India.`
- Image: headshot. Alt text: `Portrait of Siddharth Baad`

### Career
- `[H2]` `How I got here`
- `[P]` `I started as a reporter at The Asian Age and Indian Express. Journalism taught me to find the story, respect the reader, and write it clearly.`
- `[P]` `I moved into corporate communications at Torrent, Intas, Anil, Heubach Colour, and Biocon, then led communications at Ahmedabad University. At SANVI IT I ran digital marketing and lead generation. For five years I led corporate communications and marketing at a CRO, supporting the Group CEO across four business units.`
- `[P]` `Today I'm Digital Marketing Lead at InoRx, a CRO serving India and the US.`

### Capabilities
- `[H2]` `What I bring`
- `[P]` bullets:
  - `Content strategy and SEO`
  - `B2B digital marketing and demand generation`
  - `CRM and marketing automation in HubSpot`
  - `Executive communications and LinkedIn thought leadership`
  - `Investor relations and crisis communications`
  - `Regulatory intelligence for CDSCO, EMA, and USFDA`
  - `AI-assisted content workflows`

### Education
- `[H2]` `Education`
- `[P]` bullets:
  - `Master of Communication Studies, The Maharaja Sayajirao University of Baroda`
  - `Postgraduate degree in Digital Marketing and Social Media, MICA`
  - `B.Sc. in Statistics, The Maharaja Sayajirao University of Baroda`

### CTA
- `[H2]` `Let's talk about your project`
- `[P]` `Book a free 30-minute call about B2B content, SEO, or executive thought leadership.`
- Button (primary): `Book a free call`, linked to Contact

---

## C9. Contact page (`/contact`)

### Booking
- `[H1]` `Book a free discovery call`
- `[P]` `Pick a time that works for you. It's a free 30-minute Microsoft Teams call about your content, SEO, or executive thought leadership goals.`
- Add the **Wix Bookings** service widget (Add, Bookings, Service list or Book button), set to show only `Free 30-Minute Discovery Call`. If this page was the old Bookings page, keep its widget and make sure the two hidden services no longer show.

### Brief form
- `[H2]` `Prefer to send a brief?`
- `[P]` `Tell me about your project and I'll reply by email.`
- **Wix Forms** form with these fields:
  - Name (required)
  - Work email (required)
  - Company
  - Which service? (dropdown: `B2B content strategy and SEO`, `Executive and LinkedIn thought leadership`, `Not sure yet`)
  - Message (required)
- Submit button: `Send my brief`. After submit, go to the Thank You page.
- `[P]` (14px, slate) `Based in Trenton, New Jersey. Or email siddharth_baad@hotmail.com.`

---

## C10. Thank You page (`/thank-you-page`)

- `[H1]` `Thanks, your brief is in.`
- `[P]` `I'll reply by email. If you'd like to talk sooner, book a free 30-minute call.`
- Button (primary): `Book a free call`, linked to Contact

---

## C11. Dashboard settings

**Business name.** Go to Settings, Business info, and change the business name from `Content Marketing` to `Siddharth Baad`. This name appears in the default title tags and in `og:site_name` when links are shared. Claude couldn't make this change through the API in this session.

**Bookings.** Claude already updated the service through the API on 2026-10-28. "Content Strategy Consultation" (previously ₹150, paid online, 60 minutes) is now **Free 30-Minute Discovery Call**: free, 30 minutes, online booking on. Writing Workshop and Content Review Session are hidden. In the dashboard:

1. **Bookings, Settings, Video conferencing account:** choose **Custom link**. Paste a recurring Microsoft Teams meeting link: in Teams or Outlook, create a recurring meeting with no end date and copy its join link. Wix has no automatic Teams integration, so every booking gets this one link. If Wix asks for a plan upgrade, video conferencing needs a Business-tier plan.
2. Open the **Free 30-Minute Discovery Call** service. Under Locations, turn on Video conferencing.
3. **Availability:** set the hours you take calls. The site timezone is Asia/Kolkata. If you mainly take US calls, change the timezone in the Bookings settings.
4. **Notifications:** confirm that booking emails go to your preferred inbox.

---

## C12. Mobile pass and publish

1. Open the mobile view. On every page, check: there's one column, nothing overflows sideways, buttons are at least 44px tall, the text is 16px or larger, and the header's Book a Call button is visible.
2. Hide any decorative elements that crowd the mobile layout.
3. Preview the whole site, then **Publish**.
4. Tell Claude it's published, so Claude can finish the SEO tags and redirects.
