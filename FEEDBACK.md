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
| 2 | 2026-07-23 | Udit Parikh (personal network) | 🎨 + 📊 + 👍 | Tech great; "milk" shows bottle not the sign; unclear who it's for; broaden audience?; punch up tech copy | 🔴 open |
| 1 | 2026-07-20 | Early tester (competition) | 🐛 + 👍 | Demo great; camera-flip ×2 silently kills hand detection | 🟢 actioned |

---

## Entries

### #2 — 2026-07-23 · Positioning + "show the sign" gaps
- **Who / source:** Udit Parikh (personal network — likely WhatsApp/personal share; *not* a target parent)
- **Type:** 🎨 UX/product + 📊 demand/positioning (+ 👍 praise)
- **Feedback (verbatim):**
  > - the actual tech/recognizing video and instructions are great! The milk one did not show the sign
  >   just showed the bottle so was confused for a second, but overall the camera function and
  >   recognizing worked great!
  > - I think on the main page… it needs to better come across who this product is for… I did not
  >   realize until later that this is for parents of deaf/hard to hear kids. I would make it front and
  >   center … something like… 'do you struggle with ASL while communicating with your loved one
  >   impaired of hearing? Check out this online coach that makes you an expert in 2 weeks!'
  > - Also, can't this be a use case for anyone wanting to communicate with deaf people, why just
  >   parents and children?
  > - Need to make the tech sound as cool as it is… something like … 'our AI assisted hand recognition,
  >   unique technology allows you to track exact movements and coach you through perfecting signs for
  >   each word/sentences'
- **Breakdown & read:**
  1. 🎨 **"Milk shows a bottle, not the sign"** — real gap: the demo names the target + a 🍼 emoji but
     never *shows how to form the sign*. Users don't know the handshape/motion up front. **Fix:** add a
     visual/textual reference of each sign (reference image or step description) next to the target.
     High-value, do it. → 🟡
  2. 🎨 **"Unclear who it's for"** — valid; a non-target user missed the audience. Strengthen the hero to
     put the parent audience + value prop front-and-center. (Temper the "expert in 2 weeks" overpromise —
     don't claim outcomes we can't back.) → recommend acting.
  3. 📊 **"Why just parents — isn't this for anyone communicating with deaf people?"** — matches our own
     **pivot thesis / Market Landscape** in `PROJECT.md` (parents = beachhead; broader market = general
     learners). Decision for now: **keep the focused parent message for the demand test** (narrow
     converts + it's the health-equity wedge); log as a strong signal that broadening resonates —
     candidate A/B later. → parked-by-design (revisit post-test).
  4. 🎨 **"Make the tech sound as cool as it is"** — easy win: add an AI/CV capability line. → do it.
- **Action taken:** _pending — see recommendations discussion 2026-07-23._
- **Status:** 🔴 open

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
