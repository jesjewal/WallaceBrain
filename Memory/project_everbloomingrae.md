---
name: EverBloomingRae Website
description: Live Astro/Netlify website for Maria Rae's floral preservation business — fully built and deployed
type: project
---

Jesse built a full website for his friend **Maria Rae**'s floral preservation business, **EverBloomingRae**.

**Why:** She had no standalone site — only Instagram and a Linktree.

**How to apply:** Site is live and actively maintained. Always preview locally before deploying.

## Business
- Floral preservation — wedding bouquets, memorial flowers, custom shadow box keepsakes
- Instagram: https://www.instagram.com/everbloomingrae/
- TikTok: https://tr.ee/BZyIRvzWrb
- Contact: everbloomingrae@gmail.com

## Stack
- **Framework:** Astro (v6.3.1), static output
- **Styling:** Custom CSS (no Tailwind), design system based on Stitch "Petal & Heirloom / Eternal Spring"
- **Fonts:** Cormorant Garamond (display/serif) + Montserrat (UI/sans), loaded via `<link>` in Base.astro
- **Hosting:** Netlify — https://everbloomingrae.netlify.app
- **Repo:** https://github.com/jesjewal/everbloomingrae (private)
- **Local path:** `/Users/wallace/Projects/everbloomingrae/`

## Design System
- **Primary color:** `#6f2434` deep wine rose
- **Surfaces:** Semi-transparent warm creams over a fixed illustrated texture background (`/images/hero-texture.png`, opacity 0.13)
- **Fonts:** Cormorant Garamond for headlines/eyebrows, Montserrat for body/buttons/labels
- **Buttons:** Pill shape (`border-radius: 9999px`), 13px / weight 500 / 0.055em tracking / uppercase
- **Eyebrows/labels:** Cormorant Garamond roman, 12px, uppercase, 0.22em tracking
- **Nav links:** Montserrat 14px, weight 500, normal case
- **Design tokens in:** `src/styles/global.css`

## Pages
- `/` — Homepage: hero carousel (5 shadow box images, 3.5s fade), bouquet intro, keepsake grid, process steps, final CTA
- `/services` — Service offerings with pricing
- `/process` — How it works, step-by-step detail
- `/gallery` — Masonry grid (currently using shadow box product photos as placeholders)
- `/about` — Maria's story
- `/faq` — Accordion FAQ
- `/contact` — Contact form (Netlify Forms, submissions go to Netlify dashboard) + social links
- `/invest` — Pricing/investment page

## Key Implementation Notes
- Hero: two-column split on desktop (text left, framed rotating carousel right), single column on mobile (image on top)
- Carousel: CSS `position: absolute` stacked images, JS `setInterval` 3500ms, `opacity` transition 1s
- Texture: `position: fixed` div in Base.astro, `z-index: 0`, `opacity: 0.13`
- Surfaces use rgba() alpha so texture shows through all sections evenly
- Solid `background: #ffffff` on image containers so PNG transparency doesn't expose texture
- Mobile drawer nav: solid `#fff8f5` (not transparent)
- Dropdowns: solid `#ffffff` (not transparent)
- Google Fonts: must use `<link rel="stylesheet">` in `<head>`, NOT `@import` in CSS (Astro bundler drops @import)
- Netlify Forms: `data-netlify="true"` on form element

## Mobile Improvements Applied
- Section padding tightened: `2.75rem` vertical (was `4rem`) so sections feel connected
- Soft gradient section dividers between all major sections
- Process steps convert to vertical timeline on mobile (CSS grid + pseudo-element connecting line)
- Intro section h2 steps down to `1.75rem` on mobile (hero stays at `2.4rem`)
- Intro CTA: "Meet Maria" = primary button, "How It Works" = text link (not two equal buttons)
- Keepsake card gap tightened to `1.25rem` on mobile, CTA button pulled closer
- Hero CTAs stack full-width column on small screens

## Pending
- Real gallery photos from Maria (currently using shadow box product shots as placeholders)
- Maria's logo PNG (currently text-only logo)
- Custom domain (add via Netlify dashboard when Maria gets one)

## Deploy Workflow
1. Make changes
2. `npm run build && npx astro preview`
3. Show Jesse the local URL (http://localhost:4321)
4. Wait for explicit "push" confirmation
5. `netlify deploy --dir=dist --prod`
