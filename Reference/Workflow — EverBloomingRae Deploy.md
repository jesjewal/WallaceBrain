---
tags: [workflow, everbloomingrae, deploy]
---

# Workflow — EverBloomingRae Deploy

Always run `npm run build && npx astro preview` and share the local URL before deploying to Netlify. Wait for explicit confirmation before running `netlify deploy --prod`.

**Why:** Jesse wants to visually review changes locally before they go live.

**Command sequence:**
```bash
cd /Users/wallace/Projects/everbloomingrae
npm run build && npx astro preview
# → share http://localhost:4321
# → ask "looks good to push?" before deploying
```

**Related:** [[Projects/EverBloomingRae]]
