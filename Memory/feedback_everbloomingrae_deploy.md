---
name: EverBloomingRae — Deploy Workflow
description: Always preview locally before pushing to Netlify for the EverBloomingRae project
type: feedback
---

Always run `npm run build && npx astro preview` (or equivalent local preview) and tell the user the local URL before deploying to Netlify. Wait for explicit confirmation before running `netlify deploy --prod`.

**Why:** User wants to visually review changes locally before they go live. Was frustrated that pushes happened immediately without a local preview step.

**How to apply:** After finishing code changes on the EverBloomingRae site, build and start the local preview server, share the URL (usually http://localhost:4321), and ask "looks good to push?" before deploying.
