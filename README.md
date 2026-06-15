# JNV School Website

Official website for **Jawahar Navodaya Vidyalaya**, a residential co-educational school under the Navodaya Vidyalaya Samiti. Built with [Astro](https://astro.build) — a static site generator delivering fast, SEO-friendly pages with zero JavaScript overhead.

## Tech Stack

- **Framework:** [Astro](https://astro.build) v6 — static site generation (SSG)
- **Styling:** Plain CSS with custom properties (design tokens)
- **Language:** JavaScript (`.astro` components)
- **Deployment:** Static HTML output in `dist/`

## Pages

| Route | Description |
|---|---|
| `/` | Home — hero, stats, about preview, features, CTA |
| `/about` | School history, mission/vision/values, principal's message |
| `/academics` | Curriculum overview, academic programs, exam info |
| `/teaching-staff` | Faculty listing table with qualifications |
| `/contact` | Contact details, inquiry form (Netlify-ready) |

## Design System

The UI uses CSS custom properties for a consistent, themeable design. Colors switch automatically in dark mode via `[data-theme="dark"]`.

### Color Palette

| Token | Light | Dark |
|---|---|---|
| `--brand-navy` | `#0F172A` | `#0F172A` |
| `--brand-royal` | `#2563EB` | `#60A5FA` |
| `--brand-sky` | `#60A5FA` | `#93BBFC` |
| `--brand-gold` | `#F59E0B` | `#FBBF24` |

### Shadows

- `--shadow-sm` — subtle card depth
- `--shadow-md` — elevated cards
- `--shadow-lg` — hover state
- `--shadow-xl` — images, modals

### Gradients

- `--gradient-primary` — `#2563EB` to `#3B82F6`
- `--gradient-soft` — `#EEF6FF` to `#DBEAFE`
- `--hero-overlay` — navy-to-royal gradient

All tokens defined in `src/layouts/Layout.astro`.

## Getting Started

```bash
# Install dependencies
npm install

# Start dev server at localhost:4321
npm run dev

# Build for production (outputs to dist/)
npm run build

# Preview the production build
npm run preview
```

## Project Structure

```
src/
├── components/
│   ├── Footer.astro
│   ├── Navbar.astro
│   └── ThemeToggle.astro
├── layouts/
│   └── Layout.astro     # Global shell, SEO meta, CSS variables
├── pages/
│   ├── index.astro       # Homepage
│   ├── about.astro
│   ├── academics.astro
│   ├── teaching-staff.astro
│   └── contact.astro
├── assets/               # (reserved for icons, images)
└── images/               # Static images (referenced in pages)
```

## Deployment

Build produces a fully static site in `dist/` — deployable to Netlify, Vercel, Cloudflare Pages, or any static host. The contact form includes `netlify` attribute for Netlify Forms integration.
