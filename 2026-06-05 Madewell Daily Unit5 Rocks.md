---
title: "Madewell Daily — Unit 5 (Cycling of Earth's Materials) + class-lock fix"
date: 2026-06-05
allDay: false
startTime: "13:10"
endTime: "13:35"
area: "Build"
worth: 11
tvm: 3
by: claude
created: 2026-06-05 13:35
cssclasses:
  - nl-doc
---
Generated **all of Unit 5 — Cycling of Earth's Materials** (Science 7, Weeks 20–23) — first earth-science unit, gold/amber theme: **13 issues, Dec 21 → Jan 22** (winter break compressed the unit; Scout correctly mapped the one pre-break day + the January weeks). Rock cycle & three rock types → mechanical/chemical weathering → erosion & deposition → the Unit 5 Assessment. 27 agents, ~925k tokens, ~24 min.

**Two verifier agents failed** (didn't emit StructuredOutput) — Jan 13 and Jan 19. The writers had already written both files; only the verify pass was missing, so **I verified those two myself**: the cipher decodes to DEPOSITION (10 letters, matches), the riddle answers EROSION (7), and both leads are scientifically sound. While checking them I caught a new defect class: those two writers had invented **unstyled puzzle sub-classes** (`daily-code`, `daily-puzzle-rule`, `daily-hint`, `daily-riddle`) that don't exist in `stratosyn.css` — they'd render unstyled. Normalized both into the styled `.daily-vocab` convention. A library-wide class audit then confirmed **zero invented classes remain** anywhere (the only unstyled `daily-*` hooks left — `daily-ann/lead/side/puzzle` — are in the locked template itself and styled via their parents).

The rest of the unit was clean: palette all on-token (gold lead), per-week puzzles distinct, the Jan-12 crossword passed grid validation, no placeholders.

**Forward fix (in Unit 6+):** the script now (a) **class-locks** the puzzle box (only `.daily-grid` / `.daily-cross`+`.cx` / `.daily-vocab`; explicitly forbids `daily-code` & friends) and (b) tells the verifier it **must** end by calling StructuredOutput (so verify-stage drop-outs stop). My per-unit QC gate now includes the invented-class audit.

**Files:** `The Madewell Daily/2026-12-21 … 2027-01-22` (13 issues); Workflow `madewell-daily-unit5-rocks`. Library now **91 issues** (Units 1–5). On to Unit 6 (Plate Tectonics).
**Why:** full-year roll; this unit exposed verify-stage flakiness + an unstyled-class gap, both now closed.
**TVM:** base 11 × 3× (midday + building) ≈ **ƒ33 effective**.
