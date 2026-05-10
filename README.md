# Homepage Hero Prototypes — FBC Huntersville

Static site presenting nine homepage hero prototypes for First Baptist Church Huntersville,
organized into three strategic directions, for leadership review and discussion.

## Local viewing

Just open `index.html` in any browser. No build step.

## GitHub Pages deployment

This folder is self-contained and deploys cleanly to GitHub Pages.

**Option A — Dedicated repo (simplest):**

```bash
cd hero-review-site
git init
git add .
git commit -m "Initial review site"
git remote add origin git@github.com:USERNAME/REPO.git
git push -u origin main
```

Then in repo Settings → Pages, set source to `main` branch, root folder.
Site will be live at `https://USERNAME.github.io/REPO/`.

**Option B — `/docs` subfolder of existing repo:**

Copy this entire folder into `docs/` of your existing repo, then in repo Settings → Pages
select source `main` branch, `/docs` folder.

The `.nojekyll` file is included so GitHub Pages serves files as-is without Jekyll processing
(important because some folder names start with letters Jekyll would otherwise filter).

## Folder structure

```
hero-review-site/
├── index.html              ← entry point (the review document)
├── assets/
│   └── logo.jpg            ← FBC Huntersville logo (used by all variants)
├── concierge/
│   ├── v1.html             ← Refined Split
│   ├── v2.html             ← Cinematic Floating Card
│   └── v3.html             ← Editorial Magazine
├── messaging/
│   ├── v1.html             ← Atmospheric Centered
│   ├── v2.html             ← Editorial Pull-Quote
│   └── v3.html             ← Bold Stacked Type
└── people/
    ├── v1.html             ← Worship Silhouette
    ├── v2.html             ← Congregation From Behind
    └── v3.html             ← Mosaic Grid
```

## Notes for production

- **Photos are placeholders.** Each variant has a "Photo direction" overlay describing what
  to commission. None of the imagery is final.
- **Masthead replicates the live Wix site** — same logo, same nav (About / Sermons / Ministry /
  Outreach / Giving), same dropdowns, same teal-on-white styling.
- **External dependencies:** Google Fonts (Montserrat, Cormorant Garamond) and Unsplash images.
  Both are CDN-loaded and require an internet connection to render fully.

## Updating

To change a variant's hero, edit the corresponding file in `concierge/`, `messaging/`, or
`people/`. All variants share the same masthead (`.wix-header` block at the top of each file)
so changing the masthead requires editing each variant — or doing a search-and-replace across
the nine files.
