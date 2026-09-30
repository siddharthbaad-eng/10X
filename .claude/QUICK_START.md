# Quick Start (~250 tokens)

## Essential Commands

```bash
# Serve locally
python3 -m http.server 8000
# → http://localhost:8000/top10-tourist-places-india.html

# Validate all HTML (uses the html-validate npm package; exit 0 = pass)
npx --yes html-validate "*.html"
```

There is no install, build, or database step.

## Change Workflow

1. Read `.claude/COMMON_MISTAKES.md`.
2. Edit the HTML file.
3. Validate → render at desktop and phone width → fact-check changed content.
4. Commit with a descriptive message.
5. Write a completion doc in `.claude/completions/` for non-trivial tasks (template: `.claude/templates/completion-template.md`).

## Common Workflows

| Task | Steps |
|------|-------|
| Add a destination | Copy a `<section class="place">` block, renumber, update the title if the count changes |
| Restyle the page | Edit the `<style>` block; recheck contrast and mobile width |
| Add a new page | Start from the head of the main page; see `docs/learnings/html-css-patterns.md` |
