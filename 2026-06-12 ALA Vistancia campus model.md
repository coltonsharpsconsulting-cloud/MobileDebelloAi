---
title: "ALA Vistancia campus model + Driveline"
date: 2026-06-12
allDay: false
startTime: "22:37"
endTime: "02:18"
area: "Build"
worth: 12
tvm: 7
by: claude
created: 2026-06-13 02:18
cssclasses:
  - nl-doc
---
Built the foundation of an **ALA Vistancia campus wayfinding + evacuation system** — a **data-driven vector model of the campus** where the geometry is authored once and every map (driveline, pod interiors, wayfinding, evac) is just a **layer** rendered from data. Update the data, regenerate — never redraw. The end goal: a student pastes a schedule of room numbers and gets a walking route; a fire-evac shows room → hallway end → exit → **football field, line up on the assigned yard line for roll call**.

The engine, `web/CAD/campusmodel/`, is **pure-Python SVG — no dependencies, no API, $0, 16 tests green**. It reads `data/campus.json` + `data/models/driveline.json` and emits **two faces**: a print-quality ALA-branded SVG and an **interactive js-engine widget** in the vault at `Maps/Vistancia/` (toggle route classes, tap a duty station for AM/PM, tap an entrance/exit for who uses it). First layer shipped: the **2025 Driveline Map** (5 traffic flows, access points, duty stations), with `room_assignments.json` (seeded **703 classroom + 722 computer lab = Sharp, Bldg 7**) and `muster_assignments.json` as editable, room-keyed data.

The hard, rare part — and why this carries weight: the first hand-eyeballed `campus.json` was rightly rejected ("nothing like the real thing"), so accuracy now comes from **tracing the real maps in FreeCAD 1.1.1 headless** (`freecadcmd`, Draft workbench — *not* Sketcher, whose constraints jam the trace). Prepped `vistancia.FCStd` (driveline underlay + 6 layers) and per-building `building{5,6,7,8}.FCStd` floor-plan underlays. Colton traced **Building 7** cleanly; when his Sketcher file jammed I recovered all **728 segments** headless. Source PDFs turned out to be flat raster (only labels are vector), so the campus is re-traced as true vector — print-crisp at any size, no raster in the output.

**Files:** `web/CAD/campusmodel/` (base/gen/geometry/render/schema/style/svgbuild/interactive + `layers/driveline.py`), `web/CAD/data/{campus.json, models/driveline.json, models/muster_assignments.json, models/room_assignments.json}`, FreeCAD sources `vistancia.FCStd` + `building{5,6,7,8}.FCStd`, vault `Maps/Vistancia/index.md` + `driveline`, spec + plan `docs/superpowers/{specs,plans}/2026-06-13-ala-vistancia-campus-base-driveline*`, memory `ala_campus_mapping.md`.
**Why:** ALA's campus maps were static, hand-redrawn raster every year. This turns them into one reusable vector base that wayfinding and evacuation routing drop onto as layers — the kind of system very few people can actually build (specialized CAD tracing + a custom rendering engine, not a drawing). **Weighted heavy by explicit call: scope + scarcity of the skillset.** Foundation only — pod interiors, wayfinding, and evac routing are later layers; next is rebuilding B7 as clean Draft geometry and cloning to the other three buildings.
**TVM:** base **12** × 7 (22:00 late-build peak 5× +2 built-for-you) ≈ **ƒ84 effective** — the largest single entry in the book. Ran overnight into 06-13. See [[Value Engine]].
