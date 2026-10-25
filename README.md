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

## Notes

- Listings, filters, gallery and contact form are front-end only — no data leaves the page.
- Photography sourced from [Unsplash](https://unsplash.com) under the Unsplash License.
