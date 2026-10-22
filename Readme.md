# Personal Portfolio

> https://giridevspace.netlify.app/

Static portfolio site for **Sunil Giri**, AI/ML Engineer. Plain HTML, CSS and jQuery — **no build step, no dependencies to install**. Push the files and they are served as-is.

## Deploying (GitHub Pages)

1. Push to `main`.
2. **Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)`**.
3. Site is served at `https://<user>.github.io/<repo>/`.

All asset paths are relative, so the site works at a domain root or in a project sub-path. `.nojekyll` disables Jekyll processing so every file is published verbatim.

## Structure

```
index.html              Single-page site: hero, about, education, experience,
                        skills, portfolio grid, contact
assets/
  css/style.css         All custom styling and design tokens
  js/main.js            Motion layer: section reveal, nav, isotope filters, venobox
  img/                  Profile, education, certification and project imagery
  vendor/               Vendored front-end libraries (see below)
projects/               Standalone project detail pages, opened in a Venobox iframe
favicon.png
```

## Vendored libraries

Committed rather than CDN-loaded, so the site has no third-party runtime dependency.

| Library | Version | Used for |
| --- | --- | --- |
| Bootstrap | 4.4.1 | Grid and layout |
| jQuery | 3.x | DOM and event handling |
| Isotope | 3.0.6 | Portfolio category filtering |
| Venobox | — | Project detail lightbox / iframe |
| Typed.js | — | Hero typing animation |
| Boxicons, Icofont, Remixicon | — | Icon fonts (woff2 + woff only) |

## Editing

- **Content** — edit `index.html` directly; each section is a commented `<section>`.
- **Theme** — colours, radii, fonts and shadows are CSS variables in the `:root` block of `assets/css/style.css`.
- **New project** — add an HTML file to `projects/` and a card in the `#portfolio` section of `index.html`.
