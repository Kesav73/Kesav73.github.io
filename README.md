# kesavpatneedi.in

Personal portfolio site — static HTML/CSS/JS, no build step, no dependencies.

## Structure

```
index.html              single page — all content lives here
assets/css/style.css    design tokens, layout, light/dark themes
assets/js/main.js       theme toggle, scroll reveals
assets/img/             cut-out portrait (webp + png fallback), og-cover.png link preview
data/                   résumé PDF and source photo (git-ignored, never deployed)
```

## Local preview

```bash
python -m http.server 5173
```

Then open <http://localhost:5173>.

## Editing content

Everything is in `index.html` — there is no CMS or data file. Sections are marked
with `<!-- ===== NAME ===== -->` comments.

The headline numbers under the hero and the stat boxes on each job repeat figures
from the bullet points, so update both when a number changes. The project
architecture diagrams are inline SVG next to each project's text.

## Résumé

The résumé buttons link to a Google Drive file, not a file in this repo (the PDF
contains a phone number). To update it, replace the file in Drive, or change the
Drive URL in `index.html` (it appears three times).

## Regenerating the portrait

The hero image is `data/Passport.png` with the background removed (rembg),
exported as a 760px WebP with a 520px PNG fallback. `assets/img/og-cover.png` is a
1200x630 screenshot of a small HTML card using the same portrait and fonts.
