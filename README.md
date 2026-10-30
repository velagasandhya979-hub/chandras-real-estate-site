# Chandra Estates

Single-page front-end design for a real estate agency (Houses, Apartments, Land & Plots, Farm Houses).

## Preview

Open `index.html` in a browser, or serve the folder locally:

```powershell
python -m http.server 8000
```

Then visit http://localhost:8000

## Design

A mix of Swiss grid discipline, bento layout, glass surfaces and wabi-sabi warmth:

- 12-column bento grid with asymmetric, softly rounded tiles
- Glass panels over a living "ink wash" backdrop (animated colour orbs)
- Warm palette: plaster paper, clay, deep moss, honey and blush
- Fraunces for display, Inter for UI, Caveat for handwritten annotations
- Real photography (WebP, locally hosted) instead of illustrations
- Motion: marquee ticker, scroll progress, hero ken-burns + parallax, image reveals, counters
- All motion respects `prefers-reduced-motion`

## Stack

- One self-contained `index.html` (markup, CSS and JS inline)
- Local image assets in `assets/` (WebP, ~2 MB total)
- Google Fonts: Fraunces + Inter + Caveat
- Hash router: `#home`, `#listings`, `#listings-<category>`, `#property-<id>`, `#about`, `#contact`

## Publish

The site is a static folder (`index.html` + `assets/`), so any static host works:

- **GitHub Pages** — Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)`. The repo must be public for free Pages, or keep it private and use another host.
- **Netlify Drop / Cloudflare Pages** — drag the folder in, no build step.
- **Any host** — upload `index.html` and `assets/` to the web root.

After a real domain exists, change the two share-image tags to absolute URLs
(`https://your-domain/assets/hero.webp`) so Facebook and WhatsApp can preview the image.

## Notes

- Listings, filters, gallery and contact form are front-end only — no data leaves the page.
- Contact number 98499 96566 is wired for both `tel:` calls and WhatsApp.
- Anything marked `FEATURED`, the counters (412 sold, 4.9 rating) and the testimonials are sample content — replace with real figures before launch.
- Photography sourced from [Unsplash](https://unsplash.com) under the Unsplash License.
