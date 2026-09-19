# Lheianne & Kyle — wedding site

Static site. No build step, no dependencies, no third-party requests.
Edit `index.html`, commit, push. GitHub Pages redeploys in under a minute.

## Before it goes live

1. **`SITE_URL`** — two occurrences in the `<head>` of `index.html`. Replace both
   with the real domain (no trailing slash, e.g. `lheianneandkyle.com`).
   Link previews in WhatsApp and iMessage need an absolute URL or they show no image.
2. **`CONFIG.form`** — near the top of the `<script>`. Paste the Google Form's
   `formResponse` URL and the five `entry.` ids.

## Things worth knowing

- **`robots.txt` and the `noindex` meta tag** keep the site out of Google. Delete
  both if you would rather guests could search for it by name.
- **Photos** live in `photos/` at four widths each, as WebP and JPEG. To swap one,
  replace all eight files for that number, keeping the names. The `srcset` in
  `index.html` does not need touching.
- **Fonts** are self-hosted. Simple Serenity and the Latin cut of Gotu are inlined
  in the CSS; the extended Gotu subsets sit in `fonts/` and are only fetched if a
  guest types a name that needs them.
- **`.nojekyll`** stops GitHub running the files through Jekyll. Leave it there.

## Weight

| | |
|---|---|
| First paint | 179 KB (the whole page, fonts included) |
| Gallery, desktop | +283 KB |
| Gallery, phone at 3x | +1.1 MB, and only once you scroll to it |
