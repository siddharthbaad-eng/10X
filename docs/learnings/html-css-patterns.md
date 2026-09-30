# HTML & CSS Patterns (~450 tokens)

Self-contained guide for markup and styling in this static site.

## Page Structure
- Start every page with `<!DOCTYPE html>`, `<html lang="en">`, a UTF-8 charset meta, and a viewport meta.
- Use one `h1` per page, then `h2` for each item. Do not skip heading levels.
- Wrap primary content in `<main>` (the current page omits it; add it on the next structural edit).

## Repeated Content
- Each destination is a `<section class="place">` with an `h2` and two `p` elements.
- Keep numbering in the `h2` text in sync with order. If the list grows, consider an `<ol>` so numbering is automatic.

## CSS
- Current approach: one inline `<style>` block per page. Fine for a single page.
- **Extract to `styles.css`** once a second page reuses the rules, and link it with `<link rel="stylesheet" href="styles.css">`.
- Prefer CSS custom properties for the palette so a restyle touches one place:
  ```css
  :root { --heading: #2c3e50; --accent: #2980b9; --text: #333; --bg: #fafafa; }
  ```
- Use relative units (`rem`, `%`, `max-width`) over fixed pixel widths.

## Layout
- A readable line length is roughly 60–80 characters; `max-width: 70ch; margin: 0 auto;` on `main` achieves this.
- For card grids, `display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1rem;` adapts from phone to desktop without media queries.

## Anti-Patterns
- Inline `style=""` attributes on individual elements.
- `<br>` for spacing (use margins).
- `<div>` where a semantic element (`section`, `article`, `nav`) fits.
