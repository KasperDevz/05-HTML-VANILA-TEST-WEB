# Draft — Course Platform Landing Site

A vanilla HTML landing site for **Draft**, an online course platform. Every page is built as a plain `.html` file styled with [Tailwind CSS](https://tailwindcss.com/) via the CDN build — no bundler, no `npm install`, no build step. Clone it and open a file in a browser.

## Preview

| Page | Description |
| --- | --- |
| [`src/index.html`](src/index.html) | Landing page — hero, course spec highlights, CTA banner |
| [`src/courses.html`](src/courses.html) | Course catalog — full course grid with duration, level, and price |

## Tech Stack

- **HTML5** — no framework, no JSX, no templating
- **[Tailwind CSS](https://tailwindcss.com/)** — loaded via `cdn.tailwindcss.com`, configured inline per page
- **Google Fonts** — [Syne](https://fonts.google.com/specimen/Syne) (display), [Inter](https://fonts.google.com/specimen/Inter) (body), [IBM Plex Mono](https://fonts.google.com/specimen/IBM+Plex+Mono) (labels/annotations)

## Design System

The site follows a "blueprint" visual theme: a navy background with a faint drafting grid, corner registration marks, and mono-font spec annotations, echoing an engineering drawing.

| Token | Value | Usage |
| --- | --- | --- |
| `navy` | `#16233D` | Page background |
| `navy2` | `#1D3050` | Hover state on dark surfaces |
| `paper` | `#ECE8DC` | Reserved for light surfaces |
| `amber` | `#E8963C` | Primary accent, CTAs |
| `line` | `#4C6D9C` | Borders, grid lines |
| `ink` | `#E9ECF2` | Primary text on dark background |
| `slate` | `#8CA0BE` | Secondary/muted text |

Color and font tokens are defined once per page inside an inline `tailwind.config` `<script>` block, so each page stays fully self-contained.

## Project Structure

```
.
├── src/
│   ├── index.html       # Landing page
│   └── courses.html     # Course catalog page
├── CHANGELOG.md          # Version history
└── README.md
```

## Getting Started

No installation required.

```bash
git clone https://github.com/KasperDevz/05-HTML-VANILA-TEST-WEB.git
cd 05-HTML-VANILA-TEST-WEB
open src/index.html   # macOS; use `start` on Windows or `xdg-open` on Linux
```

Or serve it locally with any static server, e.g.:

```bash
npx serve src
```

## Adding a Page

1. Copy the `<head>` block (fonts + `tailwind.config`) from an existing page under `src/` so the color and font tokens stay consistent.
2. Reuse the shared navbar and footer markup.
3. Link the new page from the nav in `src/index.html` and `src/courses.html`.

## Versioning

Changes are tracked in [`CHANGELOG.md`](CHANGELOG.md) following [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and [Semantic Versioning](https://semver.org/).

## License

No license specified yet.
