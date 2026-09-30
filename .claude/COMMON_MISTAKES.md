# Common Mistakes ⚠️

Read before every change (~400 tokens).

## Top 5 Critical Mistakes

1. **Outdated administrative geography.** Ladakh became a separate Union Territory on 31 Oct 2019. The page currently lists Leh-Ladakh under "Jammu and Kashmir", which is out of date. Always check the current state/UT before editing a location line.
2. **Shipping invalid HTML.** Browsers hide markup errors, so a page can look fine and still fail validation. Run `npx --yes html-validate "*.html"` before every commit.
3. **Duplicating CSS across pages.** Copying the `<style>` block into a second page creates drift. Extract a shared stylesheet as soon as two pages share rules.
4. **Breaking mobile layout.** Never remove the viewport meta tag, and avoid fixed pixel widths. Check the page at ~375px.
5. **Hot-linking or unlicensed images.** If you add photos, use images you own or that carry a clear licence (e.g., Wikimedia Commons with attribution), store them in the repo, and always include `alt` text.

## Static-Site Gotchas

- File names are case-sensitive on most web hosts (including GitHub Pages); `Index.html` ≠ `index.html`.
- There is no `index.html`, so a host serves a directory listing or 404 at the site root.
- Opening files via `file://` can break relative fetches; use `python3 -m http.server`.

## Testing Pitfalls

- Visual checks alone miss accessibility issues (heading order, missing `alt`, contrast).
- Validator exit code 0 does not prove content is accurate; fact-check separately.

## Deployment Issues

- Committing the empty `firstfile.html` publishes a blank page; fill it or remove it before deploying.
