# CORE — landing page

Marketing site for **CORE**, the honest life-OS: most apps reward a fake perfect streak; CORE rewards the honest one — log every slip, prove the real work, climb one Life Score, with an AI coach that knows your history.

## What's here

A single self-contained static site (no build step, no framework):

- `index.html` — the whole landing page (vanilla HTML/CSS/JS, Apple system font)
- `privacy.html`, `terms.html` — legal pages (fill in the `[BRACKETED]` placeholders before launch)
- `assets/` — logo, app icon, screenshots, demo video

### Features
- Pink/purple gradient hero, site-wide starfield, scroll "tracing beam"
- Resizable navbar (shrinks into a floating pill on scroll)
- How-it-works steps, benefits, an interactive 3D globe (Three.js via CDN — needs http(s))
- Pricing with a monthly/annual toggle ($4.99/mo · $39.99/yr)
- Single-open animated FAQ accordion
- Contact form wired to FormSubmit → corestudiosupport@gmail.com

## Run locally

It's static — serve the folder over http (the globe and contact form need http(s), not `file://`):

```bash
python3 -m http.server 4321
# open http://localhost:4321
```

## Deploy

Drop the folder on any static host (Netlify, Vercel, GitHub Pages, Cloudflare Pages). No build needed.

## Before launch
- Add real App Store / Google Play links (currently `#`)
- Fill in the legal-page placeholders
- Activate the FormSubmit endpoint (one-time confirmation email on first submit)
