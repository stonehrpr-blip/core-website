# CORE — landing page

Marketing site for **CORE**, the honest life-OS: most apps reward a fake perfect streak; CORE rewards the honest one — log every slip, prove the real work, climb one Life Score, with an AI coach that knows your history.

## What's here

A single self-contained static site (no build step, no framework):

- `index.html` — the whole landing page (vanilla HTML/CSS/JS, Apple system font)
- `privacy.html`, `terms.html` — finished legal pages (still need a final lawyer review before launch)
- `404.html` — branded not-found page
- `site.webmanifest`, `_headers`, `robots.txt`, favicons — deploy metadata
- `assets/` — logo, app icon, and a land-mask used by the globe

### Features
- Pink/purple gradient hero, site-wide starfield, scroll "tracing beam"
- Resizable navbar (shrinks into a floating pill on scroll)
- How-it-works steps and a 2×2 benefits grid
- A lightweight 2D `<canvas>` dot-globe with animated city arcs (continents drawn from local `assets/land-mask.png`; no external/CDN dependency)
- Pricing with a monthly/annual toggle ($0.99 first month → $4.99/mo, or $39.99/yr), with auto-renew disclosure
- Single-open animated FAQ accordion
- Contact form + "Notify me at launch" email capture, both wired to FormSubmit → corestudiosupport@gmail.com (activated and delivering)
- Always opens at the top on load/refresh; respects `prefers-reduced-motion`

## Run locally

It's static — serve the folder over http (the globe fetches a local asset and the forms POST over the network, so use http(s), not `file://`):

```bash
python3 -m http.server 4321
# open http://localhost:4321
```

## Deploy

Drop the folder on any static host (Netlify, Vercel, GitHub Pages, Cloudflare Pages). No build needed. `_headers` sets baseline security headers on Netlify.

## Before launch
- Add real App Store / Google Play links (currently `#`, intentionally disabled "Coming soon")
- Final lawyer review of `privacy.html` / `terms.html`; confirm the real legal entity, governing law, and contact address
- After choosing the custom domain: set absolute `og:url`/`og:image`/canonical URLs, add a `sitemap.xml` + `Sitemap:` line in `robots.txt`, and (optionally) a Content-Security-Policy in `_headers`
