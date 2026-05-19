# Paradox.cat 🐱

**Schrödinger's Cat — a bilingual landing page about quantum uncertainty.**

The cat is both alive and dead. Until you look.

[![paradox.cat](https://img.shields.io/badge/web-paradox.cat-67e8f9?style=flat-square)](https://paradox.cat)

---

## Overview

A single-page, bilingual (English / Catalan) landing page exploring Schrödinger's Cat and quantum superposition. Built as a minimal, elegant, interactive experience.

- **Interactive experiment** — Click "Observe" to collapse the superposition. The cat is randomly alive or dead.
- **Bilingual** — Instant language switcher (EN / CA) with full i18n for all content.
- **Particle effects** — Subtle quantum-inspired particles floating in the background.

## Tech Stack

| Tech                                                                                                                      | Purpose                          |
| ------------------------------------------------------------------------------------------------------------------------- | -------------------------------- |
| Vanilla HTML / CSS / JS                                                                                                   | Zero framework, no build step    |
| [Tailwind CSS](https://tailwindcss.com/) (CDN)                                                                            | Utility-first styling            |
| [Playfair Display](https://fonts.google.com/specimen/Playfair+Display) + [Inter](https://fonts.google.com/specimen/Inter) | Serif headings + sans-serif body |
| Cloudflare Pages                                                                                                          | Deployment & CDN                 |

## Features

- **SEO-optimised** — Meta tags, Open Graph, Twitter Cards, JSON-LD structured data, sitemap, hreflang
- **GDPR-compliant** — Cookie consent banner, privacy policy modal, no tracking
- **Accessible** — ARIA labels, keyboard navigation, skip link, reduced-motion support
- **Responsive** — Mobile-first, works on all screen sizes

## Getting Started

```bash
# Clone the repo
git clone https://github.com/tommodore/paradox-website.git

# Open locally (no build step needed)
open index.html
```

## Deployment

Deployed via **Cloudflare Pages**. The repo is configured with:

- [`wrangler.toml`](./wrangler.toml) — Cloudflare Pages config
- [`_headers`](./_headers) — Security & caching headers
- [`_redirects`](./_redirects) — Redirect rules
- [`robots.txt`](./robots.txt) — Search engine crawling
- [`sitemap.xml`](./sitemap.xml) — XML sitemap

### Deploy via CLI

```bash
npx wrangler pages deploy .
```

### Deploy via Dashboard

Connect `tommodore/paradox-website` to Cloudflare Pages → set build output dir to `/`.

## Branch Strategy

```
main              ← production-ready (protected)
agent/*           ← agentic work branches (short-lived)
experiment/*      ← spikes / tests
```

## License

© Paradox.cat
