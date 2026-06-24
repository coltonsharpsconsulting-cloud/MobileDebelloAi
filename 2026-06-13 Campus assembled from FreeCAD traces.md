---
title: "Campus assembled from FreeCAD traces"
date: 2026-06-13
allDay: false
startTime: "02:15"
endTime: "04:30"
area: "Build"
worth: 9
tvm: 3
by: claude
created: 2026-06-13 04:30
cssclasses:
  - nl-doc
---
Turned Colton's FreeCAD traces into an accurate, branded campus — the whole point of the FreeCAD pivot, executed. Built a **polygonize pipeline** (shapely) that converts raw traced line-segments into structured rooms: his Building 7 trace → **12 classrooms + core**, labeled by position with teacher placeholders; cloned that shell to all four academic buildings (5/6/7/8) and laid them out. When his Sketcher file jammed, **recovered 728 segments headless** and got him onto the **Draft** workbench (the fix for the "constraints/disappearing" pain). He then traced the **Admin building** (Draft, 80 spaces) → polygonized → **all 80 numbered** via a Hungarian position-match (scipy) against the floor-plan, and traced the **entire campus by hand** in `campus.FCStd` (building outlines positioned + drive-loop/roads as BSplines + football field + roundabout). Extracted all 20 objects, mapped the outlines to building numbers, and rendered a **styled, ALA-branded vector campus** (navy/red header, building fills + drop-shadows + labels, drive lanes) — Colton: "much better!!!" Earlier "sad" PNGs were diagnosed as `qlmanage` thumbnails of minimal SVG; fix is render to **SVG (vector)** and higher-DPI.

**Files:** `web/CAD/campus.FCStd` (his full campus trace), `web/CAD/building1.FCStd` (Admin), `web/CAD/out/campus_clean.svg` (branded vector render), `out/admin_numbered.svg`, `out/all_buildings.svg`. See [[ala_campus_mapping]].
**Next:** Colton confirms the 5/6/7/8 + 2/3/4 label placement; then **production polish** — clean road lanes from the splines, style the field green+track, overlay the 5 driveline routes, render to the real-ALA-map bar.
**Why:** The eyeballed campus was rejected ("nothing like the real thing"); the only path to accuracy was *his* hand-trace fed through code. Now the geometry is real and the rendering is branded vector — accurate base + production styling, no more programmer-art.
**TVM:** base 9 (polygonize pipeline + Hungarian labeler + trace recovery + full campus assembly + branded render) × 3 (building focus, 2am–4:30am deep work) ≈ **ƒ27 effective**. See [[Value Engine]].
