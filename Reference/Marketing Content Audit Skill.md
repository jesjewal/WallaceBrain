# Marketing Content Audit Skill
**Location:** `~/.claude/skills/marketing-content-audit/SKILL.md`
**Created:** 2026-05-13

## What It Does
Full 5-dimension marketing content audit on any organization's website. Fetches real page content, runs 5 analysis agents in parallel, synthesizes a single scored report.

## How to Trigger
Say: "audit [company]'s marketing" or "grade [website URL]'s content" or "/marketing-content-audit https://..."

## The 5 Dimensions
| Dimension | What It Evaluates |
|---|---|
| Brand Perception | Clarity, resonance, trust signals, differentiation, consistency |
| Content Strategy | Depth, audience journey, storytelling, variety, CTAs, gaps |
| Copywriting | Generic vs. strong copy, headline hierarchy, CTA effectiveness |
| Marketing Psychology | Cialdini's 7 principles: social proof, authority, reciprocity, urgency, liking, consistency, specificity |
| SEO Content | Keyword intent, content depth, location SEO, service pages, thought leadership, internal linking |

## Scoring
- Brand Perception: /60 → divide by 6 for /10
- Content Strategy: /60 → divide by 6 for /10
- Copywriting: letter grade → numeric (A=9.5 ... C-=5 ... F=2)
- Psychology: /10
- SEO: /10
- Average = Overall score /10

## Competitive Mode
Feed multiple URLs → runs full audit on each → outputs side-by-side comparison table.

## Audits Completed
- **Shive-Hattery** — 4.4/10 — May 13, 2026 → see [[Shive-Hattery — 2026-05-13]]
