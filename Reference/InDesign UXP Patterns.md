# InDesign UXP Scripting Patterns
*For use with indesign-sidekick MCP plugin*

## Key DOM Facts
- Entry point: `require('indesign')`
- Active doc: `app.activeDocument`
- Collection iteration: `.everyItem().getElements()` — required to get arrays
- Always specify units as strings: `"11pt"`, `"1in"`, `"5mm"` — bare numbers use doc units unpredictably
- Master spreads NOT accessible immediately after doc creation
- `geometricBounds = [top, left, bottom, right]`

## Core Helper Functions

```javascript
const doc = require('indesign').app.activeDocument;

// Create rectangle
function R(page, bounds, color) {
  const r = page.rectangles.add();
  r.geometricBounds = bounds;
  r.fillColor = doc.swatches.itemByName(color);
  r.strokeWeight = 0; r.strokeColor = doc.swatches.itemByName('None');
  return r;
}

// Create text frame
function T(page, bounds, content, font, size, tracking, leading, color, align) {
  const tf = page.textFrames.add();
  tf.geometricBounds = bounds;
  tf.contents = content;
  const p = tf.paragraphs.everyItem().getElements();
  for (const para of p) {
    if (font)     para.appliedFont = doc.fonts.itemByName(font);
    if (size)     para.pointSize   = size;
    if (tracking != null) para.tracking = tracking;
    if (leading  != null) para.leading  = leading;
    if (color)    para.fillColor   = doc.swatches.itemByName(color);
    if (align)    para.justification = align;
  }
  return tf;
}
```

## Image Placement
```javascript
const frame = page.rectangles.add();
frame.geometricBounds = [top, left, bottom, right];
frame.place('/absolute/path/to/image.jpg');
frame.fit(require('indesign').FitOptions.FILL_PROPORTIONALLY);
```

## Gotchas
- `strokeWeight = 0` alone doesn't remove stroke — also set `strokeColor = 'None'`
- Font name format: `'Montserrat\tBold'` (tab-separated family + style)
- Page indexing: use `doc.pages.item(n)` (0-based) — bracket notation returns undefined in UXP
- RIGHT-HAND pages in spreads: x offset = `pg.bounds[1]` — always add to all bounds
- `pg.allPageItems.everyItem()` is NOT a function — use rectangles + textFrames separately
- Capitalization inheritance: set `p.capitalization = Capitalization.NORMAL` on every paragraph
- InDesign caches images by filename — use unique names to force fresh load

## Workflow Rule
Always snapshot the target page before AND after making changes to visually verify results.
