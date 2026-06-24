---
title: "Campus foundation + live FreeCAD"
date: 2026-06-13
allDay: false
startTime: "20:41"
endTime: "22:30"
area: "Build"
worth: 9
tvm: 5
by: claude
created: 2026-06-13 23:55
cssclasses:
  - nl-doc
---
The night the campus stopped fighting back. The hand-traced lanes kept coming back as squiggles because I kept *re-processing* his clean geometry; the fix was two moves. **(1) Method:** dropped the "fancy math" and used the **standard road centerline + offset** — cluster his concentric hand-lanes by a parallel-neighbor test into **7 road groups**, take one centerline each, stroke to a uniform width with round caps (uniform lanes *and* clean entrance terminations, for free). The straight equal-length `Line` sets read as **parking stall stripes**, kept thin. **(2) Source of truth:** installed his `freecad-mcp` fork (AICopilot workbench) and — the unlock — reached its Unix socket **directly** with a tiny JSON client (no Claude restart, no MCP registration), marshalling GUI ops onto the server's main-thread task queue. With live eyes on the model I built **8 semantic groups** into `campus.FCStd` (Buildings/Field/Roads/Parking/Zones/Roundabouts/Markings/Details — all **127 objects**), exported a **manifest** as the render source of truth, **confirmed orientation is FreeCAD Y-up** (the earlier "inverted" was my own vertical flip), read the **real underlay** to confirm Markings = parking stripes + Details = islands, and captured the **5 driveline gates**. Also caught and fixed a bug *my own* headless save introduced — it regenerated the GuiDocument with everything hidden — by restoring visibility and re-saving his file.

**Files:** `web/CAD/render_campus.py`, `web/CAD/data/campus_manifest.json`, `web/CAD/data/driveline.json`, `web/CAD/campus.FCStd` (+ groups, backup `campus.FCStd.bak-pregroup-*`), `/tmp/fc_sock.py` (reusable socket client), `.mcp.json`. See [[ala_campus_mapping]].
**Next:** render the definitive polished map off the locked classification; then **wayfinding** (schedule→route) and **evac** (room→muster) on the gate rules.
**Why:** every campus redo traced to one root cause — me *guessing* what his objects were and which way was up. Making his FreeCAD model the authority (live-readable, grouped, manifest-backed) ends the guessing permanently.
**TVM:** base 9 (live-MCP socket integration + live-edit foundation + full 127-object classification + 2 bug fixes) × 5 (evening build, 8–10:30 PM) ≈ **ƒ45 effective**. See [[Value Engine]].
