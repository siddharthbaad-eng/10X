# Documentation Maintenance (~400 tokens)

## When to Update COMMON_MISTAKES.md

Add an entry when a mistake:
- shipped to a published page (wrong fact, broken layout), or
- cost more than one attempt to fix, or
- is likely to recur for anyone editing this stack.

Keep the file under ~60 lines. Merge similar entries; move detail into a learnings file and link to it.

**Example:** A destination was listed under the wrong state → add to "Top 5" if serious, with the correct source to check.

## When to Create Completion Docs

After every non-trivial task (new page, restyle, content batch). Skip for typo fixes.
Use `.claude/templates/completion-template.md`; name it `YYYY-MM-DD-short-slug.md` in `.claude/completions/`.

## When to Archive Docs

Move a file to `docs/archive/` (or `.claude/sessions/archive/`) when it is:
- a planning doc for work that is finished,
- a proof-of-concept summary, or
- superseded by a newer file.

Add a one-line entry to `docs/archive/README.md` noting what replaced it.

## When to Update Learnings

- A new, reusable pattern emerges (e.g., shared stylesheet, image component) → add to the matching `docs/learnings/` file.
- A file grows past ~1,000 lines → split it by topic and update `LEARNINGS_INDEX.md` and `docs/INDEX.md`.

## Decision Tree

```
Finished a task?
├── Caused or fixed a real bug? ── yes → update COMMON_MISTAKES.md
├── Non-trivial?                ── yes → write completion doc
├── Found a reusable pattern?   ── yes → update docs/learnings/<topic>.md
└── Made a doc obsolete?        ── yes → move it to docs/archive/
```
