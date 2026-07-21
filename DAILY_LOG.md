# Talk to the Hand — Daily Log

A chronological work log for the project. Strategic state lives in `PROJECT.md` (§Session Log);
this file is the human-readable "what we actually did each day."

---

## 2026-07-12 — Kickoff, validation plan, and first build

**Framing:** role = serial healthcare-domain founder; entering the **Half Baked** 10-day hackathon.
Idea = a webcam ASL coach that grades hand shape/speed to beat the "Mirror Limit."

### Research & brainstorm
- Sized the market: ~500K ASL primary users, 6.4–7M signers, $3–10B sign-language economy.
- Reframed the buyer to **hearing learners**; chose the beachhead: **hearing parents of deaf children**
  (90%+ of deaf kids born to non-signing parents → health-equity urgency).
- Competitor read: Lingvano "Sign Mirror" and ASL Bloom address the *feeling* of the Mirror Limit,
  **not** true CV pose grading → that gap is our wedge ("They give you a mirror. We give you a coach.").
- Confirmed the tech is trivially buildable: MediaPipe Hands, in-browser, no GPU, 99%+ on static signs.
- **Surfaced the #1 risk:** the parent segment is saturated with FREE subsidized alternatives (state
  Deaf Mentor programs, Gallaudet/ASL Connect, IDEA Part C) → **willingness-to-pay is the crux.**

### Decisions locked
- Goal = validate **market viability + WTP**, not build a product.
- Parents-first, but **pivotable** (coaching engine is the permanent asset; vocab/pricing/channel swap).
- Demo vocab = 3–5 static first-signs (lead with ILY), used only as a credibility prop.
- Added a 5-segment **Market Landscape** table (parents = mission; general learners + healthcare = money).

### Infra & handoff
- Initialized git in the working dir; created GitHub repo `darsh94/talk-to-the-hand`; wired remote.
- Committed `PROJECT.md` (the full brief) and installed the Claude GitHub app.
- Ran **Ultraplan** cloud refinement → landed as PR #1 and **merged**. It locked the go/pivot/kill
  thresholds and resolved all open questions (ad budget ≤$50–100 unpaid-first; **B2B/grant A/B arm**;
  Netlify/Vercel static + decide-at-build capture).
- Set up the **"Talk to the Hand"** recall memory so future sessions resume from the Session Log.

### Built
- **`landing/index.html`** — deployable demand-test landing page: parent hook, ILY demo slot, how-it-works,
  mission strip (frames as *complement* to Deaf teachers), and the waitlist form with the **pricing probe
  incl. the B2B/grant arm** (captures email + WTP in one submit).
- **`landing/README.md`** — deploy steps (Netlify/Vercel) + how to read results vs. the locked thresholds.

### Open / next
- ⬜ Plug in Formspree endpoint + analytics before the page can collect data (user accounts).
- ⬜ Warm up FB parent groups + reach a **Hands & Voices** chapter contact before posting (no Reddit).

---

## 2026-07-13 — Live ILY demo

- Built **`landing/demo.html`** — a working, self-contained live demo: opens the webcam, tracks the
  hand with **MediaPipe Tasks Vision** (in-browser, nothing uploaded), and coaches the user to the ASL
  **"I love you"** sign in real time. Features: mirrored video + hand-skeleton overlay, a 5-point
  live checklist (thumb out / index up / pinky up / middle down / ring down), a progress meter, and
  specific encouraging hints ("So close — lift your pinky up 🤙"). Detection uses orientation-tolerant
  geometric heuristics (finger extended = tip farther from wrist than its PIP joint).
- Wired the landing page's demo tile → **"▶ Try it live"** linking to `demo.html`.
- Tested locally via `python3 -m http.server` on localhost (camera needs https/localhost). **Looks good
  — detection accepted as-is, no tuning needed.**
- **Deployed to Vercel** (Git-connected, root dir `landing`, auto-redeploys on push). **LIVE:
  https://talk-to-the-hand.vercel.app** — landing at `/`, live webcam demo at `/demo.html` (verified).
- **Added a dynamic motion sign — "MILK" 🍼** — the demo's marquee value proof (coaching *movement*,
  which a mirror/static-app can't do). Added a **sign-picker** (ILY static + MILK dynamic). MILK logic:
  a **continuous "openness"** measure (avg fingertip→wrist distance / palm size) drives an open↔fist
  state machine that **counts squeezes** (open-close-open-close = 2 reps → success), gated on **horizontal
  hand orientation** (palm down — the correct form; wrist→middle-knuckle vector must be mostly sideways).
  Success freezes on a celebration until "Start over"; won't trigger on an open hand or wrong orientation.
  Iterated live with the user to tune thresholds + orientation; dev debug readout hidden for shipping.
- **Next (to start collecting data):** (1) create a Formspree form → wire its endpoint into the
  landing form (replaces `REPLACE_WITH_FORM_ENDPOINT`); (2) add analytics for visit→signup rate;
  then (3) warm-up outreach to FB parent groups + a Hands & Voices chapter.

