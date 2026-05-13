---
name: Jesse Portfolio Website
description: macOS desktop-style portfolio site built in React + Vite + Framer Motion at /Users/wallace/Projects/bychudy-clone
type: project
---

Active portfolio project at `/Users/wallace/Projects/bychudy-clone`. Dev server runs at http://localhost:5173 via `npm run dev`. Deployed via GitHub push to `jesjewal/jesse-wallace-portfolio` → Netlify auto-deploys. Live at `jessewallaceportfolio.netlify.app` and custom domain `jesseleewallace.com`.

**Why:** Jesse's personal portfolio website with macOS desktop aesthetic.

**How to apply:** Always ask before pushing to GitHub — Jesse is credit-conscious. Folder is named `bychudy-clone`. All portfolio images in `/public/portfolio/`, gallery in `/public/gallery/`. Originals moved to `/Users/wallace/Projects/leftover photos/`.

## Stack
- React 18 + Vite 5
- Framer Motion 11 (drag, animate)
- CSS Modules (no Tailwind)
- No router — single-page SPA

## Architecture

**App.jsx** — root state + PROJECTS array. PROJECTS holds all portfolio items with id, title, category, client, year, thumb, type, description, optional link/linkLabel/openExternal/mobileExternal.

**Components:**
- `Desktop.jsx` — 4 folder icons (Videos/Photography/Design/Learning), shuffled randomly on each page load
- `FolderWindow.jsx` — opens on folder click, lists projects by category. Mobile position: `{ x: 76, y: 110 }`. Desktop: centered + 80px lower than default.
- `Window.jsx` — project detail popup. Draggable. `openExternal` forces external link always; `mobileExternal` forces external on mobile only (≤768px). Desktop embeds YouTube via BrowserWindow.
- `BrowserWindow.jsx` — embeds URLs in iframe, converts YouTube watch URLs to embed format automatically. Blocked sites list includes uihc.org.
- `NotesWindow.jsx` — CV/About/Interests. Tabs scroll to top on switch (useRef fix applied).
- `GalleryWindow.jsx` — photo gallery with GALLERY_PHOTOS array. Separate from project photos.
- `Dock.jsx` — left: FCP/Photoshop/InDesign app icons; mid: Gallery/CV/Mail; right: resume + LinkedIn.

## Folders (Desktop)
- **Videos** — red folder
- **Photography** — green folder
- **Design** — purple folder (renamed from Creative)
- **Learning** — blue folder
- Order is randomized on each visit (shuffle() in Desktop.jsx)

## Projects — Learning folder
- UFG Learning Quest (UFG Insurance (Spec))
- GreenState Values Swipe (GreenState Credit Union (Spec))
- MD Welcome Interview (Carver College of Medicine — MD Admissions) — replaced MyChart; YouTube embeds on desktop, external on mobile
- What to Expect Series (Holden) — two YouTube links, embeds on desktop
- Holden cancer series uses mobileExternal: true for Wave and Recruitment

## Key Deployment Notes
- Push to GitHub triggers Netlify build — do NOT use `netlify deploy` directly (creates new random site)
- Custom domain `jesseleewallace.com` registered via Porkbun, nameservers point to Netlify
- Accidental Netlify site was created (clinquant-sprinkles) — user deleted it
- `dist/` folder is committed (legacy) but Netlify builds from source

## Image Organization
- All gallery/photo images use "Large" versions only — originals moved to `/Users/wallace/Projects/leftover photos/`
- Gallery references maintained in `GalleryWindow.jsx` GALLERY_PHOTOS array
- Photo project references in `App.jsx` PROJECTS array (photos field)
- PDF files moved to `/Users/wallace/Projects/other pdfs/`
- Annual Report now links externally to greateriowacity.com

## Current Photo Sets (as of 2026-05-13)
- **Scenes:** 999A5475-2, 999A5744, 999A5982, BENJER2, DJI_0940-2, IC Sunset Update, IMG_0084, IMG_5467, IMG_5469, IMG_5473, JW5D0989, JW5D1589-3, JW5D9315, copter story, P1088048_lab, _V0A0024, _V0A8645_2, _V0A8912, _V0A9827, _V0A9870 2, _V0A9895, beegee, birdcompilation, bleedingheart, deercomp, flower updated-2, pickles, starfishsmall, 4V0A5102, 4V0A8516-Enhanced-NR_1, Deer up- sign removed, elknew, 40109725391, 48532904122, 49480637536, 32634520110
- **Astrophotography:** LONER, OLDCORN, STARCORN 2023, WINDMILLKYWAY4, mooonr7, 1F6A2084-2, 1F6A2134 copy, 2moon2, 518-Min Horizon Star Dupe-2, 564-Min Horizon Star Dupe-3, 8ABEAAD2, 50216258192

## DNS Issue (resolved ~2026-05-05)
- `jesseleewallace.com` had local DNS caching issue on home router — resolved on its own
