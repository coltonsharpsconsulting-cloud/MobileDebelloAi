---
title: "Madewell Daily — Unit 3 (Human Body Systems) + palette/crossword fixes"
date: 2026-06-05
allDay: false
startTime: "12:30"
endTime: "12:50"
area: "Build"
worth: 12
tvm: 3
by: claude
created: 2026-06-05 12:50
cssclasses:
  - nl-doc
---
Generated **all of Unit 3 — Human Body Systems** (Science 7, Weeks 10–13) via the rolling Workflow: **20 issues, Sep 28 → Nov 6** (Scout correctly mapped the post-fall-break dates and skipped the break). Levels of organization → system interdependence → organ models → sensory receptors / stimulus-response → nervous system → the Unit 3 Assessment study-guide. 41 agents, ~1.65M tokens, ~15 min. **20/20 verifier PASS.** Per-week puzzles all distinct (the write-time enforcement held), both crosswords structurally checked.

**Two real defects my QC caught that the per-day verifiers missed:**
1. **Off-palette theme.** I'd told writers to accent the unit with `#ec4899` (pink) — but reading the actual `stratosyn.css`, there is **no pink token**; the named accents are gold/cyan/green/purple #a855f7/indigo #5e6ad2. Units 1–2 use zero pink — it was purely my Unit-3 instruction. One verifier "fixed" it to purple, the others rationalized keeping it, leaving the unit half-pink/half-purple. Standardized all 20 issues to **purple `#a855f7`** (on-palette, consistent); normalized a stray `#2a3450` → `#28324a`.
2. **A malformed crossword** (Nov 2, "Taste and Smell"): SMELL and NERVE ran in adjacent parallel columns and overlapped, producing two un-clued 2-letter runs — it would have printed broken. Rebuilt it as a validated pinwheel (TASTE/SENSE across, SMELL/NERVE down, every crossing letter checked in code).

**Forward fix (baked into Unit 4+):** the script now embeds the exact Stratosyn palette (named tokens only, "no #ec4899") in the writer theme, the verifier palette-check, and the crossword spec — plus a crossword rule that words may only touch at a shared crossing letter (never parallel-adjacent). A programmatic grid-geometry check is now part of my per-unit QC gate.

**Files:** `The Madewell Daily/2026-09-28 … 2026-11-06` (20 issues); Workflow `madewell-daily-unit3-body`. Library now **58 issues** (Units 1–3).
**Why:** rolling the full year; Unit 3 surfaced a palette + crossword-construction gap, now closed for the remaining units.
**TVM:** base 12 × 3× (midday + building) ≈ **ƒ36 effective**.
