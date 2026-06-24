---
title: "Class Hub rollout + generator hardening"
date: 2026-06-06
allDay: false
startTime: "05:30"
endTime: "06:05"
area: "Build"
worth: 6
tvm: 3.5
by: claude
created: 2026-06-06 06:05
cssclasses:
  - nl-doc
---
Rolled the **Class Hub** to all six course hubs (each in its color), so every class now opens onto its live this-week card + build-out arc. Fixed both Robotics textbook lines (raw Python dict → just the title). **Hardened the generator** (`gen-curriculum-map.py`): added `COURSE_HUE`, made the textbook line dict-safe, and made every course hub auto-include the Class Hub embed — so regenerations keep it. Verified it compiles.

**Files:** 6 course hub notes, `scripts/gen-curriculum-map.py`.
**Why:** "go" — finish the class-hub progression across the board and bake it in.
**TVM:** base 6 × 3.5× (5–6 AM, early-bird + building — the elite window passed) ≈ **ƒ21 effective**.
