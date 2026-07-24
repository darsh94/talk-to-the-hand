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
| 3 | 2026-07-23 | Rob Neal (mentor / personal network) | 📊 + 🎨 | Reframe site around PROBLEM + CUSTOMER (not the AI solution); adopt *The Mom Test* for interviews; domain `talkingtohands.com`; milk instructions unclear (again) | 🟢 actioned (rebrand parked) |
| 2 | 2026-07-23 | Udit Parikh (personal network) | 🎨 + 📊 + 👍 | Tech great; "milk" shows bottle not the sign; unclear who it's for; broaden audience?; punch up tech copy | 🔴 open |
| 1 | 2026-07-20 | Early tester (competition) | 🐛 + 👍 | Demo great; camera-flip ×2 silently kills hand detection | 🟢 actioned |

> **⚠️ Convergent signals (2+ independent sources) — highest priority:**
> - ✅ **"Milk" instructions unclear** — #2 (Udit) + #3 (Rob) → **fixed** 2026-07-23: added a "How to
>   sign it" step guide (hand-emoji motion) to every sign, with a "🍼 is just the word" note.
> - ✅ **Site too solution-focused; unclear who it's for** — #2 + #3 → **fixed** 2026-07-23: landing
>   reframed problem-first / customer-first.

---

## Entries

### #3 — 2026-07-23 · Reframe around problem + customer; fix how you ask for feedback
- **Who / source:** Rob Neal (personal network — startup/marketing mentor). Voice memo → speech-to-text.
- **Type:** 📊 demand/positioning + 🎨 marketing/process (+ small 🐛 product note)
- **Feedback (key points; condensed from a spoken transcript):**
  1. **Obsess over the PROBLEM, not the solution.** *"Your website is mostly focused around the
     solution [the AI that tracks your hands]… your customers don't care. You want to obsess and talk
     a lot about the problem — learning how to talk with your hands for your little one."*
  2. **Obsess over the CUSTOMER: parents of deaf kids.** *"Be more obsessed with your customer than
     your product. The problem is learning sign language (aka talk to hands); who it is: parents with
     children who are deaf."* Clear customer → clearer ask for intros (*"do you know anyone with someone
     deaf in their life trying to learn to communicate with them?"*).
  3. **Brand vs. category:** *"Talking To Hands"* is just branding around ASL (like Frosted Flakes vs.
     "frosted corn flakes"); the real focus is the problem = learning sign language. Suggests grabbing
     the domain **`talkingtohands.com`** (preferred "Talking With Hands" but taken since 2012).
  4. **Reposition around the top pain points** parents hit learning ASL — find the top ~10, lead with
     the top 3, thread the rest down the page.
  5. **Fix how you ask for feedback — read *The Mom Test*.** *"Right now you're asking people to lie to
     you… tell you how awesome your product is."* Instead ask about current behavior: *"How are you
     currently solving this? What are you currently paying for it?"* → reveals if it's a real, painful,
     **payable** problem. Also refs *Buyer Personas*, *Demand-Side Sales*, patternsandmarketing.com.
  6. **Positioning > product:** people must believe it's worth their *time* (to use) and *money* (to
     buy). *"Cure for cancer dressed like they're homeless — you wouldn't believe them; put them in a
     lab coat…"* Lead by talking about their problem confidently; skip your solution and your hard work.
  7. **Product note (marketing aside):** *"I love you is good. I got stuck on milk — instructions
     weren't as clear."* Curious how difficulty/curriculum progresses. (Didn't deep-test the product.)
- **Read / decisions:**
  - Reframe landing copy **problem-first + customer-first**, de-emphasize the AI/coach mechanics —
    strong, and *converges with #2*. → act (propose new copy for review).
  - **Adopt Mom Test framing** — our `OUTREACH_KIT.md` interview script already leans this way (asks
    current tools/spend, avoids "would you pay"), but audit it against the book's rules and tighten. → act.
  - **Milk instructions** — same as #2; fix the "how to sign it" reference. → act.
  - **Domain `talkingtohands.com`** + possible rebrand ("Talk to the Hand" → "Talking to Hands") —
    strategic/brand call for the user. → decision pending.
  - **Broaden vs. narrow** — Rob *reinforces the parent-first focus* (unlike Udit's "why just parents");
    good — confirms keeping the parent beachhead for the test.
- **Action taken (2026-07-23):** ✅ **Landing page reframed problem-first / customer-first** — new hero
  ("Your child is learning to sign. Learn to sign back."), tech "how it works" steps replaced by 3
  emotional parent pain points, AI demoted to one credibility line, CTA + title/OG updated
  (`landing/index.html`). ✅ "Milk"/all-sign instructions fixed — added "How to sign it" motion guides.
  ✅ **Mom Test audit** of the interview script done — removed the 3 hypothetical/"would-you-pay"
  questions, reframed to past behavior + currency (time/money already spent) + a commitment ask
  (email/deposit/intro); added a Mom Test rules primer (`OUTREACH_KIT.md` §3–4).
  ✅ **Domain/rebrand decision (2026-07-23): PARKED.** Keep "Talk to the Hand" for now — a rename touches
  the repo, live URL, analytics, and everything already shared (real switching cost) and doesn't change
  what the demand test measures. Revisit branding *after* signup numbers justify the investment. (May
  grab `talkingtohands.com` defensively later without committing to a rename.)
- **Status:** 🟢 actioned (rebrand parked by decision)

### #2 — 2026-07-23 · Positioning + "show the sign" gaps

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
- **Action taken (2026-07-23):** ✅ Landing reframed problem/customer-first (points 2 & 4 — the tech now
  reads as one credibility line). ✅ Point 1 fixed — added a "How to sign it" step guide (hand-emoji
  motion) to each sign in the demo, with an explicit "🍼 is just the word" note. Point 3 (broaden)
  parked-by-design (revisit post-test).
- **Status:** 🟢 actioned (broaden parked by design)

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
