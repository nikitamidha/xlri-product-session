# assets

Drop the portrait here as **`nikita.jpg`**.

Both `about-me.html` and `about-me.md` point at `assets/nikita.jpg`. The HTML
page falls back to an "NM" monogram if the file is missing, so it still renders
cleanly before the photo lands.

Any roughly portrait-ratio crop works — the page uses `object-fit: cover` with
the focal point set high (`object-position: 50% 22%`) so a head-and-shoulders
shot sits correctly. Around 800×1000px is plenty.
