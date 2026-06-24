---
title: "Filled campus map approved"
date: 2026-06-13
allDay: false
startTime: "04:30"
endTime: "05:05"
area: "Design"
worth: 6
tvm: 3
by: claude
created: 2026-06-13 05:05
cssclasses:
  - nl-doc
---
Took the campus render from "sad" to approved. Two rejections drove it: (1) the early pastel-block PNGs ("shitty crayon"), and (2) overlaying routes as raw color-extracted dots. The breakthrough was reading Colton's `campus.FCStd` trace correctly — he didn't trace roads, he traced **filled zones**: paved campus pads (BSpline006/007), north parking (010), south ground (003), athletic grounds (005), and the **football field as two nested wires** — `Wire015` (green field) inside `BSpline002` (track ring), concentric at (512,387). My bug was drawing a bounding-box rectangle instead of filling his actual wire. Rebuilt as a properly **filled** vector map (zones filled as materials, buildings solid on top + shadows + labels, real field + track + yard lines, ALA navy/red brand chrome, north arrow, legend) — rendered to crisp SVG. **Colton: "looks great approved."**

**Files:** `web/CAD/out/campus_filled.svg` (approved), `out/diag.svg` + `out/diag_fill.svg` (the loop/zone classification that cracked it). See [[ala_campus_mapping]].
**Next:** zone material colors (which zone is parking vs concrete vs desert — his input); add the driveline routes *cleanly* (smooth lines, not dots); confirm 5/6/7/8 + 2/3/4 building labels.
**Why:** He's a designer — "make it better than the PDF, fill don't outline" was the bar. The fix was understanding his trace was regions to fill, not lines to stroke; once filled, it reads like a real campus map.
**TVM:** base 6 (production design iterations + trace-structure debugging + field fix + approved deliverable) × 3 (design focus, 4:30–5am) ≈ **ƒ18 effective**. See [[Value Engine]].
