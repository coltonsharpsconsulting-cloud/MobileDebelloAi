---
tags:
  - vex
  - match
  - competition
  - debrief
event: "{{Event Name}}"
date: {{date}}
result: "{{Win | Loss | Tie}}"
score-us: 0
score-opp: 0
---

<style>
.match-header{border-radius:14px;padding:18px 22px;margin-bottom:20px;border:1.5px solid}
.match-header.win{background:rgba(0,255,136,.07);border-color:rgba(0,255,136,.3)}
.match-header.loss{background:rgba(255,34,68,.07);border-color:rgba(255,34,68,.3)}
.match-header.tie{background:rgba(255,238,0,.07);border-color:rgba(255,238,0,.3)}
.match-header h1{margin:0 0 4px;font-size:1.5em}
.match-header .meta{color:rgba(255,255,255,.45);font-size:.82em;letter-spacing:1.2px}
.score-display{display:flex;gap:16px;margin:14px 0;align-items:center}
.score-num{font-size:3em;font-weight:900;line-height:1}
.score-us{color:#00f5ff}
.score-opp{color:rgba(255,255,255,.4)}
.score-sep{font-size:1.5em;color:rgba(255,255,255,.2);font-weight:300}
.score-label{font-size:.7em;letter-spacing:1.5px;text-transform:uppercase;color:rgba(255,255,255,.35)}
.four-box{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin:14px 0}
.fbox{background:rgba(255,255,255,.025);border:1px solid rgba(255,255,255,.07);border-radius:10px;padding:14px}
.fbox h3{margin:0 0 8px;font-size:.82em;letter-spacing:1.2px;text-transform:uppercase;color:rgba(255,255,255,.4)}
.fbox p,.fbox ul{margin:0;font-size:.88em;color:rgba(255,255,255,.7);line-height:1.6}
.fbox ul{padding-left:16px}
.fbox.worked{border-color:rgba(0,255,136,.2)}
.fbox.failed{border-color:rgba(255,34,68,.2)}
.fbox.learned{border-color:rgba(0,245,255,.2)}
.fbox.changes{border-color:rgba(255,238,0,.2)}
.rating-row{display:flex;gap:8px;align-items:center;margin:6px 0;font-size:.85em}
.rating-row .rlabel{flex:1;color:rgba(255,255,255,.6)}
.stars{color:rgba(255,238,0,.8);letter-spacing:2px}
.divider{border:none;border-top:1px solid rgba(255,255,255,.07);margin:16px 0}
</style>

<div class="match-header {{win|loss|tie}}">
<h1>🏟️ {{Event Name}}</h1>
<div class="meta">{{date}} &nbsp;·&nbsp; Match debrief</div>
<div class="score-display">
<div>
<div class="score-label">Our Score</div>
<div class="score-num score-us">{{score-us}}</div>
</div>
<div class="score-sep">–</div>
<div>
<div class="score-label">Opponent</div>
<div class="score-num score-opp">{{score-opp}}</div>
</div>
</div>
</div>

← [[🏆 Competition Log]] | [[⚡ VEX Robotics MOC]] →

---

## 👥 Match Details

| Field | Value |
|-------|-------|
| Event | {{Event Name}} |
| Date | {{date}} |
| Match # | — |
| Alliance Partner | — |
| Opponents | — |
| Autonomous result | Win / Loss / Tie |
| Final result | **{{result}}** |

<hr class="divider">

## 📊 Performance Ratings

<div class="fbox" style="margin:12px 0">

<div class="rating-row">
<span class="rlabel">Autonomous routine</span>
<span class="stars">☆☆☆☆☆</span>
</div>
<div class="rating-row">
<span class="rlabel">Driver control — precision</span>
<span class="stars">☆☆☆☆☆</span>
</div>
<div class="rating-row">
<span class="rlabel">Driver control — speed</span>
<span class="stars">☆☆☆☆☆</span>
</div>
<div class="rating-row">
<span class="rlabel">Mechanical reliability</span>
<span class="stars">☆☆☆☆☆</span>
</div>
<div class="rating-row">
<span class="rlabel">Alliance coordination</span>
<span class="stars">☆☆☆☆☆</span>
</div>
<div class="rating-row">
<span class="rlabel">End-game execution</span>
<span class="stars">☆☆☆☆☆</span>
</div>

</div>

<hr class="divider">

## 🔍 Post-Match Debrief

<div class="four-box">
<div class="fbox worked">
<h3>✅ What Worked</h3>
<ul>
<li></li>
<li></li>
</ul>
</div>
<div class="fbox failed">
<h3>❌ What Failed</h3>
<ul>
<li></li>
<li></li>
</ul>
</div>
<div class="fbox learned">
<h3>💡 What We Learned</h3>
<ul>
<li></li>
<li></li>
</ul>
</div>
<div class="fbox changes">
<h3>🔧 Changes Before Next Match</h3>
<ul>
<li></li>
<li></li>
</ul>
</div>
</div>

<hr class="divider">

## 🗺️ Strategy Notes

> Use [[📍 Field Map]] to plan the next match. Document the planned autonomous path and driver priorities below.

**Autonomous plan:**
- 

**Driver priority order:**
1. 
2. 
3. 

**Alliance coordination:**
- 

<hr class="divider">

## 💬 Student Quotes

> Direct words from your students — these become the best coaching material later

*"{{student quote here}}"* — {{Student Name}}

<hr class="divider">

## 🔗 Connected Notes

- [[🏆 Competition Log]]
- [[📍 Field Map]]
- [[⚡ VEX Robotics MOC]]
- *Link to specific student profiles who competed*
