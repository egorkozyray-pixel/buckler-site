# Buckler Site — Deploy Package

Static HTML site. No build step. Hosted on GitHub Pages under the `buckler.by` domain.

## Structure

- `index.html` — entry / chooser page (Professional vs Digital); the Professional half plays the factory video loop
- `Buckler.html` — Buckler Professional landing: hero video, 12 products with detail sheets, repair-process rail,
  factory film, PDF catalog viewer (pdf.js from jsDelivr, SRI-pinned), partners
- `Buckler Digital.html` — Buckler Digital landing (Ozon line)
- `assets/pro/` — Professional page assets
  - `products/<code>.webp` (960 px) and `<code>-600.webp` — product scenes (Gemini Nano Banana Pro, labels checked
    against the can renders; 207 and 107 had a misspelled Russian line repaired from the render)
  - `process/*.webp` — repair-process photos (Gemini), `stills/*.webp` — frames from the factory film
  - `video/hero-1080.mp4`, `hero-720.mp4`, `hero-m.mp4` (vertical, phones) — 16 s muted loop cut from the 4K
    factory film; `factory-film.mp4` — the full film (1080p); `*-poster.jpg` — first frames
  - `cta.webp` / `cta-m.webp` — partners background, `og.jpg` — share card, `logo-*.png`, `icon-*.png`, `shield.png`,
    `car-line.png` (red car line cut from the HS 105 label artwork)
- `assets/digital/` — Digital page assets
- `assets/og-image.jpg` — share card for the home page
- `assets/catalog.pdf` — 32-page Professional catalog
- `tds/`, `sgr/` — documents behind the label QR codes (stable URLs, see tds/README.txt)

## Design

Colours come from the Buckler Professional labels: Pantone Black 6 (`#101820`, page `#0b1117`) and Pantone 485
(`#da291c`). Font: Montserrat (Google Fonts). Layout is mobile-first (breakpoints 640 / 900 / 1200 px).

## Deploy

Push to `main`; GitHub Pages rebuilds in 1–3 minutes. Never commit `CLAUDE.md` or `.deploy.env`.

## Contact

compositecoat@gmail.com

© ООО «Композиционные материалы и технологии», Солигорск, Беларусь
