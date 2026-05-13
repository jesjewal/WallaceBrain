---
name: Shive-Hattery Proposal — Corridor Mixed-Use Development
description: Active 12-page InDesign proposal for Shive-Hattery architecture firm, Coralville Iowa project
type: project
---

Active InDesign document (untitled, 12 pages) — a proposal from Shive-Hattery architecture firm for "Corridor Mixed-Use Development" in Coralville, Iowa. Estimated project start Q3 2024.

**Why:** Practice/demo proposal built to look like a real Shive-Hattery submission. Uses real firm branding, real project references, and scraped images from shive-hattery.com.

**How to apply:** When resuming, always snapshot the target page first to verify current state before making changes.

---

## Document Specs
- Page size: 51p × 66p (picas)
- Footer baseline: ~63.48p from top
- Units: PICAS throughout

## Page Order (0-indexed)
0. Cover
1. Firm Overview
2. Project Understanding
3. Cover Letter
4. Our Approach
5. RSM US (project)
6. Orchard Court Lofts (project)
7. Riverfront West (project)
8. Project Team
9. Alex Collins (staff profile)
10. References
11. Schedule

## Brand Colors (swatches)
- SH-Blue — primary blue header/accent
- SH-NearBlack — footer strip, body headlines
- SH-GrayLight — table row backgrounds
- SH-White — reversed text
- SH-Gray — secondary body text

## Typography System (Montserrat throughout)
- ExtraBold 16pt+ tracking -10: major page titles
- Bold 6-7pt tracking 160-180: section labels / eyebrows
- SemiBold: sidebar values, callout numbers
- Regular 9-9.5pt leading 16: body copy
- Medium: metadata, captions
- Italic: quotes, attributions

## Blue Header — All Pages
- Header rect: [0, 0, 4.2, 51] (height 4.2p)
- Header left text (SHIVEHATTERY logo): [1.4, 3.0, 3.2, 20.0] — Montserrat Bold 7pt SH-White tracking 160
- Header right text (section label): [1.4, 22.0, 3.2, 48.0] — Montserrat Bold 7pt SH-White tracking 160, RIGHT_ALIGN
- Header texture overlay: firm_overview.jpg at Multiply 25% over full header rect

## Footer Structure (all pages)
- NearBlack strip: [63.48, 0, 66, 51]
- Logo frame centered bottom
- Left footer: "People-Centered Design · A+E"
- Right footer: "shive-hattery.com"

## Ghost Background Treatment (pages 3–12 except cover/firm overview)
- Rect: [4.2, 0, 63.48, 51], page-specific image at 8% opacity, Normal blend
- Z-order: behind content but above header rect
- Left column overlay (Paper swatch): starts at content start, ~65% opacity
- Right column overlay (Paper swatch): starts at content start, ~88% opacity

## Downloaded Images
- `/Users/wallace/Downloads/shivehattery-images/firm_overview.jpg` — WDM office interior; header texture (all pages) + page 1
- `/Users/wallace/Downloads/shivehattery-images/orchard_hero.jpg` — Orchard Court Lofts exterior (page 7 hero)
- `/Users/wallace/Downloads/shivehattery-images/riverfront_hero.webp` — Riverfront West exterior (page 8 hero)
- `/Users/wallace/Downloads/shivehattery-images/site_context.jpg` — page 3 card 1
- `/Users/wallace/Downloads/shivehattery-images/program_mix.jpg` — page 3 card 2
- `/Users/wallace/Downloads/shivehattery-images/community.jpg` — page 3 card 3
- `/Users/wallace/Downloads/shivehattery-images/market.jpg` — page 3 card 4
- `/Users/wallace/Downloads/shivehattery-images/rsm_bg.jpg` — ghost bg page 6
- `/Users/wallace/Downloads/shivehattery-images/orchard_bg.jpg` — ghost bg page 7
- `/Users/wallace/Downloads/shivehattery-images/riverfront_bg.jpg` — ghost bg page 8
- `/Users/wallace/Downloads/shivehattery-images/refs_bg.jpg` — ghost bg page 11
- `/Users/wallace/Downloads/shivehattery-images/sched_bg.jpg` — ghost bg page 12
- `/Users/wallace/Downloads/shivehattery-images/centennial_park.jpg` — ghost bg page 5

