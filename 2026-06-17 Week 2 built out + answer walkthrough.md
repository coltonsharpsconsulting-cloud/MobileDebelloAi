---
title: "Week 2 built out + answer walkthrough"
date: 2026-06-17
allDay: false
startTime: "18:00"
endTime: "23:10"
area: "Build"
worth: 9
tvm: 5
by: claude
created: 2026-06-17 23:10
cssclasses:
  - nl-doc
---
First the **feature** Colton asked for: a *"Check before the sim"* answer-walkthrough that turns the I-do into a bridge — **video → lock the two dials with Q&A → predict in the sim**. On the **Board** it's a new screen where each question's answer + a one-line *why* reveals on click (teacher-paced); on the **Worksheet** it's lockstep — kids commit a dropdown, then "Go over the answers" reveals each correct one + why. Added an `explain` field + a `check` section/phase; the answers-in-page tradeoff is contained to the check block (graded practice/exit stay hashed + answer-free).

Then **the rest of Week 2**. Authored the four remaining LPs in parallel (sonnet agents, one per day, each reading its Daily + picking its library video): **D2** Electric Forces—apply (smokestack), **D3** analyze-your-data, **D4** review + quiz (assessment — no reveal, simpler 5-phase board), **D5** Magnetic Forces (different content + a second self-hosted sim, PhET **Magnet & Compass**). Made both verifiers **structure-agnostic** so they pass the 8-phase lessons AND the 5-phase quiz day, and made `build-lesson` copy the right sim per-LP. Renumbered the week to a coherent **W2-D1…D5 (Mon–Fri)** to match Colton's "Lesson 1–5" framing. Built + verified + **published all five** — worksheet/board live, `lesson-plan.md` 404 (keys private), leak-audited clean — and they **auto-list in the course + Madewell hubs** by the `#lesson` Dataview.

**Files:** `scripts/{gen-worksheet,gen-board,build-lesson}.mjs`, `lib/board-render.mjs`, `assets/{ws,board}.css + {ws,board}-runtime.js` (check feature); `verify-{worksheet,board}.mjs` (now generic); `web/science-hub/sims/magnet-and-compass_all.html` (new); vault `Lessons/LP-2026-08-0{4,5,6,7}.json` + `W2-D{2,3,4,5}/` faces + launchpads. All 5 live on the hub.
**Open:** **Nikki reviews** all 5 lessons' questions/keys (the agents' wording) before students use them; the Procedures `.docx` still needs a regen to match the `.md`.
**Why:** one perfect lesson proves the system; a whole coherent **week** proves it *scales* — author an LP, run one command, it's verified, live, and navigable. The check-walkthrough was the missing pedagogy (watch → check → apply).
**TVM:** base 9 (a real feature across both faces + 4 authored lessons + generic verifiers + a 2nd sim) × 5 (long night build) ≈ **ƒ45 effective**. See [[madewell-lesson-system]] · [[Value Engine]].
