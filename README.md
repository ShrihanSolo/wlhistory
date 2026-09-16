# A history of weak gravitational lensing

A twelve-chapter illustrated history, from Newton's *Opticks* to the shear
catalogues of Euclid, Rubin and Roman. Built from a long conversation about the
field's development (`HistoryofWeakLensing.rtf`, kept here for reference) laid
into a page designed with Claude Design.

## Publishing to GitHub Pages

The site is plain static files and needs no build step.

```bash
git init
git add .
git commit -m "Weak lensing history site"
git branch -M main
git remote add origin git@github.com:<you>/<repo>.git
git push -u origin main
```

Then: **Settings → Pages → Source: Deploy from a branch → Branch `main`, folder
`/ (root)`**. It appears at `https://<you>.github.io/<repo>/` within a minute or two.

### Do not delete `.nojekyll`

GitHub Pages runs Jekyll by default, and **Jekyll silently drops directories
whose names begin with an underscore.** `_ds/` is the entire design system, so
without the empty `.nojekyll` file at the repo root the site deploys with no
styling at all and no error message. It is the one real trap here.

## What's in here

| Path | What it is |
|---|---|
| `index.html` | The whole page. This is the only file to edit. |
| `_ds/classical-*/` | The Classical design system — one stylesheet plus its tokens. |
| `support.js` | Claude Design runtime. Loads React from unpkg and mounts the page. |
| `image-slot.js` | The fillable image placeholder element. |
| `images/` | Photographs, plus `README.md` listing what each slot wants and where to find it. |
| `.nojekyll` | Required. See above. |
| `Weak Lensing History Website v2.zip` | The same page packaged for Claude Design. |
| `HistoryofWeakLensing.rtf` | Source conversation the text is drawn from. |
| `Weak Lensing History Website.zip` | The original design export, untouched. |

## Editing

**In a text editor** — `index.html` is self-contained: chapters are
`<section id="ch1">` … `<section id="ch12">`, in order, with all styling inline
so nothing is remote-controlled by a stylesheet you have to hunt for.

**In Claude Design** — open `Weak Lensing History Website v2.zip`. This is the
easier route for dropping photographs into the image slots. When you export
again, rename the `.dc.html` back to `index.html` to republish.

Colours, fonts and spacing all come from the design system's CSS variables
(`var(--color-accent-700)`, `var(--font-heading)` and so on). Taking new values
from those tokens rather than typing hex codes keeps the page consistent if the
theme ever changes.

### Running it locally

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000/>. Serve it rather than double-clicking the
file — that is how Pages will serve it, and it avoids `file://` path surprises.

The page fetches React from unpkg and the fonts from Google Fonts at load time,
so it needs a network connection to render. That is about 90 KB gzipped and the
trade for keeping the Claude Design round-trip.

## Figures

Chapters 5, 6, 11 and 12 carry drawn SVG diagrams — the signal-in-noise problem,
E-modes against B-modes, the Bullet Cluster collision geometry, and the S₈
measurements — which need no image files and are styled from the design tokens.
Everything else is an empty image slot; see `images/README.md`.
