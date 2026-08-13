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
├── projects/                     # Three complete, tested portfolio projects ↓
│   ├── taskflow/                 # Kanban app — Node/Express/SQLite, 22 Jest tests
│   ├── shoplite/                 # E-commerce API — FastAPI/SQLAlchemy, 22 pytest tests
│   └── devmetrics/               # GitHub analytics — zero-dep JS + SVG charts
├── scripts/split-projects.sh     # Promote each project to its own GitHub repo
└── .github/workflows/            # deploy.yml (Pages) + ci.yml (runs all test suites)
```

## The projects

Each folder in `projects/` is a complete, self-contained application with its own README, test suite, `.gitignore`, and CI workflow:

| Project | Stack | Tests | Highlights |
|---|---|---|---|
| **TaskFlow** | Node.js, Express, SQLite | 22 (Jest + Supertest) | JWT auth, ownership enforcement, transactional drag-and-drop reordering |
| **ShopLite** | Python, FastAPI, SQLAlchemy 2.0 | 22 (pytest) | Stock control, immutable order snapshots, money as integer cents |
| **DevMetrics** | Vanilla JS, GitHub REST API | browser-verified | Hand-rolled SVG charts, 202-retry handling, deep links; live on this site's Pages deploy |

**To give each project its own GitHub repository** (recommended — separate repos look better on a profile): install the [GitHub CLI](https://cli.github.com), run `gh auth login`, then:

```bash
./scripts/split-projects.sh
```

Each new repo's CI goes green on the first push. Afterwards, point the portfolio's `Code ↗` links at the new repo URLs.

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
