# Uday Pratap — Data Science Portfolio

A clean, production-ready single-page portfolio built with vanilla HTML/CSS/JS. Designed for recruiters and employers, it showcases education credentials (IIT Madras PG Diploma), technical skills, three featured Kaggle projects with notebook previews, extracurricular leadership, and contact options. The site is fast, fully responsive, and search-engine optimized.

## Features

- **Fixed glass-style top bar** with touch-friendly horizontal nav and smooth "back to top" on profile/name click (keyboard accessible)
- **Dark/light theme** toggle respecting system preference
- **Subtle highlights** for key credentials (IIT Madras education, core skills) in both themes
- **Featured projects** with Kaggle notebook embeds/links (NLP, regression, classification)
- **Social sidebar** docked left (GitHub, LinkedIn, YouTube, Kaggle, Instagram); docks to a centered mobile bar on small screens
- **Contact form** powered by Formspree with browser validation
- **SEO-ready**: meta description, OpenGraph tags, JSON-LD Person schema, robots.txt, sitemap.xml, and 404 page
- **Favicon support**: SVG + ICO fallback for modern and legacy browsers

## Project Structure

```
mysite/
├── index.html           # Single-page app with inline CSS/JS
├── 404.html             # Friendly not-found page
├── robots.txt           # Crawler permissions + sitemap link
├── sitemap.xml          # SEO sitemap
├── favicon.svg          # Scalable favicon (modern browsers)
├── favicon.ico          # Fallback icon (legacy browsers)
└── README.md            # This guide
```

Everything is self-contained in `index.html` for trivial hosting (GitHub Pages, Netlify, Vercel, etc.). No build step required.

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

### GitHub Pages (recommended)
1. Push the repo to GitHub.
2. In Settings → Pages, set source to `main` branch (root).
3. Your site will be live at `https://yourusername.github.io/mysite/` within minutes.
4. Update `robots.txt` and `sitemap.xml` with your live URL.

### Netlify / Vercel
- Drag-drop the folder or connect the repo.
- No build command needed; serve the root directory.
- Custom domain: follow platform docs to add a `CNAME` record.

## Files & Configuration

- **robots.txt**: Allows all crawlers; points to `sitemap.xml`. Update the sitemap URL if using a custom domain.
- **sitemap.xml**: Lists your main page. Update the `<loc>` URL and `<lastmod>` date when making significant changes.
- **404.html**: Friendly error page with auto-redirect (5s) and a "Go to Home" button.
- **favicon.svg / favicon.ico**: Brand icons. Replace with your own (tools like [favicon.io](https://favicon.io/) can help).
- **Formspree action URL**: In `index.html`, swap `https://formspree.io/f/mblzbdnz` with your endpoint.
- **OpenGraph / JSON-LD**: Update `og:url`, `og:image`, and `sameAs` links in the `<head>` to your live site and socials.

## Troubleshooting

- Kaggle iframes not loading: use direct links; add screenshots as inline previews.
- Topbar overlaps on tiny screens: content uses `scroll-margin-top`; verify media queries.
- Dark mode not toggling: ensure the toggle button is present and JS runs (no CSP blocking inline scripts).

## Roadmap / Nice-to-haves

- Add a small "Highlights" row under the intro (chips: IIT Madras, core stack, focus areas)
- Convert featured projects to cards with inline metrics (RMSE, ROC-AUC, F1)
- Replace Google Sheet portfolio embed with a fast link list + tags
- Add basic analytics (e.g., Plausible, GA4)
- Custom domain + HTTPS
- Performance audit (Lighthouse score 95+)

## Contributing

Suggestions and improvements are welcome! Open an issue or PR if you spot something that could be better.

## License

MIT — you're free to fork and adapt this for your own portfolio. See `LICENSE` if added to the repo.

---

**Live site**: [https://udayprattap.github.io/mysite/](https://udayprattap.github.io/mysite/) (update with your actual URL)  
**Author**: Uday Pratap  
**Contact**: udayprattap@gmail.com | [LinkedIn](https://www.linkedin.com/in/udayprattap/)
