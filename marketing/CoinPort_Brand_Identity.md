---
layout: default
title: CoinPort Brand Identity Guide
description: Brand system, tokens, components and usage rules for the CoinPort exchange.
---

# CoinPort Brand Identity Guide

**Version 2.0 · May 2026**
**Sources:** `light.pcss` · `dark.pcss` · `LogoIcon.tsx` · `CH_Colour_Template.svg` · live product screenshots

> The interactive version with live demos, screenshots, and component previews is at **[CoinPort_Brand_Identity.html](./CoinPort_Brand_Identity.html)**. This page is the searchable plain-text reference.

---

## Tagline

> **Easy, fast and safe way to trade crypto.**

### Approved variants

| Variant | Form | Use |
|---|---|---|
| Full form (primary) | "Easy, fast and safe way to trade crypto." | Landing hero, About page, paid ad headlines, OG meta, App Store / Google Play descriptions, `_config.yml` site description, SEO meta description, press boilerplate |
| Short form | "Easy, fast and safe." | Three-word lockup for icon rows, social bio, footer strap |
| Pillar attribute set | "Easy · Fast · Safe" | Feature-row labels. Maps to: **Easy** → instant AUD via Osko/PayID · **Fast** → sub-minute deposits · **Safe** → AUSTRAC VASP, 2FA, cold storage |

### Punctuation & capitalisation

- **Comma** — single comma between "Easy" and "fast". No serial comma before "and safe".
- **Lowercase** — "easy", "fast", "safe", "way", "trade", "crypto" all lowercase in body context. Sentence-case at the start. All-caps only in micro-contexts (badges, labels < 14px).
- **Full stop** — include when the tagline ends a paragraph or sits alone. Drop when set inline in a sentence or as a button/CTA label.
- **Emphasis** — when highlighting one phrase, italicise or colour-shift the first three words ("Easy, fast and safe"), never the last clause.

### Do

- Use the full form on every public-facing surface where there's room.
- Pair with a single specific proof (zero fees, instant AUD, AUSTRAC, 24/7 support) — not three.
- Set in Poppins, 600–700 weight.
- Treat the tagline as a sentence: capital E at start, full stop at end (where context allows).
- Keep "Easy", "fast" and "safe" in that order — the rhythm is the brand.

### Don't

- Reorder — never "Fast, safe and easy" or "Safe, easy and fast".
- Add adjectives — not "Easy, fast, safe *and cheap*" or "*The* easiest, fastest, safest...".
- Translate inside a single en-AU asset — English only on AU surfaces.
- Use as a verb claim ("We make crypto easy, fast and safe") — keep it as a noun-phrase descriptor.
- Combine with hype phrases ("Easy, fast and safe — to the moon").

---

## Quick reference

