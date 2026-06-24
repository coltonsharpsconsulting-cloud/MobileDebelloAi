---
title: "Class nav + back-home wayfinding"
date: 2026-06-06
allDay: false
startTime: "06:05"
endTime: "06:50"
area: "Build"
worth: 7
tvm: 3.5
by: claude
created: 2026-06-06 06:50
cssclasses:
  - nl-doc
---
Wired the navigation Colton asked for. **Class Nav** (`Scripts/class-nav.js`) in the Today block: a button per class, and the one you're teaching *right now* (by the bell schedule) lights up + badges "now" and jumps to its class hub. Every **course hub now links back home** (`[[Colton|← home]]` · ALA · Dashboard; Science 7 → `[[Nikki]]`), baked into the generator via an `OWNER` map. To avoid a third copy of the bell times, extracted **`Scripts/schedule.js`** as the single source (SCHED + `currentPeriod`) and refactored `board.js` to import it (async render; embeds now `return await`).

**Files:** `Scripts/schedule.js`, `Scripts/class-nav.js`, `Scripts/board.js`, `Colton.md`, `Maps/ALA.md`, `Nikki.md`, 6 course hubs, `stratosyn.css`, `gen-curriculum-map.py`.
**Why:** "tie it back to the home page… class buttons… based on schedule that button appears in the today block."
**TVM:** base 7 × 3.5× (early morning + building) ≈ **ƒ25 effective**.