## Page 10 (Staff Profile, index 9) — Two-person half-page layout (final 2026-04-11)
- Divider at 33.3p (SH-NearBlack rule, full width)
- TOP HALF — Alex Collins, AIA: name/title/creds in left area, PORTRAIT photo at [4.5,38.5,15.5,49] (11p×10.5p), separator at 15.8p, sidebar + bio + 3 projects below
- BOTTOM HALF — Renee Hartmann, AIA: same structure from B=34.0p, photo at [34.3,38.5,45.3,49], separator at 45.6p
- Photo frames are PORTRAIT (11p tall × 10.5p wide) — matches team page grid proportions
- Top-anchor fix: must use r.geometricBounds (numeric) NOT the input bounds array (strings) when computing graphic offset
- allPageItems is a plain JS array on this page — do NOT call .everyItem()

## Page 9 (Project Team, index 8) — Style-aligned + headshots placed (2026-04-11)
- 3×2 grid: top row [19.5–31.5p], bottom row [38–50p], cols at left=3,17.5,32 right=16,30.5,45
- Headshots placed, all top-anchored, Tom Vogt zoomed 1.4× for face consistency
- Typography: names SemiBold 9.5pt SH-NearBlack, eyebrow labels SH-Blue tracking 160, titles 7pt SH-NearBlack no tracking
- All names populated (see Team Roster below)

## Page 7 (Orchard Court Lofts, index 6) — Fixed this session
- Layout order corrected: label [22.5p] → title [24.1p] → date [27.2p] → sidebar+body [29p]
- Matches RSM page (index 5) structure

## Team Roster (Corridor Mixed-Use Development)
- **Renee Hartmann, AIA** — Principal-in-Charge · Des Moines Studio · 22 yrs
- **Alex Collins, AIA** — Senior Project Architect · Iowa City Studio · 12 yrs
- **Marcus Teel, PMP** — Project Manager
- **Brian Schroeder, PE** — Structural Engineer
- **Lindsey Park, PE** — MEP Engineer (Mechanical/Electrical)
- **Tom Vogt, PE, LEED AP** — Civil Engineer

## Downloaded Images (Headshots — added 2026-04-11)
- `/Users/wallace/Downloads/shivehattery-images/headshot_alex_collins.png` — Alex Collins, 1152×1536
- `/Users/wallace/Downloads/shivehattery-images/headshot_principal.png` — Renee Hartmann, 1152×1536
- `/Users/wallace/Downloads/shivehattery-images/headshot_pm.png` — Marcus Teel, 1152×1536
- `/Users/wallace/Downloads/shivehattery-images/headshot_structural.png` — Brian Schroeder, 1152×1536
- `/Users/wallace/Downloads/shivehattery-images/headshot_mep.png` — Lindsey Park, 1152×1536
- `/Users/wallace/Downloads/shivehattery-images/headshot_civil.png` — Tom Vogt, 1152×1536
- Source images in `/Users/wallace/Downloads/` — cropped from Gemini-generated PNGs to consistent 3:4 portrait (top-favored crop)

## References Page (index 10) — Contacts populated 2026-04-11
- RSM US LLP: Patricia Haber · Director of Real Estate · (954) 372-8450 · p.haber@rsmus.com
- Midwest Financial Group: Thomas Kuhn · COO · (319) 337-4210 · t.kuhn@midwestfinancialgroup.com
- Riverfront West Partners, LLC: James Ostrander · Principal/Owner · (319) 621-5837 · j.ostrander@riverfrontwestpartners.com

