# hussien4321.github.io

Personal portfolio — served by GitHub Pages at **https://hussien4321.github.io**

## Layout

```
index.html        the whole site: markup, styles and script in one file
assets/*.webp     screenshots, resized and compressed (324 KB total)
.nojekyll         tells Pages to serve the files as-is, no Jekyll build
```

No build step, no dependencies. Open `index.html` in a browser to preview locally.

## Publishing

For a `<username>.github.io` repository, GitHub Pages serves the default branch
automatically — push to `main` and the site updates within a minute.

If it doesn't appear: Settings → Pages → Source → *Deploy from a branch* → `main` / `/ (root)`.

## Editing

Everything lives in `index.html`:

- **Colours** are CSS custom properties at the top (`:root`). The site is dark-only,
  so the palette is defined once and changing an accent means changing one value.
- **Each project** is one `<article class="entry">`. Copy one to add a sixth: the
  number goes in `.rail`, the summary in `.lede`, the detail bullets in `.notes`, the
  grouped stack in `.built` and the links in `.links`.
- **Two image layouts.** A wide screenshot uses `.screens.mid` (or `.screens.pair` for
  laptop + phone) and sits above the text; a tall phone screenshot goes in
  `.entry-main` so the text sits beside it instead of leaving an empty column
  (`.entry-main.compact` for a smaller one). Small secondary shots go in `.strip`,
  which scrolls sideways when it runs out of room.
- **Images** should be WebP and no wider than they are displayed — the page loads in
  well under half a megabyte, which is most of why it feels instant.

## Fonts

Bricolage Grotesque (display), Spline Sans (body) and JetBrains Mono (data), loaded
from Google Fonts. Each has a real fallback stack, so the page still sets correctly
if the request fails.
