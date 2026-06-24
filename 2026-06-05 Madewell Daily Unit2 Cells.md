---
title: "Madewell Daily — Unit 2 (Cells) generated, no-repeat enforced"
date: 2026-06-05
allDay: false
startTime: "12:15"
endTime: "12:30"
area: "Build"
worth: 11
tvm: 3
by: claude
created: 2026-06-05 12:30
cssclasses:
  - nl-doc
---
Generated **all of Unit 2 — Cells** (Science 7, Weeks 6–9) in one background Workflow: **18 issues, Sep 1 → Sep 25** (Topic Launch → living/nonliving → cell theory → organelles → plant-cell models → careers → tree-mass/photosynthesis → Reteach → the **Unit 2 Assessment** study-guide). Scout correctly skipped the No-School Mon (Aug 31) and Labor Day. 37 agents, ~1.38M tokens, **~10.5 min** (Unit 1 took 28 — pipeline's warm now).

**The no-repeat fix landed and worked.** Unit 1's two puzzle drifts both traced to the *"science riddle"* assignment — writers didn't know the format and fell back to a crossword/cipher, colliding within the week. Unit 2's writers got (a) a per-week-distinct type assigned in code, (b) a hard "make EXACTLY this type, here are your week's reserved types, no substitution," and (c) an explicit format spec per puzzle type. Result: **all four weeks carry fully distinct puzzles with zero post-run cleanup** — riddles honored on Sep 3 (MICROSCOPE) and Sep 16, no drift. Both crosswords (Sep 10, Sep 22) validated programmatically — run-lengths match declared clue lengths, every run numbered, no orphans.

**Verification — 18/18 PASS** (3 fixed in place: a Labor-Day-date error on the Sep 1 issue, plus two minor science/SVG fixes). My own gate: every issue has both SVGs, green-leaning life-science palette (Stratosyn-only), zero placeholders, no invented classes. Real hooks were genuinely sourced (Stanford iISM label-free microscopy, Perseverance "Cheyava Falls" biosignature, Valonia "sea pearl" giant cell).

**Files:** `The Madewell Daily/2026-09-01 … 2026-09-25` (18 issues); Workflow `madewell-daily-unit2-cells`. Library now **38 issues** (Units 1–2). Next: Unit 3 (Human Body Systems, Weeks 10–13) or the Launch Week template.
**Why:** "knock out the entire year via sub-agents" — Unit 2 clean on the first pass thanks to the hardened pipeline.
**TVM:** base 11 × 3× (midday + building) ≈ **ƒ33 effective**.
