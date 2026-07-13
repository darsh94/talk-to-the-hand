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
- ⬜ Plug in Formspree endpoint + analytics + ILY clip before the page can collect data (user accounts).
- ⬜ Warm up FB parent groups + reach a **Hands & Voices** chapter contact before posting (no Reddit).
- ⬜ Next build options: the ILY MediaPipe demo, or the outreach + parent-interview script.
