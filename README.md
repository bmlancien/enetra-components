# Enetra Prototype

Static HTML/Tailwind prototype for the Enetra application UI.

## Getting started

**Prerequisites:** Node.js 18+

```bash
npm install
npm run dev
```

The dev server starts at `http://localhost:5173` (or the next available port).

### Other commands

```bash
npm run build    # production build → dist/
npm run preview  # preview the production build locally
```

## Pages

| File | Description |
|---|---|
| `pages/landing.html` | Landing page |
| `pages/login.html` | Auth — sign in |
| `rpages/egister.html` | Auth — create account |
| `pages/forgot-password.html` | Auth — request password reset |
| `pages/reset-password.html` | Auth — set new password |
| `pages/projects.html` | Project list |
| `pages/project-overview.html` | Single project overview |
| `pages/ergebnisse.html` | Scenario results |
| `pages/szenarienvergleich.html` | Side-by-side scenario comparison |
| `pages/einstellungen.html` | Settings |
| `pages/user-rechte.html` | User rights / permissions |
| `index.html` | Entry point |

## Components

Reusable Cotton components live in `components/`.

| Component | Description |
|---|---|
| `toolbar` | Section toolbar: search, sort dropdown, card/table toggle, primary action button |
| `flaechen-uebersicht` | Leaflet map card with metric dropdown and a side panel slot; supports scenario-driven polygon recoloring |

## Tech stack

- [Vite](https://vitejs.dev/) – dev server and build tool
- [Tailwind CSS v4](https://tailwindcss.com/) – utility-first CSS
- [Alpine.js](https://alpinejs.dev/) – lightweight reactivity (loaded via CDN)
- [Lucide Icons](https://lucide.dev/) – icon set (loaded via CDN)
- [Leaflet](https://leafletjs.com/) – interactive maps (loaded via CDN, used on `ergebnisse` and `szenarienvergleich`)
- [ECharts](https://echarts.apache.org/) – charts (loaded via CDN, used on `ergebnisse`)
- [Inter](https://fonts.google.com/specimen/Inter) – typeface (loaded via Google Fonts)

## Third-party licenses

### Lucide Icons
ISC License — Copyright (c) 2022 Lucide Contributors  
https://github.com/lucide-icons/lucide/blob/main/LICENSE

### Tailwind CSS
MIT License — Copyright (c) Tailwind Labs, Inc.  
https://github.com/tailwindlabs/tailwindcss/blob/next/LICENSE

### Vite
MIT License — Copyright (c) 2019-present, VoidZero Inc. & Vite contributors  
https://github.com/vitejs/vite/blob/main/LICENSE

### Alpine.js
MIT License — Copyright (c) 2019-present Caleb Porzio & contributors  
https://github.com/alpinejs/alpine/blob/main/LICENSE.md

### Leaflet
BSD 2-Clause License — Copyright (c) 2010–2024, Vladimir Agafonkin  
https://github.com/Leaflet/Leaflet/blob/main/LICENSE

### ECharts
Apache License 2.0 — Copyright (c) Apache Software Foundation  
https://github.com/apache/echarts/blob/master/LICENSE

### Inter Typeface
SIL Open Font License 1.1 — Copyright (c) 2016 The Inter Project Authors  
https://github.com/rsms/inter/blob/master/LICENSE.txt
