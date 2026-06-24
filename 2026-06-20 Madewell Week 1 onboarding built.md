---
title: "Madewell Week 1 — pure-onboarding launch built"
date: 2026-06-20
allDay: false
startTime: "09:30"
endTime: "12:50"
area: "Build"
worth: 15
tvm: 3
by: claude
created: 2026-06-20 12:50
cssclasses:
  - nl-doc
---
Built **Week 1 — the 3-day pure-onboarding launch** (Jul 29–31) for Madewell's Science 7, the last piece before the year can roll forward. Colton chose **pure onboarding** (no science content; the static-electricity "wow" held back so Week 2 opens hot) and a **week-by-week-then-unit-batch** rollout cadence. The discovery that reframed the whole year: **all 39 week-seeds already exist** (phenomenon · sim · lab · assessment · vocab), so the rest of the year is *expand seed → daily faces*, not author-from-scratch.

Each day → **Board · Worksheet · Launchpad · Lesson-Plan**, reusing the proven Week 2 pipeline. **Day 1** = welcome + the 3 promises + core-procedures live-practice + "Scientist About You" survey. **Day 2** = lab-safety spot-the-hazard + the Safety Contract + science-notebook setup + §10 behavior + an Index-Card-Tower team challenge that drills the routines. **Day 3** = beginning-of-year **diagnostic** (read-the-graph, claim-evidence, living/non-living, prior knowledge) + goal-setting + how-the-year-runs.

Only real new code: **two generic, data-driven board screens** — `slide` (eyebrow/heading/bullets/note) and `practice` (live do-it-now steps + cue) — fed from each agenda item's `content` (the renderers now take a 3rd arg `a`), plus a `bellwork` `a.content` branch for procedural do-nows and a launchpad bell-work-link that prefers an explicit note. Reusable for every future launch/refresher week. The **worksheet generator was untouched** (it already renders arbitrary sections + closed/short questions); onboarding LPs validate as-is because `assets.sim/video/reading` are optional. Added a `console.warn` on unknown board-screen keys (review catch — guards the year's LP authoring against typos that silently blank a slide).

Bell work: archived the 3 redundant electric do-nows (Week 2 already carries electric content) to `_retired-from-wk1/` and authored **3 onboarding do-nows** — name-tent, copy-objective-+-3-safety-things, and read-the-graph (with a drawn bar-graph SVG) — via the system's documented launch-week inline-phenomenon path; renamed the 3 notes. There is intentionally **no Week 1 Daily** (onboarding has no content Daily — exactly why `bellwork.js` has the launch-week fallback).

Run through the **subagent pipeline** (implementer + spec + code-quality review): the board code came back APPROVED; the content review caught a missing spec-mandated diagnostic short-response (added `d8` "explain the graph") and polished two distractors. All three days build green (Playwright board + worksheet verifiers), every closed answer hashes to a real option, no answer-key leak (SHA-256 only), and the diagnostic shows zero answer-reveals.

**Files:** `scripts/lib/board-render.mjs` (+`slide`,`practice`,`bellwork` a.content); `scripts/gen-board.mjs` (pass agenda item + unknown-screen warn); `scripts/gen-lesson-index.mjs` (explicit bell-work note); `scripts/verify-board-render.mjs` (+8 asserts); `Lessons/LP-2026-07-{29,30,31}.json` + generated `W1-D{1,2,3}/` faces + launchpads; `Bell Work/source/2026-07-{29,30,31} *.json` (+ `_retired-from-wk1/`); spec + plan under `docs/superpowers/`.
**Why:** the launch week is the on-ramp — walk out Friday with a fully-procedured, safe, baseline-assessed class that can hit Unit 01 cold on Aug 3. The pure-onboarding template + the rollout doctrine turn the remaining ~37 weeks into a repeatable expand-and-review.
**Note:** **Published LIVE** to the Science Hub at session end (Colton authorized) — board + worksheet for W1-D1…D3, keys/lesson-plan + reading correctly 404, Week 2 preserved, all faces HTTP 200. Colton + Nikki still hand-review Weeks 1 & 2 before rolling Unit 01 forward (re-publish after any edits). Flag for Nikki: diagnostic `d7` (push/pull → "force") is a borderline prior-knowledge probe — confirm it fits her students' 6th-grade background. Also earlier this session (Fix): restored a blanked `Nikki.md` + cleaned the meal-log collateral; the Meal-log Templater bug had already been patched with a safety guard.
**TVM:** base 15 × 3 (daytime build) ≈ **ƒ45 effective**. See [[Madewell]] · [[madewell-lesson-system]] · [[Value Engine]].