| | |
|---|---|
| **Legal entity** | CoinPort Pty Ltd · ABN 12 624 879 223 |
| **Address** | Level 2, 696 Bourke St, Melbourne VIC 3000 |
| **Regulator** | AUSTRAC VASP · Registration #100633359 |
| **Web** | [coinport.com.au](https://www.coinport.com.au) |
| **Docs** | [doc.coinport.com.au](https://doc.coinport.com.au) |
| **iOS** | App Store ID 1477376905 |
| **Android** | app.mobile.coinport |
| **Social** | [@CoinPortEx](https://twitter.com/CoinPortEx) |
| **Brand font** | Poppins (weights 300–800) |

---

## 01 — Logo system

The CoinPort wordmark is composed of three elements:

1. **Keyhole** — the cyan dot inside the "C", `#1AADFF`. Never recolour.
2. **Letterforms** — `#00233A` on light backgrounds, `#FFFFFF` on dark.
3. **Counter-holes** — the "o" letters use two sub-paths with `fill-rule="evenodd"` so the inner counter punches through.

### Variants

| Variant | Background | Letterforms | Keyhole | Use |
|---|---|---|---|---|
| Light wordmark | Light surfaces | `#00233A` | `#1AADFF` | Email signatures, light landing, print |
| Dark wordmark | Dark surfaces (≥ `#002355`) | `#FFFFFF` | `#1AADFF` | Headers, nav, dark mode, photos |
| Icon mark | Any | `#00233A` or `#FFFFFF` | `#1AADFF` | App icons, favicons, square contexts |

### Clear space

Minimum clear space around the wordmark equals the height of the keyhole circle. Never crop, recolour the C/letterforms, add effects (shadow, glow, bevel), or rotate.

**Source file:** `web/src/components/Logo/LogoIcon.tsx`. Use the SVG directly — no rasterisation unless required for OG/social.

---

## 02 — Colour system

Defined as RGB triplets in `light.pcss` / `dark.pcss`. Mode toggled via `:root.light-mode` / `:root.dark-mode`. Use `rgba(var(--rgb-*), alpha)` for translucent layers.

### Invariant — both modes identical

| Token | Hex | RGB | Nautical name |
|---|---|---|---|
| `--rgb-primary-cta-color` | `#0078F0` | 0, 120, 240 | Harbour Blue |
| `--rgb-contrast-cta-color` | `#FAC848` | 250, 200, 72 | Lantern Gold |
| `--rgb-landing-keyhole-color` | `#1AADFF` | 26, 173, 255 | Shoal Cyan |
| `--rgb-header-background-color` (light) | `#002355` | 0, 35, 85 | Deep Hull |
| `--rgb-asks` | `#FF617F` | 255, 97, 127 | Buoy Coral |
| `--rgb-system-yellow` | `#F7D600` | 247, 214, 0 | Beacon Yellow |

### Light mode

| Token | Hex | Nautical name | Role |
|---|---|---|---|
| `--rgb-main-background-color` | `#FFFFFF` | Sail White | Cards, panels |
| `--rgb-body-background-color` | `#F2F2F7` | Sea Mist | Page body |
| `--rgb-input-background-color` | `#F5F5FC` | Pearl Tide | Inputs, dropdowns |
| `--rgb-primary-text-color` | `#00233A` | Abyss Navy | Primary text |
| `--rgb-text-contrast-color` | `#787878` | Driftwood | Muted text |
| `--rgb-bids` | `#4BC64A` | Seagrass Green | Order book bids, positive change |
| `--rgb-secondary-contrast-cta-color` | `#FF9068` | Sunset Coral | Secondary CTA |
| `--rgb-landing-background-color` | `#0078F0` | Open Sea | Landing hero |

### Dark mode — differences from light

| Token | Light | Dark | Role |
|---|---|---|---|
| `--rgb-body-background-color` | `#F2F2F7` | `#00193C` | Page body canvas |
| `--rgb-main-background-color` | `#FFFFFF` | `#052350` | Cards, panels |
| `--rgb-header-background-color` | `#002355` | `#00193C` | Global nav header |
| `--rgb-subheader-background-color` | `#FFFFFF` | `#052350` | Sub-navigation bar |
| `--rgb-dropdown-background-color` | `#F5F5FC` | `#001E3C` | Dropdowns, inputs |
| `--rgb-primary-text-color` | `#00233A` | `#FFFFFF` | Primary text |
| `--rgb-text-contrast-color` | `#787878` | `#D2D2D2` | Secondary / muted text |
| `--rgb-secondary-contrast-cta-color` | `#FF9068` | `#F65C55` | Secondary CTA |
| `--rgb-bids` | `#4BC64A` | `#4BC65E` | Order book bids |
| `--rgb-divider-color` | `#F8F8FC` | `#002378` | Dividers |
| `--rgb-table-border-color` | `#DCDCDC` | `#234164` | Table / grid borders |
| `--rgb-alternating-row-color` | `#F8F8FE` | `#002364` | Striped table rows |
| `--rgb-landing-background-color` | `#0078F0` | `#00193C` | Landing hero |

**Alpha scale:** `--alpha: 0.12` · levels 1–8 (0.12 → 0.96 in 0.12 steps). `--button-font-weight: 500`.
Use `rgba(var(--rgb-primary-cta-color), var(--alpha-level-2))` for tinted surfaces.

---

## 03 — Typography

**Brand font:** Poppins. Loaded via Google Fonts on web; bundled with the mobile apps.

| Level | Weight | Size | Line height | Use |
|---|---|---|---|---|
| Display | 800 | 56 / 72 | 1.05 | Hero headlines |
| H1 | 700 | 36 / 48 | 1.15 | Page titles |
| H2 | 600 | 28 / 36 | 1.20 | Section heads |
| H3 | 600 | 22 / 28 | 1.25 | Sub-section heads |
| H4 | 600 | 18 / 22 | 1.30 | Card heads |
| Body lg | 400 | 16 / 24 | 1.50 | Long-form prose |
| Body | 400 | 14 / 20 | 1.55 | Default UI text |
| Body sm | 400 | 13 / 18 | 1.55 | Dense tables, metadata |
| Caption | 500 | 11 / 14 | 1.40 | Labels, footnotes, tokens |

**Numerals:** tabular figures for tables, prices, balances. Standard figures elsewhere.

---

## 04 — Buttons & navigation

### Buttons

| Variant | Background | Text | Weight | Use |
|---|---|---|---|---|
| Primary | `#0078F0` | `#FFFFFF` | 500 | Deposit, Sign In, primary actions |
| Gold | `#FAC848` | `#00233A` | 500 | Start today, secondary CTA on hero |
| Ghost | transparent | `#0078F0` | 500 | Cancel, secondary in flows |
| Dark | `rgba(0,35,85,.85)` | `#FFFFFF` | 500 | Sign In on landing page only |

All buttons use `--button-font-weight: 500`. Hover: lift to `elevation-2` and shift to slightly darker shade.

### Navigation

**Authenticated nav** — header background matches mode (`#002355` light / `#00193C` dark). White wordmark left-aligned, primary nav items mid, theme toggle + sign-out right. Active item underlined in `#FAC848`.

**Public landing nav** — same header surface. About, Blog, Learn, Research as link items. Sign In (primary) and Sign Up (gold) buttons on the right.

---

## 05 — UI patterns

- **Cards** use `elevation-1` at rest, `radius-md` (11px), 20px internal padding.
- **Order book** uses `--rgb-bids` for buys and `--rgb-asks` for sells. Never reverse.
- **Portfolio donut** colours: AUD = gold, BTC = coral, ETH = blue, Other = orange.
- **Dashboard** balance card always shows current AUD value with crypto/AUD split on a second row.

---

## 06 — Brand voice

Four pillars:

**Trustworthy** — accurate, plain language. Australian-licensed. AUSTRAC, regulated, secure are facts, not selling points to repeat in every sentence.

**Accessible** — for new users. Explain the jargon the first time. Prefer short sentences. Active voice.

**Confident** — declarative, not breathless. We don't hype, we don't promise returns, we don't use rocket emojis.

**Local** — Australian-owned, Australian-built, Australian-priced. AUD-first. Melbourne HQ.

### Do

> "Trade BTC, ETH, USDT and 40+ assets — zero fees, instant AUD deposits, backed by Australia's AUSTRAC-licensed exchange."

### Don't

> "MOON YOUR PORTFOLIO 🚀🚀 Join the CRYPTO REVOLUTION and get RICH with INSANE yields and 100x gains!!"

Never imply guaranteed returns, never use "to the moon" / "lambo" / WAGMI / GM-style jargon, never use rocket or money-with-wings emojis.

---

## 07 — Email signature

```
[CoinPort wordmark – light, 26px high]   |   Kent Kingsley
                                         |   Chief Executive Officer · CoinPort Pty Ltd
                                         |
                                         |   kent@coinport.com.au
                                         |   www.coinport.com.au
                                         |   Level 2, 696 Bourke St, Melbourne VIC 3000
                                         |   AUSTRAC VASP · Registration #100633359 · ABN 12 624 879 223
```

**Rules**

- Bottom border: `--rgb-header-background-color` (`#002355`).
- Vertical bar separating logo and details: `--rgb-primary-cta-color` (`#0078F0`).
- Links: `#0078F0`, no underline at rest, underline on hover.
- Always include AUSTRAC licence + ABN.
- Logo: light wordmark only (text `#00233A`, keyhole `#1AADFF`).
- Never include personal phone numbers in the standard signature.

---

## 08 — Alerts & warnings

Four semantic states. Never reassign colours across states.

| State | Token | Hex | Use |
|---|---|---|---|
| Success | `--rgb-bids` | `#4BC64A` | Completed positive actions only (deposit cleared, order filled, KYC approved) |
| Info | `--rgb-primary-cta-color` | `#0078F0` | Neutral notices, tips, sign-in alerts |
| Warning | `--rgb-contrast-cta-color` | `#FAC848` | User attention required, no error (maintenance, pending review, 2FA prompts) |
| Danger | `--rgb-asks` | `#FF617F` | Failures, rejections, security incidents only |

**Status pills:** Completed, Verified (success) · Processing (info) · Pending review, Action required (warning) · Failed, Cancelled (danger) · Draft, Archived (neutral).

---

## 09 — Spacing & grid

**8-point scale** derived from `--spacing-unit: 4px`. All padding, margins and gaps are multiples of 4 (preferably 8) px.

| Token | Value |
|---|---|
| `space-1` | 4px |
| `space-2` | 8px |
| `space-3` | 12px |
| `space-4` | 16px |
| `space-6` | 24px |
| `space-8` | 32px |
| `space-12` | 48px |
| `space-16` | 64px |

### Layout

- **Container max-width:** 1280px.
- **Gutter:** 24px between columns (16px at sm).
- **Page padding:** 24px mobile · 40px tablet · 64px desktop.
- **Section gap:** 80px between full-width sections on landing; 48px inside dashboard.
- **Card padding:** 20px internal; 12px headline-to-content gap.
- **Stack gap:** 16px between form fields; 8px between label and field.

### Border radius

| Token | Value | Use |
|---|---|---|
| `radius-xs` | 4px | Chips, pills |
| `radius-sm` | 8px | Small buttons, inputs |
| `radius-md` | 11px | Cards |
| `radius-lg` | 16px | Large cards, modals |
| `radius-xl` | 24px | Hero panels |
| `radius-full` | 9999px | Avatars, circle pills |

### Elevation

| Token | Shadow | Use |
|---|---|---|
| `elevation-0` | none + 1px border | Flat surfaces |
| `elevation-1` | `0 1px 3px rgba(0,35,58,.06), 0 1px 2px rgba(0,35,58,.04)` | Cards at rest |
| `elevation-2` | `0 4px 12px rgba(0,35,58,.08), 0 2px 4px rgba(0,35,58,.04)` | Dropdowns, hover |
| `elevation-3` | `0 12px 28px rgba(0,35,58,.14), 0 6px 12px rgba(0,35,58,.06)` | Modals, toasts |

### Breakpoints

`sm 640` · `md 768` · `lg 1024` · `xl 1280` · `2xl 1536`. Mobile-first.

---

## 10 — Form fields

- **Labels** always above the field. Never use floating placeholders. Required fields use a small asterisk in `#FF617F`.
- **Placeholders** show format hints only (`you@coinport.com.au`), never duplicate the label.
- **Validation** is inline immediately below the field, on blur — not as the user types. Error text `#FF617F`; success text `#4BC64A`.
- **Focus ring** must always be visible for keyboard nav. 3px ring at 18% alpha of `--rgb-primary-cta-color`. Do not set `outline: none`.
- **Spacing:** 16px between fields, 8px between label and field. Single-line height 40px.

### Component states

Text input · select · textarea · checkbox · radio · toggle — all share the same border (1.5px `--rgb-table-border-color`), the same input fill (`--rgb-input-background-color`), the same focus styling.

Checked checkbox/radio: filled with `--rgb-primary-cta-color`.
Toggle on: track `--rgb-primary-cta-color`; toggle off: track `--rgb-table-border-color`.

---

## 11 — Photography & illustration

Primary visual language is **flat illustration** — the coastal/harbour landing scene. Photography is secondary for editorial, blog and PR.

### Do

- Australian context — Melbourne CBD, Bourke St, Yarra, Sydney harbour, regional Victoria.
- Natural light — soft morning or golden hour. Cool blue-toned daylight is fine.
- Real customers in unposed moments, ages 25–65, multi-cultural, casual.
- Tight crops on hands holding phone with CoinPort UI visible.
- Cool treatment — pull yellows toward neutral, lift shadows slightly.

### Don't

- Crypto cliches — Bitcoin coins on circuit boards, neon green Matrix code, lambos, rockets.
- Hands holding glowing orbs or any AI-stock-photo aesthetic.
- Staged trading floors, suits at Bloomberg terminals.
- Heavily filtered, hyper-saturated, Instagram-y treatments.
- Celebrity, athlete, or influencer imagery without explicit licence.

### Crop ratios

| Ratio | Use |
|---|---|
| 16:9 | Hero · video |
| 4:3 | Card thumbnails |
| 1:1 | Social · OG share |
| 3:4 | Editorial portrait |
| 9:16 | Story · Reel |

### Layering rules

- **Logo on photo:** always the white wordmark, 24px safe margin, even-tone region. Add a 30–50% dark gradient at the top if the photo is busy.
- **Text on photo:** white at 92% opacity. Meet WCAG AA (4.5:1) against the photo region.
- **No image-on-image:** never sandwich illustration over photography or vice versa.
- **Attribution:** bottom-right, 10px, white at 60% opacity, prefixed "Photo: ".

---

## 12 — Icon library

Production icons are pulled from two sources in the frontend repo.

### Product UI — react-bootstrap-icons

Resolved through `web/src/assets/images/sidebar/SidebarIcons.tsx`. Used at 18px in the sidebar at `var(--cta-layer-color)`.

| Site key | Icon |
|---|---|
| `profile` | PersonCircle |
| `about` | InfoCircle |
| `legal` | FileEarmarkText |
| `dashboard` | Clipboard |
| `referrals` | Share |
| `articles` | Book |
| `apiKeys` | Key |
| `resources` | Folder |
| `research` | Search |
| `charts` | GraphUp |
| `learn` | Pencil |
| `blog` | Newspaper |
| `history` | ClockHistory |
| `orders` | ListCheck |
| `portfolio` | BarChart |
| `wallets` | Wallet2 |
| `trade` | GraphUpArrow |
| `support` | QuestionCircle |
| `api` | Cloud |
| `internal_transfer` | Shuffle |
| `quick_exchange` | ArrowLeftRight |
| `p2p` | Repeat |

### Landing — brand-coloured SVGs

`web/src/assets/images/landing/features/`:

- `Australia.svg` — Australia outline (stroke `#0078F0`)
- `Security.svg` — shield with tick (fill `#0078F0`)
- `support.svg` — 24/7 headset (fill `#0078F0`)
- `fast.svg` — lightning bolt (fill `#0078F0`)
- `zerofees.svg` — "0%" mark (fill `#0078F0`)
- `lineChart.svg` — trending line graph

`web/src/assets/images/landing/social/`:

CoinMarket · Facebook · LinkedIn · Medium · Reddit · Telegram · Tiktok · Twitter · YouTube — single-colour at `#a0a0a0`, hover state inherits `#0078F0`.

### App badges

- `web/src/assets/images/appstore.svg` — Apple App Store badge
- `web/src/assets/images/googleplay.svg` — Google Play badge

---

## 13 — Digital presence

| Channel | URL / Handle | Notes |
|---|---|---|
| Web platform | [coinport.com.au](https://www.coinport.com.au) | React app. Light/dark via `:root.light-mode` / `:root.dark-mode`. `GridMainBG.svg` + `GridMainBG_night.svg` for landing hero. |
| Documentation | [doc.coinport.com.au](https://doc.coinport.com.au) | Jekyll. Legal, policies, support, brand resources. `style.css`. OG image: `/images/logos/ch_sign_logo.png`. |
| iOS App | App Store ID 1477376905 | Native iOS. Poppins throughout. System dark mode aware. |
| Android App | `app.mobile.coinport` | Google Play. Matches iOS design exactly. |
| Social | [@CoinPortEx](https://twitter.com/CoinPortEx) | Twitter/X · Facebook · YouTube. Navy/cyan palette. Brand voice rules apply. No hype language. |
| Contact | [media@coinport.com.au](mailto:media@coinport.com.au) | Media enquiries. CoinPort will never send links or request 2FA codes by email. |

---

## Source files

| File | Where |
|---|---|
| Colour variables (light) | `frontend/web/src/styles/light.pcss` |
| Colour variables (dark) | `frontend/web/src/styles/dark.pcss` |
| Logo SVG | `frontend/web/src/components/Logo/LogoIcon.tsx` |
| Landing illustrations | `frontend/web/src/assets/images/landing/GridMainBG.svg` · `GridMainBG_night.svg` |
| Sidebar icon map | `frontend/web/src/assets/images/sidebar/SidebarIcons.tsx` |
| Feature icons | `frontend/web/src/assets/images/landing/features/*.svg` |
| Social icons | `frontend/web/src/assets/images/landing/social/*.svg` |
| Interactive guide | [CoinPort_Brand_Identity.html](./CoinPort_Brand_Identity.html) |
| Legacy PDF | [CoinPort_Identity.pdf](./CoinPort_Identity.pdf) |
