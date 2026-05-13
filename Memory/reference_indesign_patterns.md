---
name: InDesign UXP Scripting Patterns
description: Reusable DOM patterns, gotchas, and helper functions for InDesign UXP via indesign-sidekick MCP
type: reference
---

## Key DOM Facts
- `require('indesign')` — entry point
- `app.activeDocument` — active doc
- Page size 51p × 66p; geometricBounds = [top, left, bottom, right] in picas
- Collection iteration: `.everyItem().getElements()` — required to get arrays
- Always specify units as strings: `"11pt"`, `"1in"`, `"5mm"` — bare numbers use doc units unpredictably
- Master spreads NOT accessible immediately after doc creation

## Helpers Used in Shive-Hattery Project
```javascript
const doc = require('indesign').app.activeDocument;
const pg  = doc.pages.everyItem().getElements();

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

// Apply font to existing text frame
function applyFont(tf, style, size, tracking, leading, color) {
  try {
    const F = s => doc.fonts.itemByName('Montserrat\t' + s);
    const paras = tf.paragraphs.everyItem().getElements();
    for (const p of paras) {
      if (style)    p.appliedFont = F(style);
      if (size)     p.pointSize   = size;
      if (tracking != null) p.tracking = tracking;
      if (leading  != null) p.leading  = leading;
      if (color)    p.fillColor   = doc.swatches.itemByName(color);
    }
  } catch(e) {}
}
```

## Image Placement
```javascript
const frame = page.rectangles.add();
frame.geometricBounds = [top, left, bottom, right];
frame.place('/absolute/path/to/image.jpg');
frame.fit(require('indesign').FitOptions.FILL_PROPORTIONALLY);
// Then nudge image position via frame.graphics[0] if needed
```

## Page Reordering
```javascript
page.move(LocationOptions.AFTER, referencePage);
```

## Logo Duplication to New Pages
```javascript
logoFrame.duplicate(targetPage.parent); // copies to same coords on target spread
```

## Header Resize Pattern
```javascript
// Header rect: [0, 0, 4.2, 51]
// Header text: [1.4, origLeft, 3.2, origRight]
item.geometricBounds = [0, 0, 4.2, 51];
tf.geometricBounds = [1.4, gb[1], 3.2, gb[3]];
```

## Gotchas
- `strokeWeight = 0` alone doesn't remove stroke — also set `strokeColor = 'None'`
- After `page.place()`, image may need manual position nudge for centering
- Table-like layouts built from individual rectangles + text frames (no actual InDesign tables used)
- Font name format: `'Montserrat\tBold'` (tab-separated family + style)
