# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Jekyll-based static site hosted on GitHub Pages at `doc.coinport.com.au`. This repo stores **public-facing documentation** for CoinPort Cryptocurrency Exchange — including legal documents, compliance records, company policies, support articles, and blog posts. GitHub Pages was chosen as an efficient and convenient way to store and present a large amount of static information that needs to be regularly updated.

As a cryptocurrency exchange, CoinPort regularly undergoes due diligence checks with regulatory bodies and onboarding/compliance reviews with market counterparties (e.g. Binance). This repo serves as a **single source of truth** for documentation commonly requested during these processes. Content is either copy-pasted into emails and web forms, or shared as direct URLs for download.

Static content relevant to exchange members — such as contact details, terms and conditions, etc. — is also hosted here for easy access. Storing documents in a git repo provides full version history tracking. Pages are also designed to be embedded in iframes within the main `coinport.com.au` web application.

## Build Commands

```bash
bundle install              # Install Ruby dependencies
bundle exec jekyll serve    # Run local dev server (http://localhost:4000)
bundle exec jekyll build    # Build to _site/
```

Changes to `_config.yml` require a server restart (incremental build is enabled). There are no automated tests, linters, or JavaScript build tools in this project.

## Deployment

Push to `main` branch triggers automatic GitHub Pages deployment. The CNAME is `doc.coinport.com.au`.

## Architecture

**Two content patterns coexist:**

1. **Jekyll/Markdown pages** (`.md` with YAML front matter) — used for legal docs, policies, about pages, blog posts, maintenance page. Use `layout: default` for standard pages, `layout: post` for blog posts.

2. **Static HTML pages** (`index.html` in subdirectories) — used for articles (`articles/`), org chart (`org/`), block page, earn page. These are plain HTML, not processed by Liquid. Must manually include theme-switching JS and link to `/style.css`.

**Key directories:**
- `_layouts/` — `default.html` (main layout) and `post.html` (blog layout with social footer)
- `about/` — Company info pages (fees, security, careers, contact, etc.)
- `articles/` — Static HTML educational articles; use `articles/0template/` as template for new articles
- `legal/` — Legal documents, compliance records, AML/CTF program
- `policies/` — Employee and operational policy documents
- `org/` — Corporate structure chart and NZ expansion docs
- `coins/`, `chains/` — Cryptocurrency and blockchain network logo images

## Theme System

Light/dark mode is controlled via URL query parameter `?theme=dark-mode`. All pages include this JS snippet (in `default.html` layout or inline in static HTML):

```javascript
const theme = new URLSearchParams(window.location.search).get('theme');
document.body.classList.toggle(theme === 'dark-mode' ? 'dark-mode' : 'light-mode');
```

CSS variables for both themes are defined in `/style.css` (`:root` for light, `body.dark-mode` for dark).

## Iframe Integration

The `default.html` layout includes a script that reports document height to the parent window via `postMessage`, allowing the parent `coinport.com.au` app to resize the iframe dynamically.

## Blog Posts

Follow Jekyll naming convention: `_posts/YYYY-MM-DD-title.md`. The `post` layout automatically appends CoinPort branding and social media links.

## Key Configuration

- Jekyll 3.9.5 with `github-pages ~> 231` (must stay GitHub Pages compatible)
- Theme: `minima ~> 2.5` (overridden by custom layouts)
- Markdown: kramdown with GFM input and Rouge syntax highlighting
- Timezone: `Australia/Sydney`
- Plugins: jekyll-feed, jekyll-seo-tag, jekyll-sitemap, jekyll-titles-from-headings, jekyll-redirect-from, jekyll-include-cache

## AML/CTF Program

The current AML/CTF Program is `legal/docs/CoinPort_AML_CTF_Program_v3.1_2026.md` (v3.1, effective January 2026). This was produced following a periodic review with law firm Holley Nethercote. The AML/CTF Compliance Officer is Nicanor Nuqui.

## Company Context

CoinPort Pty Ltd (ABN 12 624 879 223), AUSTRAC-registered DCE (100633359). Parent entity: M1 Digital Pty Ltd. Subsidiaries include CoinPort Limited (NZ) and CoinPort Inc. (Philippines).
