# Architecture Map (~350 tokens)

## Directory Structure

```
10X/
├── CLAUDE.md                          # Agent entry point
├── .claudeignore                      # Paths agents should not auto-load
├── top10-tourist-places-india.html    # Main content page (~4 KB)
├── firstfile.html                     # Empty placeholder (0 bytes)
├── .claude/                           # Agent working docs
│   ├── COMMON_MISTAKES.md, QUICK_START.md, ARCHITECTURE_MAP.md
│   ├── LEARNINGS_INDEX.md, DOCUMENTATION_MAINTENANCE.md
│   ├── completions/  sessions/  templates/
└── docs/
    ├── INDEX.md, QUICK_REFERENCE.md
    ├── learnings/                     # Topic guides
    └── archive/                       # Historical docs
```

## Main Page Anatomy (`top10-tourist-places-india.html`)

```
<head>   meta charset + viewport, <title>, inline <style>
<body>
  <header>   h1 + intro paragraph
  <section class="place"> × 10   h2 "N. Name", p "Location: …", p description
  <footer>   credit line
```

CSS classes in use: `.place` (card: white background, 1px border, 8px radius, soft shadow).

## Where to Find Things

| Need | Location |
|------|----------|
| A destination's copy | Its `<section class="place">` block, in numeric order |
| Colours and fonts | `<style>` in `<head>` (`#2c3e50` h1, `#2980b9` h2, Arial) |
| Page title | `<title>` and `<h1>` (keep them in sync) |
