# Deployment (~300 tokens)

Any static host works because there is no build step. Choose based on your needs, not the list order.

## Options
| Host | Fits when | Notes |
|------|-----------|-------|
| GitHub Pages | Code already lives on GitHub | Enable in repo Settings → Pages; serves from a branch |
| Netlify / Cloudflare Pages / Vercel | You want preview deploys per branch or PR | Connect the repo; build command empty, publish dir `/` |
| Any web server | You already run one | Copy the HTML files to the web root |

## Pre-Deploy Checklist
- [ ] Add an `index.html` (or rename the main page) so the site root does not 404.
- [ ] Fill or remove the empty `firstfile.html`.
- [ ] Validation passes.
- [ ] File names are lowercase and match their links exactly (hosts are case-sensitive).

## After Deploy
- Open the live URL on a phone.
- Add a `<meta name="description">` and Open Graph tags if you plan to share links on social platforms.
