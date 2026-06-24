---
cssclasses:
  - nl-doc
---
<span class="nl-eyebrow">system · comings & goings</span>
# Build Log

[[Colton|← builder]]  ·  [[Deb-Coin|the mint →]]  ·  what the system built **without you lifting a finger** — every session logged in and out, valued by scope, categorized by the *kind* of work, then TVM-weighted. The machine keeps its own running score; this is the record. For the same coins seen as **daily density**, open [[Deb-Coin]].

## Sessions
```dataview
TABLE WITHOUT ID file.link AS Session, date AS When, area AS Type, startTime + "–" + endTime AS Window, ("ƒ" + worth) AS Base, ("×" + tvm) AS TVM
FROM "Build Log"
WHERE by AND file.name != "Build Log"
SORT date DESC, startTime DESC
```

## By work-type — Value Index
TVM-weighted florins (base worth × time-value multiplier). See [[Value Engine]].
```js-engine
return (await engine.importJs("Scripts/ledger.js")).render({app, component, engine}, {folder:"Build Log", title:"BUILT FOR YOU · FLORINS BY TYPE", building:"all", lsKey:"wledger.period", empty:"No sessions logged yet."});
```
