# Uday Pratap — Data Science Portfolio

A simple, polished, single-file personal portfolio built with vanilla HTML/CSS/JS. The site showcases education, skills, featured Kaggle projects (with inline previews/links), and contact options. It’s designed to be fast, responsive, and recruiter-friendly with subtle highlights and dark-mode support.

## Features

- Fixed glass-style top bar with touch-friendly horizontal nav
- One-click “Back to top” via profile/name (clickable, keyboard accessible)
- Responsive layout with dark and light themes
- Subtle highlights for key credentials (IIT Madras) and skills
- Featured projects with Kaggle notebook links and dynamic preview iframes
- Social sidebar docked left; docks to a mobile-friendly bar on small screens
- Contact form powered by Formspree
- Basic SEO: meta description, OpenGraph tags, and JSON-LD Person schema

## Project Structure

```
mysite/
├── index.html           # Single-page app with inline CSS/JS
├── README.md            # This guide
└── (optional assets)
```

Everything lives in `index.html` to keep hosting trivial (GitHub Pages, Netlify, etc.).

## Getting Started

1. Open `index.html` in any modern browser. No build step is required.
2. To develop locally, use a static server (optional) for clean URLs.

### Quick local preview (optional)

- Python 3: `python -m http.server 8000`
- Node: `npx serve .`

Then visit http://localhost:8000

## Customization

- Name, location, email: at the top section (`id="top"`).
- Social links: in the left `.social-sidebar` nav.
- Sections: edit or reorder `Education`, `Skills`, `Certifications`, `Featured Projects`, `Portfolio`, `Extracurricular`, `Contact`.
- Highlights: tweak `.edu-highlight` and `.skill-highlight` in the CSS for emphasis colors.
- Dark mode: handled by a simple toggle and `prefers-color-scheme` listener.

## Featured Projects

Each featured project includes a short summary and a link to the full Kaggle notebook. If Kaggle blocks iframes in your browser, keep the link and optionally add a screenshot thumbnail.

Recommended on-page additions to improve recruiter signal:
- Key outcomes for each project (e.g., RMSE/MAE, ROC-AUC, F1, recall@precision)
- One line on data size and validation approach (e.g., 5-fold CV)

## Contact Form (Formspree)

- Replace the `action` URL with your own Formspree endpoint to receive submissions.
- Form fields already include browser validation attributes.

## SEO & Social

- Meta description, OpenGraph tags, favicon, and Person schema are included.
- Update `og:url`, `og:image`, and `sameAs` links to your canonical site URL and avatar.

## Accessibility

- Keyboard-accessible topbar identity (Enter/Space to go to top)
- Aria labels on social links
- Sufficient contrast for links in both themes

## Deployment

- GitHub Pages: push the repo and enable Pages for the `main` branch (root).
- Netlify/Vercel: drag-drop or point to the repo; no build required.

## Troubleshooting

- Kaggle iframes not loading: use direct links; add screenshots as inline previews.
- Topbar overlaps on tiny screens: content uses `scroll-margin-top`; verify media queries.
- Dark mode not toggling: ensure the toggle button is present and JS runs (no CSP blocking inline scripts).

## Roadmap / Nice-to-haves

- Add a small “Highlights” row under the intro (chips with IIT Madras, core stack, focus areas)
- Convert featured projects to cards with metrics shown inline
- Replace Google Sheet portfolio embed with a fast list of links + tags
- Add basic analytics (e.g., Plausible/GA4)

## License

MIT — see `LICENSE` if you add one to the repo.
