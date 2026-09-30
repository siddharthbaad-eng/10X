# CLAUDE.md — 10X

## Project Overview

10X is a static, beginner-friendly HTML site. It has no build step, no framework, and no dependencies.
The main page, `top10-tourist-places-india.html`, lists ten Indian travel destinations using plain HTML with inline CSS.
`firstfile.html` exists but is currently empty (0 bytes).

## Session Start Protocol

**MANDATORY** at the start of each session. Claude Code auto-loads this file; the imports below pull in the rest (~1,700 tokens total):

- CLAUDE.md (this file)
- @.claude/COMMON_MISTAKES.md ⚠️ CRITICAL
- @.claude/QUICK_START.md
- @.claude/ARCHITECTURE_MAP.md

**Then load task-specific docs** (~200-550 tokens each). See `docs/INDEX.md` for navigation.

**⚠️ NEVER auto-load** (load only when the user explicitly asks):
- `.claude/completions/**`
- `.claude/sessions/**`
- `docs/archive/**`

## Quick Start

```bash
python3 -m http.server 8000                 # serve locally → http://localhost:8000/top10-tourist-places-india.html
npx --yes html-validate "*.html"            # validate markup (exit 0 = pass)
```

Full command list: `.claude/QUICK_START.md`.

## Architecture Quick Reference

| What | Where |
|------|-------|
| Main page | `top10-tourist-places-india.html` |
| Styles | Inline `<style>` block in each page's `<head>` |
| Placeholder page | `firstfile.html` (empty) |
| Agent docs | `.claude/` |
| Human/topic docs | `docs/` |

Details: `.claude/ARCHITECTURE_MAP.md`.

## Testing Methodology

No automated test suite exists. Verify each change in three steps:
1. **Validate:** run `npx --yes html-validate "*.html"` and fix every error.
2. **Render:** serve locally and check the page at desktop and ~375px phone width.
3. **Fact-check:** confirm any changed place name, state, or claim against an authoritative source (see `docs/learnings/content-accuracy.md`).

## Documentation Navigation

- `docs/INDEX.md` — task-based navigation with token estimates
- `docs/QUICK_REFERENCE.md` — fast lookups
- `docs/learnings/` — topic guides (load one at a time)
- `.claude/DOCUMENTATION_MAINTENANCE.md` — when to update, archive, or record mistakes

## Code Style Guidelines

- HTML5 with `<!DOCTYPE html>`, `lang="en"`, UTF-8 charset, and a viewport meta tag.
- Two-space indentation.
- Use semantic elements (`header`, `main`, `section`, `footer`); one `h1` per page.
- Keep CSS in the page's `<style>` block unless a second page needs the same rules; then extract to a shared `.css` file.
- Class names: lowercase, hyphenated (`.place`, `.place-card`).
- Write copy in plain, active-voice English suited to beginners.
