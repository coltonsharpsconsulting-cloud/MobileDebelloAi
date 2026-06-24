---
title: "Campus drafting — roads + roundabout"
date: 2026-06-15
allDay: false
startTime: "14:08"
endTime: "18:12"
area: "Build"
worth: 5
tvm: 3
by: claude
created: 2026-06-16 22:18
cssclasses:
  - nl-doc
---
Hands-on campus geometry in FreeCAD, live over the socket. Joined his hand-drawn polylines into closed wires, **filleted** the hard corners to match real curb radii, drafted the **curves off his guide-lines** where his shapes were still straight, and **traced the roundabout** cleanly. Pulled the underlay image so he could read his own lines on a white background, **reorganized the model tree** into sane groups, and drafted the **south-end road** where there was nothing to trace from. Iterative craft work — his lines, my fillets/joins — building the real perimeter and lane network into `campus.FCStd`.

**Files:** `web/CAD/campus.FCStd` (geometry); live socket client `/tmp/fc_sock.py`.
**Why:** the map is only as good as the geometry under it; getting the roads, curbs, and roundabout drafted to real radii is what makes the eventual wayfinding/evac layers trustworthy.
**TVM:** base 5 × 3 (afternoon build) ≈ **ƒ15 effective**. See [[Value Engine]] · [[ala_campus_mapping]].
