# kesavpatneedi.in

Personal portfolio site — static HTML/CSS/JS, no build step, no dependencies.

## Structure

```
index.html              single page — all content lives here
assets/css/style.css    design tokens, layout, light/dark themes
assets/js/main.js       theme toggle, scroll reveals
assets/img/             web-optimised portrait (webp + png fallback)
data/                   résumé PDF served by the download button
_source/                original full-size photos (git-ignored)
```

## Local preview

```bash
python -m http.server 5173
```

Then open <http://localhost:5173>.

## Editing content

Everything is in `index.html` — there is no CMS or data file. Sections are marked
with `<!-- ===== NAME ===== -->` comments.

When updating the résumé, replace `data/Kesav_Resume_Latest.pdf`; the download
button renames it to `Kesav_Patneedi_Resume.pdf` on the way out.

## Regenerating the portrait

The hero image is a background-removed PNG, resized to 640px and exported as
WebP with a PNG fallback. Source lives in `_source/`.
