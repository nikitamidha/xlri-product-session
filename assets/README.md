# assets

## Portrait

Drop it here as **`nikita.jpg`**. Both `about-me.html` and `about-me.md` point
at `assets/nikita.jpg`; the HTML page shows an "NM" monogram until it exists.
Portrait crop, roughly 800×1000px, head-and-shoulders.

## Logos — `logos/`

| File | Status |
| --- | --- |
| `microsoft.svg` | Real mark — the four-square logo in its exact brand colours |
| `salesforce.svg` | Real mark — official cloud outline (Font Awesome Free, CC BY 4.0) |
| `freshworks.svg` | **Placeholder** — monogram tile |
| `podrock.svg` | **Placeholder** — monogram tile |
| `xlri.svg` | **Placeholder** — monogram tile |
| `bits.svg` | **Placeholder** — monogram tile |

The placeholders are plain monogram tiles rather than hand-drawn imitations of
the real marks. To swap one in, save the official SVG over the same filename.
Keep it 24 units tall with the wordmark included, so row heights stay even.

### Two copies, on purpose

`about-me.html` has these SVGs **inlined** rather than linked, so the wordmarks
can use `currentColor` and follow the light/dark theme. An SVG loaded through
`<img>` is isolated and cannot inherit page colour — it would render black on
black in dark mode.

The files in this folder are the copies `about-me.md` links to, and they use a
fixed mid-grey that reads on both GitHub themes. **If you replace a logo, update
it in both places** — the file here and the inline copy in `about-me.html`.