### End-of-session status (2026-07-13)
**Shipped & live:**
- ✅ Validation plan locked & merged (thresholds, B2B/grant arm) — `PROJECT.md`
- ✅ Landing page + waitlist + pricing probe (incl. B2B/grant arm) — `landing/index.html`
- ✅ Live in-browser demo, two signs — `landing/demo.html`:
  - 🤟 **ILY** — static handshape, 5-point live checklist + hints
  - 🍼 **MILK** — dynamic moving sign (openness squeeze-counter, horizontal-orientation gate, 2-rep
    completion + freeze). The product's core "coach, not a mirror" proof.
- ✅ Deployed on **Vercel** (Git-connected, auto-redeploy on push): https://talk-to-the-hand.vercel.app
- ✅ Repo: `github.com/darsh94/talk-to-the-hand`; recall memory + this daily log kept current.

**Not done yet (blocks the demand test from producing data):**
- ⬜ Wire Formspree endpoint into the waitlist form (still `REPLACE_WITH_FORM_ENDPOINT`)
- ⬜ Enable analytics (Vercel Analytics one-click, or Plausible) for visit→signup rate
- ✅ **Outreach + interview kit drafted & ready** — `OUTREACH_KIT.md` (FB posts A/B, Hands & Voices
  email, 15–20 min parent interview script with the WTP crux, capture template, recruiting checklist)
- ⬜ *Run* the outreach + 5–10 parent interviews (needs form wired + community warm-up first)
- ⬜ Read results vs. locked Go/Pivot/Kill thresholds → viability decision

**Key reminder:** the demo is strong, but the *goal is market-viability validation* — capturing signups +
WTP is what actually answers the question. Wiring the form is the true next priority.

---

## 2026-07-17 — Demo polish: third sign, celebrations, auto-detect

Session scoped to making `landing/demo.html` more appealing as a credibility prop (still a prop, not
the product — see §Key reminder above; the form-wiring priority is unchanged).

- **Added a third sign — "Yes" ✊** (fist nodding up/down, 2 reps to complete), pulled from the
  yes/no vocab already listed in `PROJECT.md`. Reuses the milk sign's open/closed-style state machine,
  but keyed on vertical wrist motion (via a slow-adapting baseline) instead of hand openness, gated on
  a stable "fist" handshape.
- **Celebration feedback:** confetti burst + a Web Audio chime + a glow-pulse on the video card when a
  sign is completed (and a short tick sound per counted rep) — replaces the old silent text-only "Perfect!".
- **Progress tracker:** "🏅 X of 3 signs mastered" badge row, persisted in `localStorage` so returning
  visitors see prior progress.
- **Auto-detect toggle:** guesses which sign is being attempted from hand shape/orientation and
  switches the picker automatically (debounced ~10 stable frames; won't interrupt a rep in progress).
- **Mobile camera flip button** (front/back facingMode).
- **Debounced verdict/state text** (small per-signal hysteresis) to stop the coaching hints from
  flickering frame-to-frame — a known rough edge from the 07-13 build.
- **"Still there?" re-prompt** after 10s with no hand detected, replacing the static "show your hand"
  placeholder.
- **Coach-vs-mirror tagline** ("They give you a mirror. We give you a coach.") now surfaces on the
  panel whenever a sign is being nailed, reinforcing the pitch line directly in the product.
- **Verification:** this sandbox's network policy blocks the MediaPipe CDN (`cdn.jsdelivr.net`), so a
  live camera pass wasn't possible here — confirmed via syntax check, a Playwright pass on the static
  UI (picker, progress badges), and a standalone unit test replicating the new detection math (ILY
  scoring, milk-vs-yes orientation disambiguation, debounce logic, rep-counting) against synthetic
  hand poses (16/16 passing). **A real camera pass on the deployed Vercel build is still owed** before
  trusting it for the pitch clip.
- Committed and pushed to branch `claude/repo-status-5zpjxb` (not yet merged to `main`).

### Data capture wired (same session, continued)

Picked up the 07-13 blocker directly: the demand test can't produce a go/pivot/kill read without
signups + WTP actually being captured. Both remaining plug-ins from `landing/README.md` are now wired.

- **Formspree endpoint live:** created a Formspree form (user did the signup — needs a real account,
  not something buildable from the sandbox) and wired `https://formspree.io/f/mzdnerjr` into
  `landing/index.html`'s waitlist form.
- **Form UX upgraded:** submits via `fetch` instead of a full-page POST, so a successful signup shows
  an inline "You're on the list! 🎉" message instead of redirecting away to Formspree. Added a
  `_gotcha` honeypot field (silently drops bot spam) and a `_subject` field for a clean notification
  email subject.
- **Vercel Web Analytics wired and enabled:** added the `/_vercel/insights/script.js` loader plus a
  custom `signup` event (tagged with the chosen `plan_interest` tier) fired on every successful
  submit. User enabled **Web Analytics** in the Vercel project dashboard — page views vs. the
  `signup` event now gives a direct **visits → signups** read, with the WTP tier breakdown attached,
  exactly what the Go/Pivot/Kill thresholds in `PROJECT.md` need.
- **Verification:** this sandbox's network policy also blocks `formspree.io` (confirmed via a direct
  curl — same class of restriction as the MediaPipe CDN block above), so the live submission couldn't
  be end-to-end tested from here. Instead verified locally with Playwright against a stubbed endpoint:
  placeholder-endpoint state shows a graceful error, the honeypot/subject fields are correctly hidden
  and set, `window.va` loads, and a successful submit correctly swaps in the confirmation message.
  **A real test submission against the live Formspree form is still owed** once deployed — submit one
  test entry on the live site, confirm it lands in Formspree, then delete that test row.
