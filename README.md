# ReyGris

**Documentation hub for ReyGris Technologies** — standards, vision, mission, brand, and operating principles.

ReyGris is named for the Gray Kingbird (*Tyrannus dominicensis*), a bird native to the Caribbean and symbolic of home, vigilance, and purposeful leadership. This repository is the single source of truth for how we describe ourselves and how we work.

## Repository structure

| Path | Description |
|------|-------------|
| [docs/about.md](docs/about.md) | Origin story and what ReyGris stands for |
| [docs/vision-mission.md](docs/vision-mission.md) | Vision, mission, and north-star principles |
| [docs/values.md](docs/values.md) | Core values and behavioral expectations |
| [docs/brand.md](docs/brand.md) | Brand identity, voice, and visual guidelines |
| [docs/goals.md](docs/goals.md) | Strategic goals and success metrics |
| [docs/standards/](docs/standards/) | Operational and technical standards |
| [site/](site/) | **Public website** — Escape Velocity template, ReyGris-branded |

## Public website

The `site/` folder is the publishable homepage, built on [Escape Velocity](https://html5up.net/escape-velocity) (HTML5 UP) with ReyGris content, colors, and SVG artwork.

```bash
cd site && python3 -m http.server 8080
```

Deploy the `site/` folder to your domain — entry point is `index.html`. See [site/README.md](site/README.md).

## Contributing

Update markdown in `docs/` first, then mirror key changes in `site/index.html` so the live site stays in sync.
