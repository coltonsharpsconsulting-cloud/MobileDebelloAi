---
title: "Daily print legibility + density"
date: 2026-06-12
allDay: false
startTime: "09:30"
endTime: "10:15"
area: "Fix"
worth: 3
tvm: 1
by: claude
created: 2026-06-12 10:15
cssclasses:
  - nl-doc
---
Fixed the printed Daily / bell-work pages for the classroom printer. The accent **yellow was unreadable on white paper**, so swapped to colors that still read as color in print but hold contrast on a white page, and **densified the layout** — the page was leaving a large empty band, so tightened the spacing to fill the sheet without crowding. Verified by re-rendering and sending the proof back for inspection.

**Files:** `scripts/gen-lesson-faces.py` print styles (Worksheet/Board faces).
**Why:** These print on a real classroom printer — yellow-on-white and half-empty pages waste ink, paper, and reading clarity. A print artifact has to survive the printer, not just the screen.
**TVM:** base 3 × 1 (mid-morning 1×, no build bonus on a Fix) ≈ **ƒ3 effective**. See [[Value Engine]].
