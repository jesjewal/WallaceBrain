# Jesse Wallace Portfolio Site
**Status:** Live · Last updated 2026-05-13

## Links
- **Live site:** https://jesseleewallace.com
- **Also at:** https://jessewallaceportfolio.netlify.app
- **GitHub:** https://github.com/jesjewal/jesse-wallace-portfolio (private)
- **Local:** `/Users/wallace/Projects/bychudy-clone/`

## Stack
- React 18 + Vite 5
- Framer Motion 11 (drag, animate)
- CSS Modules (no Tailwind)
- Single-page SPA — no router
- Deploys via GitHub push → Netlify auto-build (do NOT use `netlify deploy` directly)

## Domain
- `jesseleewallace.com` — registered via Porkbun, nameservers point to Netlify

## Architecture
- **App.jsx** — root state + PROJECTS array
- **Desktop.jsx** — 4 folder icons, shuffled randomly on each load
- **FolderWindow.jsx** — opens on folder click, lists projects by category
- **Window.jsx** — project detail popup, draggable
- **BrowserWindow.jsx** — embeds URLs in iframe, auto-converts YouTube watch → embed
- **NotesWindow.jsx** — CV/About/Interests with tab scroll fix
- **GalleryWindow.jsx** — photo gallery, separate GALLERY_PHOTOS array
- **Dock.jsx** — app icons left, Gallery/CV/Mail center, resume + LinkedIn right

## Folders
| Folder | Color | Category |
|---|---|---|
| Videos | Red | `video` |
| Photography | Green | `photo` |
| Design | Purple | `design` |
| Learning | Blue | `instructional` |

## All Projects
**Videos:** Breathing New Life, Childcare Solutions, Kid Captain Nile Kron, UIHC Recruitment Series, Trelease Woods, The Hawkeye Wave

**Design:** GIC 2025 Annual Report, Architecture Proposal Concept, Architecture Web Proposal, My Portfolio

**Photography:** Crossover at Kinnick, Astrophotography, Scenes, Portraits

**Learning:** UFG Learning Quest, GreenState Values Swipe, MD Welcome Interview, What to Expect Series

## Photo Sets (as of 2026-05-13)
**Scenes:** 999A5475-2, 999A5744, 999A5982, BENJER2, DJI_0940-2, IC Sunset Update, IMG_0084, IMG_5467, IMG_5469, IMG_5473, JW5D0989, JW5D1589-3, JW5D9315, copter story, P1088048_lab, _V0A0024, _V0A8645_2, _V0A8912, _V0A9827, _V0A9870 2, _V0A9895, beegee, birdcompilation, bleedingheart, deercomp, flower updated-2, pickles, starfishsmall, 4V0A5102, 4V0A8516-Enhanced-NR_1, Deer up- sign removed, elknew, 40109725391, 48532904122, 49480637536, 32634520110

**Astrophotography:** LONER, OLDCORN, STARCORN 2023, WINDMILLKYWAY4, mooonr7, 1F6A2084-2, 1F6A2134 copy, 2moon2, 518-Min Horizon Star Dupe-2, 564-Min Horizon Star Dupe-3, 8ABEAAD2, 50216258192

## Deploy Rules
- **Always push via GitHub** — `git add → git commit → git push`
- **Never use `netlify deploy`** — creates a new random site
- **Always ask before pushing** — Jesse controls when pushes happen
