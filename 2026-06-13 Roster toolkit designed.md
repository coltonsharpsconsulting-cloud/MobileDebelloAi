---
title: "Roster toolkit designed"
date: 2026-06-13
allDay: false
startTime: "15:05"
endTime: "15:35"
area: "Design"
worth: 4
tvm: 2
by: claude
created: 2026-06-13 23:56
cssclasses:
  - nl-doc
---
Designed a **seat-map toolkit** for Madewell's classroom. Her ask: adjust seating on the fly, but keep it a **table, not a drag-and-drop canvas** — a seat-number → student-name mapping linked to the roster, with change **logging**. Wrote the spec and the implementation plan; the table-not-canvas constraint keeps it fast on a phone and auditable (every seat change leaves a record). Not built yet — design + plan only.

**Files:** `docs/superpowers/specs/2026-06-14-roster-toolkit-design.md`, `docs/superpowers/plans/2026-06-13-roster-toolkit.md`.
**Next:** implement per the plan (seat table + roster link + change log).
**Why:** seating is the one thing a sub or a fire drill needs *instantly*; a logged table beats a pretty canvas she can't trust. Ties to [[The Madewell Daily]] / her room surface.
**TVM:** base 4 × 2 (afternoon design) ≈ **ƒ8 effective**. See [[Value Engine]].
