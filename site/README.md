# ReyGris website

Public site built on **[Escape Velocity](https://html5up.net/escape-velocity)** by HTML5 UP, customized with ReyGris branding and content.

## Preview locally

```bash
cd site
python3 -m http.server 8080
```

Open [http://localhost:8080](http://localhost:8080).

## Deploy

Upload the entire `site/` folder to your static host. The entry point is **`index.html`**.

| Host | Publish directory |
|------|-------------------|
| Netlify / Vercel / Cloudflare Pages | `site` |
| GitHub Pages | `site` (or copy contents to root) |
| Any web server | contents of `site/` → web root |

Point your domain DNS to the host and enable HTTPS.

## Structure

| Path | Purpose |
|------|---------|
| `index.html` | Homepage |
| `assets/css/main.css` | Escape Velocity base styles |
| `assets/css/reygris.css` | ReyGris brand overrides (colors, header) |
| `assets/js/` | Template scripts (nav, mobile menu) |
| `images/` | ReyGris SVG artwork (banner, hero, cards) |

## Brand theme

ReyGris colors replace the template's coral accent:

- **Kingbird Slate** `#5C6670` — intro band, accents
- **Territory Charcoal** `#2D3748` — headings, footer, dark buttons
- **Crown Gold** `#B8956A` — primary buttons, highlights

## Credits

- Template: [Escape Velocity](https://html5up.net/escape-velocity) by HTML5 UP (CCA 3.0)
- Icons: Font Awesome (included with template)
- ReyGris content, SVG artwork, and theme: ReyGris Technologies

Update contact email in `index.html` (`hello@reygris.com`) before going live.

## Documentation

Company standards and internal docs remain in `/docs` as Markdown. This site is the public-facing homepage.
