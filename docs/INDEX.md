# Documentation Index

Token estimates assume ~4 characters per token and are approximate.

## Always Loaded (~1,700 tokens)

| File | ~Tokens |
|------|---------|
| `CLAUDE.md` | 650 |
| `.claude/COMMON_MISTAKES.md` | 400 |
| `.claude/QUICK_START.md` | 250 |
| `.claude/ARCHITECTURE_MAP.md` | 350 |

## Navigation by Task Type

| Task | Load | ~Extra tokens |
|------|------|---------------|
| Edit copy / add a destination | `learnings/content-accuracy.md` | 400 |
| Change layout or styles | `learnings/html-css-patterns.md`, `learnings/accessibility.md` | 700 |
| Add images | `learnings/accessibility.md`, `learnings/performance.md` | 500 |
| Add a new page | `learnings/html-css-patterns.md` | 400 |
| Verify before commit | `learnings/testing-patterns.md` | 250 |
| Publish the site | `learnings/deployment.md` | 250 |
| Update the docs themselves | `.claude/DOCUMENTATION_MAINTENANCE.md` | 400 |
| Quick lookup | `QUICK_REFERENCE.md` | 325 |

## Decision Tree

```
What are you changing?
├── Words or facts ────────────→ content-accuracy.md
├── Markup / CSS ──────────────→ html-css-patterns.md (+ accessibility.md for visuals)
├── Images, fonts, scripts ────→ performance.md + accessibility.md
├── Hosting / URLs ────────────→ deployment.md
└── Not sure ──────────────────→ QUICK_REFERENCE.md
```

## Never Auto-Load (0 tokens unless requested)

`.claude/completions/**`, `.claude/sessions/**`, `docs/archive/**`

## Before / After

| Scenario | Before (no structure) | After |
|----------|-----------------------|-------|
| Session start | Agent reads every file it finds (~1,000 tokens today, growing with each doc, completion, and session note) | ~1,700 tokens, fixed |
| Typical task | Session start + ad-hoc searching | ~1,900–2,400 tokens |

**Honest note:** this repo is tiny (the whole codebase is ~1,000 tokens), so today the docs cost more than the code. There are no savings yet. The structure pays off as pages, completion docs, and session notes accumulate, because those stay out of context by default.
