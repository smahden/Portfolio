# Mahden Saleh — Software Engineer Portfolio

A fast, responsive, accessible portfolio site built with **plain HTML, CSS, and JavaScript** — no frameworks, no build step, nothing to install. It deploys automatically to **GitHub Pages** on every push.

**Live site:** `https://smahden.github.io/portfolio/` *(available after enabling GitHub Pages — see below)*

## Features

- 🌗 Dark/light theme with system-preference detection and persistence
- 📱 Fully responsive (mobile menu, fluid type, grid layouts)
- ♿ Accessible: semantic HTML, skip link, keyboard navigation, reduced-motion support
- ⚡ Zero dependencies — loads instantly, easy to maintain
- 🎬 Subtle scroll-reveal animations and a typed hero effect
- 🚀 CI/CD: auto-deploys to GitHub Pages via GitHub Actions

## Project structure

```
├── index.html                    # All page content (edit your info here)
├── styles.css                    # Theme, layout, responsive styles
├── script.js                     # Theme toggle, mobile menu, animations
├── resume/
│   └── Mahden_Saleh_Resume.md    # Downloadable résumé (edit + export to PDF)
└── .github/workflows/deploy.yml  # Auto-deploy to GitHub Pages
```

## Getting it live (one-time setup)

1. Merge this branch into your default branch (`main`).
2. On GitHub, go to **Settings → Pages** and set **Source** to **GitHub Actions**.
3. Push (or re-run the workflow) — the site publishes to `https://smahden.github.io/portfolio/`.

## Customization checklist

Everything is plain HTML — search for these in `index.html` and make them yours:

- [ ] **Experience & Education** — replace the placeholder company/university names and bullet points with your real history (also in `resume/Mahden_Saleh_Resume.md`).
- [ ] **Projects** — swap the sample projects for your real repositories; point each card's `Code ↗` link at the actual repo, and add a `Live ↗` link if deployed.
- [ ] **LinkedIn URL** — update `linkedin.com/in/mahden-saleh` if your profile handle differs.
- [ ] **About / Quick facts** — adjust location, availability, and the tech list to match you.
- [ ] **Résumé** — fill in real details, export to PDF, and drop it in `resume/` (update the hero button's `href` if you switch to PDF).

## Local preview

No build step — just open the file, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```
