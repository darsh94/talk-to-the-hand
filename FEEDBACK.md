# Talk to the Hand — Feedback Log

Every piece of feedback we get: **who** gave it, **what** they said (verbatim where possible),
what **type** it is, and what we **did** about it. Newest at the top. Feeds product decisions
*and* the demand-test read (see `PROJECT.md` §Success metrics).

## Legend
- **Type:** 🐛 bug · 🎨 UX/product · ➕ feature request · 📊 demand/positioning · 👍 praise
- **Status:** 🔴 open · 🟡 in progress · 🟢 actioned · ⚪ parked / won't fix

## Index
| # | Date | Who / Source | Type | Summary | Status |
|---|------|--------------|------|---------|--------|
| 1 | 2026-07-20 | Early tester (competition) | 🐛 + 👍 | Demo great; camera-flip ×2 silently kills hand detection | 🟢 actioned |

---

## Entries

### #1 — 2026-07-20 · Camera-flip kills detection
- **Who / source:** Early tester via the Half Baked competition (build-in-public feedback)
- **Type:** 🐛 bug (+ 👍 praise)
- **Feedback (verbatim):**
  > great idea, and demo works well overall! 👏
  > One potential bug is that after clicking flip camera twice, hand recognition stopped working even
  > though the UI still shows auto-detect enabled and camera running. I tried start over to reset, but
  > hand recognition didn't come back. Might be worth checking whether the camera flip is properly
  > reattaching the video stream to the detection loop, and whether start over is fully reinitializing
  > the camera/model vs. just resetting the UI state.
- **Action taken:** Root cause = `detectForVideo()` threw on the 0×0 frame mid camera-swap; the
  uncaught throw killed the render loop. Fixed in `landing/demo.html` — resilient loop (try/catch +
  readiness guard + always reschedule) and clean camera swap (acquire-before-stop, await dimensions,
  reset timestamp). Commit `2c845d7` (2026-07-20), deployed.
- **Status:** 🟢 actioned

<!--
TEMPLATE — copy for each new entry:

### #N — YYYY-MM-DD · <short title>
- **Who / source:** <name / role / handle> via <channel: competition Slack, Reddit r/x, FB group, WhatsApp, parent interview, ...>
- **Type:** 🐛 / 🎨 / ➕ / 📊 / 👍
- **Feedback (verbatim):**
  > <paste exactly what they said>
- **Action taken:** <fix / change / decision — link commit; or "parked because ...">
- **Status:** 🔴 / 🟡 / 🟢 / ⚪
-->
