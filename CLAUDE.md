# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

Single-page HTML brief/onboarding form for Iron Block Módulos, built and maintained by **cami.clipp**. No build tools, no framework — pure HTML/CSS/vanilla JS.

## Files

- `brief-iron-block.html` — source of truth, always edit this
- `index.html` — copy of the above, required for GitHub Pages (keep in sync)
- `cami-clipp-brand.md` — brand guidelines (colors, typography, logo, tone)

After any edit: `cp brief-iron-block.html index.html && git add -A && git commit -m "..." && git push`

## Deployment

GitHub Pages from `master` branch → **https://cami-clipp.github.io/brief-iron-block/**

Git remote uses token auth embedded in the remote URL. If push fails, reset with:
```
git remote set-url origin https://<token>@github.com/cami-clipp/brief-iron-block.git
```

## Form submission

Formspree endpoint: `https://formspree.io/f/myklqyow` — responses go to aguilar1601cami@gmail.com.
Submission is handled via `fetch()` in vanilla JS (no page redirect).

## Brand identity (cami.clipp)

Always follow `cami-clipp-brand.md`. Key rules:
- **Colors:** Ladrillo `#B5432A` · Negro `#1A1A1A` · Crema `#FAF6F1` · Lino `#EDE3D6` · Gris cálido `#7A706B`
- **Fonts:** Playfair Display (titles, bold/italic alternating) + DM Sans (UI/body)
- **No:** gradients, shadows, border-radius on buttons, more than 3 colors per section
- Input style: `border: none; border-bottom: 2px solid #B5432A; background: transparent`

## Print/PDF

`@page { margin: 0 }` + `print-color-adjust: exact` forces background colors. User must enable **"Gráficos de fondo"** in Chrome print dialog.
