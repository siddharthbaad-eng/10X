# Performance (~200 tokens)

The page is ~4 KB with no images, fonts, or scripts, so it is already fast. Guard that as it grows.

## Images
- Use modern formats (WebP or AVIF) with a JPEG fallback via `<picture>` if needed.
- Always set `width` and `height` attributes to prevent layout shift (CLS).
- Add `loading="lazy"` to images below the first screen.
- Resize to display size; do not ship 4000px photos for 600px cards.

## Fonts
- The page uses system Arial (zero download). If you add a web font, load at most two weights and use `font-display: swap`.

## Scripts
- None today. If added, use `defer` and keep them small.

## Measure
Google's Core Web Vitals (LCP, INP, CLS) are the common benchmark: https://web.dev/articles/vitals. Check with Lighthouse in Chrome DevTools.
