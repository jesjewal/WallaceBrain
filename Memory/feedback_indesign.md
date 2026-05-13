---
name: Feedback — InDesign Workflow Preferences
description: How Wallace wants InDesign scripting tasks approached
type: feedback
---

Always snapshot the target page before AND after making changes to visually verify results.

**Why:** Changes to geometry can have unintended side effects (overlapping items, clipped text). Snapshots catch these before the user sees them.

**How to apply:** On any page-layout task, take a before snapshot if state is unknown, then an after snapshot to confirm.

---

Infer all technical implementation from high-level design direction. Don't ask for pica coordinates or font names — derive them from existing page items.

**Why:** User gives direction like "move the image left so the person is in frame" — not pixel values. Expected to translate intent into coordinates.

**How to apply:** Inspect existing items first, then calculate appropriate bounds. Only ask for clarification if genuinely ambiguous.

---

Font/brand consistency matters greatly. New pages must match the established type system exactly.

**Why:** User interrupted mid-task to add "make sure we are consistent with our fonts and branding" — it was a top concern.

**How to apply:** Before adding text to new pages, refer to the Montserrat type system in the Shive-Hattery project memory. ExtraBold for titles, Bold for labels, Regular for body.
