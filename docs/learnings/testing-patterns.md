# Testing Patterns (~300 tokens)

No test framework exists. Use this three-layer check on every change.

## 1. Markup Validation (automated)
```bash
npx --yes html-validate "*.html"
```
Exit code 0 means the markup passes. As of this setup, `top10-tourist-places-india.html` passes. Alternative with no install: the W3C Nu validator at https://validator.w3.org/nu/.

## 2. Render Check (manual)
```bash
python3 -m http.server 8000
```
Open the page and check:
- Desktop width and ~375px (browser dev tools device mode).
- Cards align, no horizontal scroll, text readable.

## 3. Content Check (manual)
Confirm each changed fact against a source in `content-accuracy.md`.

## Optional Upgrades (only if the site grows)
- Add a `package.json` with a `"validate"` script and run it in GitHub Actions on each push.
- Add Lighthouse CI or axe-core for automated accessibility checks.

## Pitfalls
- A passing validator says nothing about accuracy or accessibility.
- Testing only via `file://` hides path issues a real server would expose.