## Headshot Notes (2026-04-11)
- Brian Schroeder (headshot_structural_v2.png): dark background causes optical illusion of face being low — fixed with 1.5× zoom + 3p upward shift on graphic
- InDesign caches images by filename — use unique filenames to force fresh load (e.g., headshot_structural_v2.png)
- Top-anchor formula: use `r.geometricBounds` (numeric) NOT the input bounds string array when computing graphic offset after fit

## Final Headshot Files (2026-04-11, session 2)
- All 6 placed as `final_*.png` in `/Users/wallace/Downloads/shivehattery-images/`
- `final_renee_hartmann.png`, `final_alex_collins.png`, `final_marcus_teel.png` — identical crops (y_offset=0)
- `final_brian_schroeder.png` — y_offset=30px from v2
- `final_tom_vogt.png` — y_offset=90px, face brought up
- `final_lindsey_park.png` — identical crop
- Placed and top-anchored on both page 8 (team grid) and page 9 (staff profile)
- Document saved

## Cover Page (index 0) — Block dimensions (2026-04-15)
- SH-Black overlay block (55% opacity): [2.52, 3.30, 13.68, 25.00] — right edge trimmed from 27.60p → 25p (was too much empty space after logo text)
- Horizontal rule below logo: [11.82, 4.08, 13.02, 25.00] — trimmed to match block right edge
- SH-Blue vertical accent (left edge): [2.52, 3.30, 13.68, 3.60] — unchanged
- Logo text frame: [3.12, 4.08, 11.40, 20.52] — unchanged

## Web Version — iOS Autoplay Note
- iOS Safari blocks video autoplay unless `<video>` has `autoplay muted playsinline` attributes
- Per-device setting: Settings → Safari → Auto-Play (default "Stop Media with Sound")
- Low Power Mode and Low Data Mode also block autoplay
- Clearing browser history does NOT affect autoplay settings

## Pending / Known Issues
- Headshots still visually inconsistent due to varied backgrounds/lighting (not a crop problem) — needs Nano Banana regeneration with uniform warm-gray studio backdrop for true consistency
- Consider second firm photo on Firm Overview page (body copy slightly cut off)
- Brian's dark background is a source image problem — needs new generation

## Pivot Note (2026-04-11)
- User pivoting to HTML version of the proposal using Google Stitch for design
- InDesign version is saved and complete as-is

---

## Web Version — Astro Site (2026-04-12)

**Repo:** `jesjewal/corridor-proposal` (private GitHub, auto-deploys to Netlify)
**Local path:** `/Users/wallace/Documents/proposal-two`
**Live:** Netlify (URL unknown, check Netlify dashboard)

### Architecture
- Astro static site, 12 pages
- **Two layout systems:**
  - `src/layouts/Base.astro` — used by all pages except cover
  - `src/pages/index.astro` — cover page has its own self-contained HTML template, imports Nav directly
- `src/components/Nav.astro` — fixed left sidebar nav (`position: fixed; width: 180px; height: 100vh; background: nearblack`)
- `src/components/Header.astro` — blue header strip with hamburger button (only on Base.astro pages)
- `src/styles/global.css` — single CSS file, all styles

### Mobile Nav — RESOLVED 2026-04-12
**Fix:** The cover page button was placed after `</div><!--/.site-shell-->` in `index.astro`, pushing it below the 100vh fold on mobile — users couldn't click it. Moved button inside `.cover-topbar` (position: absolute at top of hero). Base.astro pages were always correct; CSS and inline onclick worked fine.

**Current state:**
- Cover page: button inside `.cover-topbar` with `margin-left: auto`
- All other pages: button in `.page-header-strip` (Header.astro) — unchanged
- CSS: `@media (max-width: 900px) { .site-nav { transform: translateX(-100%) } .site-nav.open { transform: translateX(0) } }` — correct and in bundle

### Nav Grouping — Added 2026-04-12
Nav.astro restructured to show section labels (PROPOSAL / PROJECTS / TEAM) using existing `.nav-section-label` CSS. Inspired by Shive-Hattery site's hierarchical navigation.