- Updated `landing/README.md` to match the wired state.
- Opened PR #3 and merged `claude/repo-status-5zpjxb` → `main`.

### Open / next
- ✅ **Live-camera smoke test** — done 2026-07-20 (see below).
- ⬜ **One real waitlist test submission** on the live site to confirm the Formspree wiring end-to-end
  (delete the test row afterward so it doesn't skew real signup counts).
- ⬜ Outreach + 5–10 parent interviews (community-access checklist from PROJECT.md still applies).
- ⬜ Read results vs. the locked Go/Pivot/Kill thresholds once signups start coming in.

---

## 2026-07-20 — Live-camera smoke test + competition launch prep

- ✅ **Live-camera smoke test PASSED** on the deployed build (https://talk-to-the-hand.vercel.app/demo.html).
  Verified the demo on a real webcam — clears the verification owed from the 07-17 cloud sessions
  (which could only logic-test, since that sandbox blocks the MediaPipe CDN). The build is now trusted
  for sharing / the pitch clip.
- **Preparing to launch the test** in the Half Baked competition Slack (build-in-public). Drafted a
  Slack post (interactive-demo-first hook + waitlist ask); ready to share.
- **Still owed before/while promoting:** one real Formspree test submission (then delete the test row);
  then run the parent outreach (`OUTREACH_KIT.md`) and read signups vs. the Go/Pivot/Kill thresholds.
- ✅ **Verified the funnel front-end** — a real test signup on the live site showed the inline "You're on
  the list! 🎉" confirmation (user; Formspree row check + delete still to do).
- **Channel playbook added** to `OUTREACH_KIT.md` — how to do Reddit + Facebook outreach without getting
  banned (warm-up, per-sub rules, community sensitivity, `?ref=` tracking, cadence).
- ✅ **`?ref=` attribution wired into the waitlist form** (`landing/index.html`): reads `?ref=` from the
  URL (persisted in sessionStorage across the hop to demo.html), falls back to referrer host then
  "direct", writes it to a hidden `ref` field so **Formspree captures which channel each signup came
  from**, and tags the Vercel `signup` event with `ref` too → signups-by-channel readout. Use per-post
  links like `…/?ref=reddit_asl`, `…/?ref=fb_parents`.
- 🐛 **Fixed camera-flip bug** (reported via early feedback): after flipping the camera ~twice, hand
  recognition silently stopped while the UI still showed "camera running," and "Start over" didn't
  recover it. Root cause: `detectForVideo()` throws on the brief **0×0 frame** during a camera swap,
  and the uncaught throw happened before `requestAnimationFrame(loop)` → the detection loop died
  permanently (reset only cleared UI state, never re-kicked the loop). Fix in `landing/demo.html`:
  (1) `loop()` wraps detection in try/catch, guards on `readyState`/`videoWidth`, and always schedules
  the next frame while running — the loop can no longer die; (2) `openCamera()` acquires the new stream
  before stopping the old, waits for `loadedmetadata` dimensions, and resets `lastVideoTime`.

### End-of-session status (2026-07-20)
**Done today:**
- ✅ Live-camera smoke test passed → demo trusted for sharing
- ✅ Drafted launch messages (Slack build-in-public, WhatsApp) for the competition + personal network
- ✅ Verified the waitlist funnel front-end on the live site (inline "You're on the list!" confirmation)
- ✅ Added Reddit + Facebook **channel playbook** to `OUTREACH_KIT.md`
- ✅ Wired **`?ref=` attribution** into the waitlist form (Formspree column + Vercel `signup` event),
  captured on both landing and demo pages → signups-by-channel
- ✅ Fixed the **camera-flip bug** that silently killed hand detection (from early user feedback)
- All committed and pushed directly to `main` (5 commits, `d201f06`..`2c845d7`); Vercel auto-deployed.

**Open / next:**
- ⬜ Delete the one real Formspree test row (front-end verified; just clean up the row)
- ⬜ Re-verify the camera-flip fix on the live build (flip 2–3×, confirm detection persists)
- ⬜ Draft per-subreddit Reddit posts (rule-compliant, `?ref=` links baked in)
- ⬜ Warm up FB parent groups + a Hands & Voices chapter; then run outreach
- ⬜ Read signups-by-channel vs. the locked Go/Pivot/Kill thresholds → viability decision
- 🧹 Housekeeping: stale merged remote branch `claude/repo-status-5zpjxb` can be deleted.
