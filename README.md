# graysuit.github.io

Source for **[graysuit.github.io](https://graysuit.github.io)** — the portfolio site of Syed Ibrahim Ali.

Desktop software, automation, scraping and AI integration. 200+ orders, 4.96/5.0, clients in 25+ countries.

## What's here

| Path | |
|---|---|
| `index.html` | Hero, stats bar, featured project cards |
| `pages/` | `projects` (filterable grid), `skills`, `about`, `contact` |
| `assets/js/projects.js` | **All 43 projects as one data array** — edit this to add content |
| `assets/js/main.js` | Rendering, filters, card expand, nav, scroll reveal |
| `assets/css/style.css` | The whole design system |
| `assets/img/projects/` | 33 real client screenshots |
| `cnic.html` | Earlier standalone project page, still linked from the site |

No build step, no framework, no dependencies. Clone, edit, push.

## Deploying

Pages serves `main` / root. Push and it goes live.

```powershell
git add .
git commit -m "Update site"
git push origin main
```

The site is served from the **domain root**, so every `canonical`, `og:url` and JSON-LD `url` is written as `https://graysuit.github.io/...` with no path prefix. If the site ever moves into a subfolder, those references and `sitemap.xml` have to change with it.

## Adding a project

Append an object to `PROJECTS` in `assets/js/projects.js`. The schema, the anonymisation rule for client names, and the screenshot workflow are documented in [`README.site.md`](README.site.md).

## Two repos, two jobs

- **`graysuit/graysuit`** — the GitHub *profile* repo. Holds the profile README that renders on [github.com/graysuit](https://github.com/graysuit).
- **`graysuit/graysuit.github.io`** — this repo. Holds the site, served at the domain root.
