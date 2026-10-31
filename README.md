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

## Demo data

All 12 properties are **fictional sample data for demonstration only**. None of them is a real
property, a real address or an offer for sale or rent.

- Prices are illustrative INR figures, not valuations and not converted from another currency.
- City and district names are real Indian places used as sample locations. Every locality, plot
  number and address is invented — addresses are prefixed `Fictional address:`. This does not imply
  the agency operates in those cities.
- No PIN code, ownership detail, survey number, approval or RERA registration exists for any record;
  those fields are `null` rather than guessed.
- Every record carries `status: "demo-only"`, `availability: "not-available"`, `priceType:
  "illustrative"`, `listingType: null` and `isDemo: true`. Nothing is offered for sale or rent.
- The same 12 records live in two places and must be kept in sync: the `const properties` array in
  `index.html` (what the site renders) and `properties.json` (a read-only export the site does not
  fetch yet).
- Demo status is shown in the interface, not only in the footer: a `DEMO LISTING` label on every
  property card, a notice on every detail page and in the quick-view drawer, a banner on the listings
  page, and a note under the enquiry form.
- Photographs are stock images used as illustrative demo images. They do not depict the property
  described; galleries are captioned and alt text is deliberately generic. Land listings use only
  their own image plus the shared `cat-land.webp`, never another plot's photo.

## Notes

- Listings, filters, gallery and contact form are front-end only — no data leaves the page, and the
  enquiry form has no backend, so nothing is sent, stored or shared.
- No phone number, email, office address or map location is published. Contact details are demo
  placeholders only; do not add real ones without the agency's confirmation.
- The hero counters (12 sample properties, 4 categories, 0 real listings) and the testimonial are
  sample content, labelled as such. There are no sold-property statistics, ratings, licensing claims
  or agency history anywhere on the site.
- Photography sourced from [Unsplash](https://unsplash.com) under the Unsplash License.
