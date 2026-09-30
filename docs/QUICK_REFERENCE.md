# Quick Reference (~350 tokens)

## Session Start Checklist
- [ ] CLAUDE.md loaded (auto)
- [ ] COMMON_MISTAKES.md, QUICK_START.md, ARCHITECTURE_MAP.md loaded (via imports)
- [ ] Task-specific learnings file picked from `docs/INDEX.md`

## Commands
```bash
python3 -m http.server 8000          # serve
npx --yes html-validate "*.html"     # validate
```

## Code Patterns

**Destination card**
```html
<section class="place">
  <h2>11. Name</h2>
  <p>Location: City, State or Union Territory</p>
  <p>One to three plain-English sentences.</p>
</section>
```

**New page skeleton**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Title</title>
</head>
<body>
  <header><h1>Page Title</h1></header>
  <main></main>
  <footer></footer>
</body>
</html>
```

## Debugging Quick Tips
- Styles not applying → check selector spelling and that the `<style>` block sits inside `<head>`.
- Layout overflowing on phones → look for fixed widths; use `max-width` and `%`.
- Validator error on a line → fix the first error first; later ones often cascade from it.

## File Locations
Main page: `top10-tourist-places-india.html` · Empty page: `firstfile.html` · Map: `.claude/ARCHITECTURE_MAP.md`
