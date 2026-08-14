# kiwidock-marketing-assets

Public, directly-embeddable static assets (screenshots, images) for the [kiwidock.com](https://kiwidock.com) marketing site.

This repo exists solely because the CMS behind kiwidock.com's marketing pages (managed via the `kiwidock-blog` MCP server from the private `kiwidock-growth` planning repo) accepts sanitized HTML for page bodies but has no image-upload/media tool. Images referenced from marketing page HTML need a stable, public, anonymously-fetchable URL — this repo, served through the [jsDelivr GitHub CDN](https://www.jsdelivr.com/documentation#id-github), is that URL.

## Usage pattern

Files here are referenced from marketing page HTML like:

```
https://cdn.jsdelivr.net/gh/derekbackus/kiwidock-marketing-assets@main/product-tour/01-dashboard.png
```

jsDelivr serves any public GitHub repo's contents with correct `content-type`, CORS, and caching, no extra account or credentials needed. If a very recently pushed file hasn't propagated yet, pin to the specific commit SHA (`@<sha>` instead of `@main`) or retry after a few minutes.

## Contents

- `product-tour/` — 9 clean product-tour screenshots from a synthetic demo tenant ("Northshore Shop"), used across kiwidock.com's `home`, `how-it-works`, `for-fab-shops`, and `for-service-businesses` pages as of 2026-08-14. Source of truth for what each screenshot shows and why: `drafts/assets/product-tour-clean/README.md` in the private `kiwidock-growth` repo (not duplicated here — this repo is asset hosting only, not documentation).

## Provenance

Do not add anything here that isn't meant to be public — this repo has no auth and no gate. All content is expected to already be public-safe (e.g. synthetic demo data, no real customer information) before it lands here.
