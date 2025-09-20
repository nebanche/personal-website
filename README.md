# Jekyll Ultra‑Lean Starter

A tiny, Harry Roberts–style, ultra‑performant Jekyll starter focused on text‑first content, minimal CSS, and zero/near‑zero JS.

## Quick start

```bash
bundle install
bundle exec jekyll serve
```

Then visit http://127.0.0.1:4000

## Deploy

- **GitHub Pages**: Enable Pages for this repo (build from `GitHub Actions` or `/docs` if you prefer).  
- **Cloudflare**: Point your domain to Cloudflare and proxy (orange cloud). Turn on Brotli, HTTP/2+3, Auto‑Minify (HTML/CSS/JS). Add caching rules: long cache for `/assets/*`, bypass for HTML.

## Performance budget

- LCP ≤ 1.5s (mid‑range mobile), CLS ≤ 0.01, INP ≤ 200ms  
- Requests ≤ 20, transfer size ≤ 200KB first view  
- CSS < 10KB, JS < 5KB (prefer 0 for content pages)

## Folder layout

- `_layouts/` — base/page/post layouts
- `_includes/` — partials (head, header, footer)
- `_sass/` — ITCSS layers (settings → utilities)
- `assets/css/` — entrypoint `site.scss`
- `assets/js/` — optional progressive enhancement
- `pages/` — static pages (About, Contact)

## License

MIT
