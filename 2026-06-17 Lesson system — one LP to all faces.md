---
title: "Lesson system — one LP → Board · Worksheet · Plan · Bell Work"
date: 2026-06-17
allDay: false
startTime: "11:30"
endTime: "17:20"
area: "Build"
worth: 13
tvm: 4
by: claude
created: 2026-06-17 17:20
cssclasses:
  - nl-doc
---
The day the **in-class "middle" got built** — the part of a teaching day that wasn't there yet (the Dailies, bell work, videos, year outline already existed). Designed it as a spec, then built it across **three subagent-driven plans (~30 agents, two-stage review + a final-review fix pass each)**. The architecture: a single **Lesson Plan JSON is the hub**, and generators turn it into every face — so one source, everything regenerates and stays linked.

What now generates from `LP-2026-08-03.json` via **one command** (`scripts/build-lesson.mjs`):
- **Student Worksheet** (`gen-worksheet.mjs`) — sectioned interactive app; **all closed questions selectable** (dropdown/mc/true-false — no spelling to grade); instant **SHA-256 self-check** (keys never in the page, only hashes); **embedded PhET Coulomb's Law sim** the kids drive; **Download-my-work → a fully-formatted `.md`** (YAML frontmatter, auto-score line, named file) — **no server, no Wi-Fi** (Canvas is the only network touch); a **paper print fallback** (Procedures §15). Proven end-to-end with Playwright.
- **Projected Board** (`gen-board.mjs`) — a **button-navigated** app (never scrolls), one screen per agenda phase, **embedded Khan video + PhET sim** inline, per-phase **countdown + live clock**, volume badges, the **"Scientists!/Ready!"** cue; display-only (no answers leak).
- **Teacher Lesson-Plan** (`gen-lesson-plan.mjs`) — the run-sheet: timed agenda, asset links, and **the answer keys** (teacher-only, the single place they appear).
- **Bell Work** rides the **same `.md` download** via a thin adapter (`bellwork-adapt.mjs`) — one turn-in motion everywhere.
- An original **full-length source reading article** (`Readings/2026-08-03 Electric Forces.md`, ~1000 words + drawn SVG) — ours, the text the Daily digests.

The riskiest unknown — *"how do you collect answers from a static page with no server"* — was de-risked early with a working proof: client-side Blob download of a vault-native Markdown file. That unlocked the whole no-server model.

**Files:** `scripts/{gen-worksheet,gen-board,gen-lesson-plan,build-lesson,bellwork-adapt}.mjs` + `scripts/lib/{lp-schema,ws-render,board-render}.mjs` + `scripts/assets/{ws,board}.css` + `scripts/assets/{ws-runtime,board-runtime}.js` + verifiers; vault `Lessons/W2-D1/{worksheet,board}.html + lesson-plan.md`, `Bell Work/W2-D1/bellwork.html`, `Readings/2026-08-03…md`; self-hosted PhET sim in `web/science-hub/sims/`. Specs/plans in `docs/superpowers/{specs,plans}/2026-06-17-madewell-*`.
**Gated (await Colton's OK):** publish to the Science Hub (public Pages) + rewrite Procedures §3/§6/§8 (Copy→paste becomes Download→upload). **Nikki reviews** the question wording + keys before go-live.
**Why:** a day only runs if the teacher has the *lesson* — board, activity, plan — not just homework. Making the LP the one authority means the whole day is generated, consistent, and regenerable, and the no-server `.md` model finally beats the school-Wi-Fi problem that killed every server idea. See [[madewell-lesson-system]] · [[madewell-daily]] · [[Value Engine]].
**TVM:** base 13 (full design + a reusable 3-face generator system + the no-server submission + the proven PhET embed, across 3 plans) × 4 (long afternoon-into-evening build) ≈ **ƒ52 effective**.
