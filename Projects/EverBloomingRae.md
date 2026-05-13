# EverBloomingRae Website
**Status:** Live · Last updated 2026-05-13

## Links
- **Live site:** https://everbloomingrae.netlify.app
- **GitHub:** https://github.com/jesjewal/everbloomingrae (private)
- **Local:** `/Users/wallace/Projects/everbloomingrae/`
- **Instagram:** https://www.instagram.com/everbloomingrae/
- **TikTok:** https://tr.ee/BZyIRvzWrb
- **Email:** everbloomingrae@gmail.com

## Background
Jesse built a full website for his friend **Maria Rae**'s floral preservation business. She had no standalone site — only Instagram and a Linktree. Site is live and actively maintained.

## Stack
- **Framework:** Astro (v6.3.1), static output
- **Styling:** Custom CSS, design system based on Stitch "Petal & Heirloom / Eternal Spring"
- **Fonts:** Cormorant Garamond (display) + Montserrat (UI), loaded via `<link>` in Base.astro
- **Hosting:** Netlify — auto-deploys from GitHub push
- **Deploy command:** `npm run build && netlify deploy --dir=dist --prod`

## Design System
- **Primary color:** `#6f2434` deep wine rose
- **Surfaces:** Semi-transparent warm creams over fixed illustrated texture background (`/images/hero-texture.png`, opacity 0.13)
- **Buttons:** Pill shape, 13px / weight 500 / 0.055em tracking / uppercase
- **Eyebrows:** Cormorant Garamond roman, 12px, uppercase, 0.22em tracking
- **Nav links:** Montserrat 14px, weight 500, normal case

## Pages
| Page | Notes |
|---|---|
| `/` | Hero carousel (5 images, 3.5s fade), keepsake grid, process steps, final CTA |
| `/services` | Service offerings with pricing |
| `/process` | Step-by-step preservation process |
| `/gallery` | Masonry grid — currently using product photos as placeholders |
| `/about` | Maria's story |
| `/faq` | Accordion FAQ |
| `/contact` | Netlify Forms + social links |
| `/invest` | Pricing/investment page |

## Mobile Improvements (May 2026)
- Section padding tightened: `2.75rem` (was `4rem`)
- Soft gradient section dividers between all major sections
- Process steps → vertical timeline on mobile
- Intro h2 steps down to `1.75rem` (hero stays `2.4rem`)
- Intro CTA hierarchy: "Meet Maria" = button, "How It Works" = text link
- Hero CTAs stack full-width column on small screens

## Deploy Workflow
1. Make changes
2. `npm run build && npx astro preview`
3. Show local preview at http://localhost:4321
4. Wait for explicit "push" confirmation
5. `netlify deploy --dir=dist --prod`

## Pending
- Real gallery photos from Maria (currently using shadow box product shots)
- Maria's logo PNG (currently text-only)
- Custom domain (add via Netlify dashboard when ready)
