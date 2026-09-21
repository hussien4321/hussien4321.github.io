# hussien4321.github.io

Personal portfolio — served by GitHub Pages at **https://hussien4321.github.io**

## Layout

```
index.html        the whole site: markup, styles and script in one file
assets/*.webp     screenshots, resized and compressed (356 KB total)
.nojekyll         tells Pages to serve the files as-is, no Jekyll build
```

No build step, no dependencies. Open `index.html` in a browser to preview locally.

## Publishing

For a `<username>.github.io` repository, GitHub Pages serves the default branch
automatically — push to `main` and the site updates within a minute.

If it doesn't appear: Settings → Pages → Source → *Deploy from a branch* → `main` / `/ (root)`.

## Editing

Everything lives in `index.html`:

- **Colours** are CSS custom properties at the top (`:root`). The light palette is
  defined once; the dark theme only redefines the same names, so changing an accent
  means changing two values.
- **Each project** is one `<article class="entry">`. Copy one to add a sixth: the
  year goes in `.rail`, the summary in `.lede`, the detail bullets in `.notes`, the
  hard numbers in `.facts`, the stack in `.stack` and the links in `.links`.
- **Two image layouts.** A wide screenshot uses `.screens.wide` / `.screens.mid` and
  sits above the text; a tall phone screenshot goes in `.entry-main` so the text sits
  beside it instead of leaving an empty column. Small secondary shots go in `.strip`.
- **Images** should be WebP and no wider than they are displayed — the page loads in
  well under half a megabyte, which is most of why it feels instant.

## Fonts

Bricolage Grotesque (display), Spline Sans (body) and JetBrains Mono (data), loaded
from Google Fonts. Each has a real fallback stack, so the page still sets correctly
if the request fails.
