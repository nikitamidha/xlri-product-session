# assets

## Portrait

Drop it here as **`nikita.jpg`**. `about-me.html` (and `index.html` on the
published site) point at `assets/nikita.jpg`; until the file exists the page
shows an "NM" monogram instead. Portrait crop, roughly 800×1000px.

## Logos — `logos/`

| File | Status |
| --- | --- |
| `microsoft.svg` | **Real** — the four-square mark in its exact brand colours |
| `salesforce.svg` | **Real** — the official cloud (gilbarbara/logos, MIT) |
| `freshworks.svg` | Placeholder — monogram tile |
| `spotdraft.svg` | Placeholder — monogram tile |
| `xlri.svg` | Placeholder — monogram tile |
| `bits-pilani.svg` | Placeholder — monogram tile |

Freshworks, SpotDraft, XLRI and BITS Pilani are not in any logo library this
environment can reach, and their own sites are blocked by the network policy —
so they are plain monogram tiles rather than hand-drawn imitations of the real
marks. Their tile colours are approximations of each brand, not sampled values.

To swap one in, save the official SVG over the same filename. Nothing else needs
to change: the page sizes every mark to 28px tall and prints the organisation
name beside it in the page font, so a mark-only SVG (no wordmark) fits best.
