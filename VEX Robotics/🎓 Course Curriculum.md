---
tags:
  - vex
  - curriculum
  - teaching
  - lesson-plan
created: 2026-06-02
---

<style>
.curr-header{background:linear-gradient(135deg,rgba(0,255,136,.08),rgba(0,128,255,.08));border:1.5px solid rgba(0,255,136,.22);border-radius:14px;padding:18px 22px;margin-bottom:20px}
.curr-header h1{margin:0 0 4px}
.curr-header p{margin:0;color:rgba(255,255,255,.45);font-size:.85em;letter-spacing:1px}
.unit{background:rgba(255,255,255,.025);border:1px solid rgba(255,255,255,.08);border-radius:12px;padding:16px;margin:12px 0}
.unit-header{display:flex;align-items:center;gap:10px;margin-bottom:10px}
.unit-num{width:32px;height:32px;border-radius:8px;background:rgba(0,245,255,.12);border:1px solid rgba(0,245,255,.3);display:flex;align-items:center;justify-content:center;font-weight:900;font-size:.85em;flex-shrink:0}
.unit-title{font-weight:700;font-size:1em;letter-spacing:.3px}
.unit-weeks{font-size:.75em;color:rgba(255,255,255,.35);letter-spacing:1px;text-transform:uppercase;margin-left:auto}
.lesson-list{list-style:none;padding:0;margin:8px 0 0}
.lesson-list li{padding:4px 0;font-size:.85em;color:rgba(255,255,255,.65);border-bottom:1px solid rgba(255,255,255,.04);display:flex;align-items:center;gap:8px}
.lesson-list li:last-child{border-bottom:none}
.lesson-list li::before{content:"→";color:rgba(0,245,255,.5);font-size:.8em;flex-shrink:0}
.phase-label{font-size:.7em;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;padding:3px 10px;border-radius:12px;display:inline-block;margin-bottom:12px}
.ph-build{background:rgba(255,102,0,.12);border:1px solid rgba(255,102,0,.3);color:#ff6600}
.ph-compete{background:rgba(255,34,68,.12);border:1px solid rgba(255,34,68,.3);color:#ff2244}
.ph-reflect{background:rgba(139,0,255,.12);border:1px solid rgba(139,0,255,.3);color:#b400ff}
.divider{border:none;border-top:1px solid rgba(255,255,255,.07);margin:20px 0}
.skills-grid{display:grid;grid-template-columns:1fr 1fr 1fr;gap:10px;margin:14px 0}
.skill-box{background:rgba(255,255,255,.03);border:1px solid rgba(255,255,255,.07);border-radius:9px;padding:12px;font-size:.82em}
.skill-box h4{margin:0 0 6px;font-size:.85em;letter-spacing:.8px;text-transform:uppercase;color:rgba(255,255,255,.6)}
.skill-box ul{margin:0;padding-left:14px;color:rgba(255,255,255,.5);line-height:1.7}
</style>

<div class="curr-header">
<h1>🎓 VEX VRC Course Curriculum</h1>
<p>Full-year course structure &nbsp;·&nbsp; Lesson plans &nbsp;·&nbsp; Skill progressions</p>
</div>

← [[⚡ VEX Robotics MOC]] | [[Templates/VEX Lesson Plan]] →

---

## 🎯 Course Learning Outcomes

By end of year, students will be able to:
- **Design & Build** — Apply engineering design process to build a competition-ready VRC robot
- **Program** — Write autonomous routines and driver-assist code in VEXcode V5
- **Compete** — Execute match strategy, adapt under pressure, work as an alliance partner
- **Collaborate** — Communicate effectively in a team, document their engineering process
- **Reflect** — Analyze performance data and make evidence-based improvements

<hr class="divider">

## 📅 Year at a Glance

<span class="phase-label ph-build">Phase 1 — Build & Learn (Aug–Oct)</span>

<div class="unit">
<div class="unit-header">
<div class="unit-num">01</div>
<div class="unit-title">Introduction to VEX & Engineering Design</div>
<div class="unit-weeks">2 weeks</div>
</div>
<ul class="lesson-list">
<li>What is VEX VRC? Season overview, game reveal, rules walkthrough — [[📍 Field Map]]</li>
<li>Engineering Design Process (EDP) — problem, ideate, prototype, test, iterate</li>
<li>VEX hardware overview: motors, sensors, brain, controller, structure pieces</li>
<li>Safety rules and lab procedures</li>
<li>Team formation and role assignment (driver, builder, programmer, captain)</li>
</ul>
</div>

<div class="unit">
<div class="unit-header">
<div class="unit-num">02</div>
<div class="unit-title">Drive Train Design & Build</div>
<div class="unit-weeks">3 weeks</div>
</div>
<ul class="lesson-list">
<li>Drive train types: tank drive, X-drive (holonomic), H-drive, mecanum</li>
<li>Gear ratios, torque vs. speed tradeoffs</li>
<li>Build first drive train — documented in [[Templates/VEX Robot Design]]</li>
<li>Driver practice — straight lines, precision turns, navigating obstacles</li>
<li>Measuring and optimizing: speed tests, pushing tests, turning radius</li>
</ul>
</div>

<div class="unit">
<div class="unit-header">
<div class="unit-num">03</div>
<div class="unit-title">Mechanisms — Intake, Lift & Scoring</div>
<div class="unit-weeks">4 weeks</div>
</div>
<ul class="lesson-list">
<li>Simple machines review: levers, gears, pulleys, linkages</li>
<li>Intake design for this season's game element (rings)</li>
<li>Lift mechanisms: 4-bar, 6-bar, DR4B, chain-bar</li>
<li>Iterative build sessions with testing checkpoints each week</li>
<li>Alliance partner compatibility — standard connection points</li>
</ul>
</div>

<div class="unit">
<div class="unit-header">
<div class="unit-num">04</div>
<div class="unit-title">Programming — Basics to Autonomous</div>
<div class="unit-weeks">4 weeks</div>
</div>
<ul class="lesson-list">
<li>VEXcode V5 environment — blocks vs. text (C++)</li>
<li>Basic driver control: tank drive, arcade drive, split arcade</li>
<li>Sensor integration: encoders, inertial sensor (IMU), limit switches</li>
<li>PID controller basics — why and how it works</li>
<li>Writing a 15-second autonomous routine — step by step</li>
<li>Debugging: logic errors vs. mechanical errors vs. sensor drift</li>
</ul>
</div>

<hr class="divider">

<span class="phase-label ph-compete">Phase 2 — Compete & Iterate (Nov–Mar)</span>

<div class="unit">
<div class="unit-header">
<div class="unit-num">05</div>
<div class="unit-title">Qualifying Tournaments</div>
<div class="unit-weeks">Oct–Jan</div>
</div>
<ul class="lesson-list">
<li>Pre-competition checklist — robot inspection criteria</li>
<li>Match strategy planning — use [[📍 Field Map]] for pre-match prep</li>
<li>Alliance communication — scouting other teams, selecting partners</li>
<li>Post-match debrief every week — [[Templates/VEX Match Notes]]</li>
<li>Iterative robot improvements between each event</li>
</ul>
</div>

<div class="unit">
<div class="unit-header">
<div class="unit-num">06</div>
<div class="unit-title">Advanced Programming & Skills</div>
<div class="unit-weeks">2 weeks</div>
</div>
<ul class="lesson-list">
<li>Odometry — tracking robot position on field</li>
<li>Path planning — smooth curves and waypoints</li>
<li>Programming Skills run optimization</li>
<li>Driver Skills run — peak performance strategies</li>
</ul>
</div>

<div class="unit">
<div class="unit-header">
<div class="unit-num">07</div>
<div class="unit-title">State Qualifier Preparation</div>
<div class="unit-weeks">2 weeks</div>
</div>
<ul class="lesson-list">
<li>Robot polish: clean wiring, secure connections, backup auton</li>
<li>Pit setup and presentation</li>
<li>Judge interview prep — Engineering Notebook review</li>
<li>Alliance selection strategy — data from [[🏆 Competition Log]]</li>
</ul>
</div>

<hr class="divider">

<span class="phase-label ph-reflect">Phase 3 — Reflect & Share (Apr–May)</span>

<div class="unit">
<div class="unit-header">
<div class="unit-num">08</div>
<div class="unit-title">Season Reflection & Knowledge Transfer</div>
<div class="unit-weeks">2 weeks</div>
</div>
<ul class="lesson-list">
<li>What did we build? What did we learn? What would we change?</li>
<li>Presentation to school/community — robot demo day</li>
<li>Documentation handoff — update [[Templates/VEX Robot Design]] for next year's team</li>
<li>Recruiting and mentoring incoming students</li>
</ul>
</div>

<hr class="divider">

## 🧠 Core Skills Taught

<div class="skills-grid">
<div class="skill-box">
<h4>Engineering</h4>
<ul>
<li>Design process</li>
<li>Mechanical systems</li>
<li>Prototyping</li>
<li>Testing & iteration</li>
<li>Documentation</li>
</ul>
</div>
<div class="skill-box">
<h4>Programming</h4>
<ul>
<li>Control flow</li>
<li>Sensor integration</li>
<li>PID control</li>
<li>Autonomous planning</li>
<li>Debugging</li>
</ul>
</div>
<div class="skill-box">
<h4>Soft Skills</h4>
<ul>
<li>Teamwork</li>
<li>Communication</li>
<li>Time management</li>
<li>Presentation</li>
<li>Resilience</li>
</ul>
</div>
</div>

<hr class="divider">

## 🔗 Connected Notes

- [[⚡ VEX Robotics MOC]] — Back to hub
- [[📍 Field Map]] — Game field reference
- [[🏆 Competition Log]] — Season results
- [[Templates/VEX Lesson Plan]] — Create individual lesson notes
- [[Templates/VEX Student Profile]] — Track student progress
