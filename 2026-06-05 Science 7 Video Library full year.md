---
title: "Science 7 Video Library — full year, 49 verified shorts (multi-agent)"
date: 2026-06-05
allDay: false
startTime: "10:30"
endTime: "12:10"
area: "Build"
worth: 16
tvm: 3
by: claude
created: 2026-06-05 12:14
cssclasses:
  - nl-doc
---
Built a **vault-native library of 49 short, real, verified review videos** for [[7th Grade Integrated Science]] — one or more per concept across **all 9 units**, every one confirmed **live and ≤ 5:00** (longest 4:59, shortest 2:02). **Zero gaps, zero dead links.** The ask: a publishable list of "YouTube shorts" a student can watch in the car, at lunch, or walking to class — mapped to the topics and AZ standards actually taught.

**Toolchain first (TDD, three stdlib-only scripts, 15 tests green).** `video-verify.py` is the honesty gate — existence + canonical title/channel/thumb via YouTube's public **oEmbed** endpoint, duration via the watch page's `lengthSeconds`, no API key; a video only enters the library if the CLI returns `ok:true` (live + ≤300s). `derive-video-slots.py` turns the curriculum seed + the vault Week notes (phenomenon + vocab focus) into draft concept slots. `gen-video-library.py` mirrors `gen-curriculum-map.py` — reads the canonical JSON and emits one atomic note per video (YAML frontmatter, tap-to-watch thumbnail, blurb, and **backlinks to its Week / Unit / Standard** so each clip joins the existing graph) plus a Dataview index. A code-review pass caught real YAML-escaping bugs (unquoted `concept:`/`vocab:` would break frontmatter on any colon/comma) — fixed with a regression test before generating anything.

**Then the curation, multi-agent.** Unit 1 ran as a human-gated slice: 8 parallel concept searchers, each forced to verify candidates through the CLI (no invented IDs), then an independent batch re-verify. After sign-off, **8 parallel unit searchers** (best-fit channel per topic) sourced Units 2–9 — 41 more videos. Every one of the final **49 was re-verified from scratch** as the integrity net: all live, all ≤5:00, durations matched. Channel mix landed diverse and reputable: Khan Academy MS Physics/Bio 13 · FuseSchool 12 · Crash Course Kids 7 · SciShow Kids 5 · National Geographic 4 · MooMooMath 4 · Free School 2 · TED-Ed 1 · HRB Education 1. Two best-fit exceptions outside the core channel list are flagged in-note (convection currents → HRB; ocean currents → TED-Ed), plus three concept `note`s where a clip covers the idea but not a secondary angle.

**Vault is the source of truth, Dataview is the lens** (as specified): the per-video notes carry the data; the index queries them; the JSON seed sits beside the curriculum seed so the science-7 site can render the same data later. Edit the JSON → re-run the generator (idempotent); re-run the verifier any time to audit link-rot in one command.

**Files:** `scripts/video-verify.py`, `scripts/derive-video-slots.py`, `scripts/gen-video-library.py` (+ `tests/test_*` ×3, 15 tests); `web/TeacherCheckOutSystem/data/science-7-video-library.seed.json` (canonical, 49 videos); vault `[[Curriculum/7th Grade Integrated Science/Video Library|Video Library]]/` (49 notes) + `Video Library.md` index; `## Watch` on the course hub + `## Video Library` on [[Curriculum Dashboard]]; spec + plan in `docs/superpowers/{specs,plans}/2026-06-05-science-7-video-library*`.
**Why:** "a fully publishable list of YouTube shorts based off topic material and standards taught" — bite-size review, on-the-go, accuracy-verified, regenerable.
**TVM:** base 16 × 3× (midday + building) ≈ **ƒ48 effective**.