### Content Fixes Done (2026-04-12)
- Team page: photo assignments corrected (brian→final_renee_hartmann.png, renee→final_marcus_teel.png, marcus→final_brian_schroeder.png)
- Staff profile page: second profile replaced from Renee Hartmann → Brian Schroeder, PE (matches reference page_10)

---

## Work Sample Booklet — 8-Page Portfolio (Interview Prep, due ~May 6, 2026)

**Purpose:** Work sample booklet for Shive-Hattery final interview, May 6. 8 pages, A4 portrait (8.27" × 11.69"), facing pages. All 8 pages built as of 2026-04-25.

**Document:** Active InDesign file (untitled). Units: INCHES. Margins: 0.5" all around.

### Page Structure
- P1 (index 0): Cover — dark navy, "Jesse Wallace", orange rule, cream footer band — EXISTS
- P2 (index 1): About Me — cream bg, serif title, photo placeholder, bio text, credential block
- P3 (index 2): Table of Contents — 3 numbered sections with sub-items and page refs
- P4 (index 3): Section 01 opener — Video & Multimedia Production
- P5 (index 4): Video detail — two image frames + UIHC + Greater Iowa City descriptions
- P6 (index 5): Section 02 opener — Print & Editorial Publishing
- P7 (index 6): Print detail — large image frame + two smaller + annual report + magazine copy
- P8 (index 7): Section 03 — Digital Content Strategy (opener + selected work links)

### Design System (implemented — "light editorial" template)
Pivoted from dark Nano Banana concept to a light cream editorial template (reference image provided 2026-04-25).

**Color swatches (in document):**
- `WS-Cream` — RGB 248, 246, 241 — page background
- `WS-NearBlack` — RGB 28, 27, 25 — primary text
- `WS-Orange` — RGB 194, 82, 36 — section numbers, accent rules, right-edge tabs
- `WS-Slate` — RGB 130, 152, 168 — thin horizontal rules, photo frame strokes, footer rule
- `WS-Gray` — RGB 120, 116, 112 — eyebrow labels, captions, metadata, page numbers

**Typography:**
- Display/titles: `Minion Pro Regular` — large serif for "About Me", "Table of Contents", section numbers (01/02/03)
- Section titles + credential: `Myriad Pro Bold` — 11–16pt, tracking 10–40
- Eyebrow labels: `Myriad Pro Regular` — 7pt, tracking 180, all-caps text content
- Body copy: `Myriad Pro Regular` — 9–9.5pt, leading 15–16pt, spaceAfter 9–10pt
- Page numbers / metadata: `Myriad Pro Regular` — 7pt

**Layout patterns (recurring):**
- Eyebrow label + full-width slate thin rule at top of every page
- Right-edge orange tab: [2.0in, 7.77in, 2.75in, 8.27in] on every page
- Footer slate rule at 11.05in + page number at 11.13in
- Section openers: large image frame left (~57% width), section number + title + facts right (right col starts at 4.9in)
- Detail pages: image grid left column, two work descriptions right column separated by orange rule

### Critical UXP Scripting Notes
- **Spread coordinate offset**: RIGHT_HAND pages require x offset = `pg.bounds[1]` (= 8.27" for pages in a 2-page spread). ALWAYS use `const ox = pg.bounds[1]` and add to all left/right bounds.
- **Page indexing**: Use `doc.pages.item(n)` (0-based). Bracket notation `doc.pages[n]` returns undefined in UXP.
- **Capitalization inheritance**: Document base style applies ALL_CAPS. Always set `p.capitalization = Capitalization.NORMAL` on every paragraph.
- **Clear page**: Use `pg.rectangles.everyItem().getElements()` + `pg.textFrames.everyItem().getElements()` (NOT `pg.allPageItems.everyItem()` — not a function in UXP).

### Pending / Next Steps
- Replace placeholder image frames with actual screenshots/photos
- Confirm CBBC inclusion in Section 03 (user still deciding)
- Fine-tune bio copy and section descriptions as needed
