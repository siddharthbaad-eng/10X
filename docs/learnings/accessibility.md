# Accessibility (~350 tokens)

Target: WCAG 2.2 Level AA (W3C Recommendation, October 2023) — https://www.w3.org/TR/WCAG22/

## Checklist
- **Language:** keep `lang="en"` on `<html>`.
- **Headings:** one `h1`, sequential `h2`s; no skipped levels.
- **Images:** every `<img>` needs `alt`. Describe the content ("Taj Mahal at sunrise, seen across the reflecting pool"); use `alt=""` only for decorative images.
- **Contrast:** normal text needs ≥ 4.5:1 against its background; large text ≥ 3:1. Current values: body `#333` on `#fafafa` = 12.1:1 (pass); footer `#666` on `#fafafa` = 5.5:1 (pass); `#2980b9` h2 on white = 4.3:1 (passes only as large text, which the bold h2 is; do not reuse it for body text); recheck any new colour with a contrast checker (e.g., WebAIM: https://webaim.org/resources/contrastchecker/).
- **Links:** descriptive text ("Read about Hampi"), never "click here".
- **Landmarks:** `header`, `main`, `footer` help screen-reader navigation; the page currently lacks `main`.
- **Motion:** wrap any animation in `@media (prefers-reduced-motion: no-preference)`.

## Quick Manual Test
1. Navigate with Tab only; focus must stay visible.
2. Zoom to 200%; content must reflow without horizontal scrolling.
3. Turn off CSS; content order must still make sense.
