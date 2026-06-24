---
title: "W2-D1 live on the hub + turn-in unified"
date: 2026-06-17
allDay: false
startTime: "17:20"
endTime: "17:55"
area: "Build"
worth: 4
tvm: 4
by: claude
created: 2026-06-17 17:55
cssclasses:
  - nl-doc
---
Took the lesson **outward**. Wrote `scripts/publish-lesson.mjs` — a *safe* publisher (never stages `lesson-plan.md`, **aborts** if any answer key would leak, preserves other lessons rather than wiping the tree, pushes as Ms. Madewell via the env token) — and put **W2-D1 live** on the Science Hub: board, worksheet, and a freshly HTML-ified reading article. **Audited every live page**: no "Answer Key", no `data-answer`, every `data-key` a 64-hex hash, and `lesson-plan.md` returns **404** — the keys stay private. Also rewrote the **Classroom Procedures §6/§8** from `Copy → paste into Canvas` to **`Download my work → upload the file`**, so the room has one turn-in motion everywhere (the paired `.docx` still needs a regen to match).

**Files:** `scripts/publish-lesson.mjs`; live `teachermadewell.github.io/7th-Grade-Science-Hub-/lessons/W2-D1/{worksheet,board,reading}.html`; `BOYD Docs/…Classroom Procedures.md` §6/§8.
**Why:** a lesson that only lives on my disk can't be taught. Publishing the student faces (keys provably excluded) and aligning the written procedure to the new download turn-in is what makes the system real for her room.
**TVM:** base 4 × 4 (evening outward-ship + the safe-publish guardrails) ≈ **ƒ16 effective**. See [[madewell-lesson-system]] · [[Value Engine]].
