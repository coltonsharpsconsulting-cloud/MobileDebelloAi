---
title: "Bellwork accountability engine"
date: 2026-06-11
allDay: false
startTime: "11:34"
endTime: "21:14"
area: "Build"
worth: 8
tvm: 3
by: claude
created: 2026-06-11 21:14
cssclasses:
  - nl-doc
---
Designed and built the **bell-work do-now system** as the accountability engine for the Madewell Daily — the first modular stepping-stone of the full curriculum-delivery stack. The flip: the week's **five Dailies become homework, published Friday afternoon** (weekend runway = equity for athletes who can't read on weeknights), and each day's do-now draws on *that day's* Daily so the reader walks in performing and the non-reader is visibly stuck. One **shared phenomenon** is defined once in the lesson file and consumed by both bell work and the Daily, so they can't drift.

Two-tier structure: **Tier 1 Notice/Wonder** (open response, full credit, no wrong answer — protects the struggling kid) and **Tier 2 Reader's edge** (closed-form `mc`/`fill` with a hashed answer key, auto-checked red/green — rewards reading). Grading is **~5% hidden weight**: high perceived stakes, low real stakes, so kids try without anyone getting buried. Wired into the **live** `gen-lesson-faces.py` (`bw_hash`/`bw_norm`, `parse_bellwork`, `bellwork_hero_html`, `bellwork_worksheet_html`, `assert_sanitized`) — answers ship as hashes, never literal text — plus a **Board hero + management-only timer** and a client `bellwork-check.js`. Authored the **Week 01 static-electricity pilot** (3 day-types) and a follow-on Week-02 lean wire-up plan. Tests at `scripts/tests/test_bellwork.py`.

**Files:** specs `docs/superpowers/specs/2026-06-11-bellwork-design.md` + `…-bellwork-daily-wireup-design.md`, plans `…/plans/2026-06-11-bellwork.md` + `…-bellwork-daily-wireup.md`, `scripts/gen-lesson-faces.py` (bellwork mode), `scripts/tests/test_bellwork.py`, Week 01 LP + `Curriculum/Madewell/Bell Work/`.
**Why:** Nikki needed something on the screen the instant students walk in — no dead air — and a mechanism that makes reading the Daily *pay off* without policing. The hidden weight is what makes "feels graded" and "nobody gets buried" both true at once.
**TVM:** base 8 × 3 (afternoon 1× +2 built-for-you) ≈ **ƒ24 effective**. See [[Value Engine]].
