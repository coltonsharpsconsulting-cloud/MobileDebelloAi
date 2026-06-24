---
title: "Lesson Faces · Science Hub"
date: 2026-06-08
allDay: false
startTime: "19:36"
endTime: "19:56"
area: "Build"
worth: 8
tvm: 4.5
by: claude
created: 2026-06-10 16:05
cssclasses:
  - nl-doc
---
Built Nikki's public **7th-Grade Science Hub** end-to-end: one vault lesson-plan JSON now renders three static "faces" — a **Board** view (project on the screen), a **Worksheet** view (what students fill in), and a **Canvas announcement embed** with a copy button — via `scripts/gen-lesson-faces.py`, then publishes to GitHub Pages with `scripts/publish-science-hub.sh`. Answer keys stay private in the vault; only the faces go public. Wrote a `shot.mjs` screenshot harness to verify each face renders before publish, and a `.env` for the repo token. Shipped live on GitHub Pages at `TeacherMadewell/7th-Grade-Science-Hub-` once Pages was enabled (06-10).

**Files:** `scripts/gen-lesson-faces.py`, `scripts/publish-science-hub.sh`, `scripts/shot.mjs`, `~/.config/madewell-science-hub/.env`, design spec `docs/superpowers/specs/2026-06-08-lesson-faces-pilot-design.md`.
**Why:** Nikki needed her Science 7 lessons to exist in three forms without authoring them three times — one source file, three audiences (board, student, Canvas). `.nojekyll` required; token needs Pages:write. This generator becomes the spine the bell-work faces later plug into.
**TVM:** base 8 × 4.5 (evening 2.5× +2 built-for-you) ≈ **ƒ36 effective**. See [[Value Engine]].
