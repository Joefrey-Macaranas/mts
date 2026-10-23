# MTS Shop — Manage Tech Shop (local HTML demo)

Self-hosted HTML/CSS/JS eCommerce demo rebranded from the **Bigshop** template.

- Source: `https://harnishdesign.net/demo/html/bigshop/v1/`
- Brand: **MTS Shop** — "Manage Tech Shop"
- Logo asset: `image/logo.png` (from `manage tech shop logo.jpeg`, trimmed + scaled)

## Run locally

```bash
cd /Users/joefreymacaranas/cloned-site
python3 -m http.server 8080
# open http://localhost:8080
```

The live demo is served from the root of this folder (no build step, no bundler).

## Rebrand notes

- Brand name replaced: `Bigshop` → `MTS Shop`, `bigshop.com` → `mtsshop.com`
- Designer credit (`HarnishDesign`) replaced with MTS Shop.
- Theme accent colour `#f15a23` (orange) → `#0b7c90` (brand cyan) with
  `#5fe3f7` / `#2ad4ee` highlights (`css/stylesheet.css`, appended `MTS Shop brand layer`).
- Header logo rendered at `66px` height via `#header #logo img { height:66px; width:auto; }`.
- Hero banners (`image/slider/banner-1..4.jpg`), sidebar promos
  (`image/banner/sb*.jpg`) and CMS promo (`image/banner/mts-promo-410x170.jpg`) are
  MTS Shop branded renders generated from the MTS Shop palette.
- Contact page: `contact-us.html` (form + store details + map).
- Returns: `returns.html` is a redirect to `return.html`.
- Favicon: `image/favicon.png`.

## Assets

- `image/logo.png` — 358×132 (2× scale of trimmed source, 179×66 @1×), 24-bit PNG.
- `email-template/logo.png` — same asset for the marketing email template.
- `image/favicon.png` — 128×128 favicon (cyan mark, black “M”).

## Validation

- `python3 /private/var/folders/g8/7g85cb8x59x07yjszl75lkx40000gn/T/opencode/link-check.py`
  (or point it at this folder) verifies all local asset references resolve.
- Rebrand was verified with headless Chromium (Playwright): titles, colours,
  logo geometry and horizontal overflow at 1440px and 390px viewports.
