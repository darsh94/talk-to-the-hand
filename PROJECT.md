# Project "Talk to the Hand" — ASL Learning Coach

> **Recall trigger:** When the user says *"Talk to the Hand"* (aka "Tall-to-the-hand"), open this
> document and resume from the **Session Log** at the bottom. This is the single source of truth
> for the project.

---

## Context — Why this document exists

The user is role-playing a **serial healthcare-domain entrepreneur** entering the **Half Baked
10-day founder hackathon** (https://starthalfbaked.notion.site/). The chosen idea attacks the
**"Mirror Limit"** in ASL learning: learners practice alone with no feedback and never know if their
hand shape or speed is correct. This doc holds (1) the viability brainstorm, (2) the 1–3 day MVP
plan, and (3) a running session log so work resumes cleanly across sessions.

**PRIMARY GOAL (set 2026-07-12):** Test **market viability** — is there a real, *payable* market for
this idea? The 1–3 days go into a **cheap demand test + market sizing**, NOT a polished product. A
thin CV demo exists only as a credibility prop on the landing page. Build stack is secondary (lean).

**Intended outcome:** A go/no-go read on demand and willingness-to-pay, plus a healthcare/health-
equity narrative sharp enough to place in the hackathon.

---

## The Idea (one line)

**A webcam ASL coach that watches your hands and tells you *how* to fix them** — not just a mirror
to compare against, but automated, encouraging, letter-by-letter feedback on hand shape and speed.

Positioning line: **"They give you a mirror. We give you a coach."**

---

## Viability Analysis

### Market (grounded in research)
- ~**500K** US ASL primary users; **6.4–7M** US adults use sign language; **~2M deaf + ~10M** hard
  of hearing. Sign-language economy estimated **$3–10B/yr**.
- **Key reframe:** the paying *learner* is mostly **hearing people who must learn ASL**, not Deaf
  native signers.

### CHOSEN WEDGE (2026-07-12): Hearing parents of deaf children
- **Why:** 90%+ of deaf kids are born to hearing, non-signing parents → early-childhood
  *language-deprivation* is a real, urgent health-equity problem. Emotional, healthcare-native,
  differentiated. Pitch = **"Help me talk to my child,"** not "learn a language."
- **Buyer motivation:** love + fear of the language gap; time-poor, guilt-driven, highly motivated.
- **Vocabulary implication:** these parents need **first/parenting signs** (mom, dad, milk, more,
  eat, sleep, love, play, yes/no, hurt) far more than the A–Z alphabet. This creates tension with
  the "static fingerspelling is easiest to build" MVP assumption — see Open Question #4.
- **Deferred segments:** healthcare workers (B2B2C, compliance angle), ASL students, teachers.

### Problem validation
- The "Mirror Limit" is real *and* named by the market — but see competition below; incumbents
  address the *feeling* of it, not the *mechanics*.
- Research caveat to weave into the pitch: self-study apps underperform human tutors on confidence
  (~60% gap). Our angle: **close that gap with automated coaching, not just content.**

### Competitive landscape (the critical finding)
- **Lingvano** — "**Sign Mirror**": front-camera *visual self-comparison*. Likely does **not** do
  true hand-shape recognition/grading. ← our wedge.
- **ASL Bloom** — AI assistant + 1,300+ signs; feedback is conversational, not CV-based pose grading.
- **The ASL App, SignSchool, InterSign** — content/dictionary, minimal live feedback.
- **Takeaway:** Differentiation must be **real computer-vision feedback on hand pose** ("tuck your
  thumb," "spread your fingers," "you're 80% there") — the thing a mirror can't do. If we can't beat
  a mirror on *specific corrective feedback*, we don't have a wedge.

### Market sizing (grounded in research, 2026-07-12)
- **New families/yr:** US births ~3.6M × **2–3 per 1,000** deaf/HH = **~7,000–11,000 new families/yr**,
  **90%+ hearing/non-signing**.
- **Beachhead stock (SAM):** families with a deaf/HH child under 18 ≈ **several hundred thousand**
  (order-of-magnitude; acquired loss adds to the birth cohort). Focus = age **0–5** (urgent language
  window).
- **TAM:** all hearing people learning ASL to reach a deaf family member + the general-learner market
  Lingvano/ASL Bloom already monetize (~$10–13/mo) inside a **$3–10B** sign-language economy.
- **SOM (this test):** waitlist signups + interviews over 1–3 days (see Validation Plan).

### ⚠️ Top viability risk — WTP vs. FREE human alternatives
The parent beachhead is the **most subsidized, free-saturated** segment in the space. Parents get, at
no cost: state **Deaf Mentor programs** (human, often in-home, grant-funded), **Gallaudet Clerc
Center** toolkits, **ASL Connect**, **VL2** apps, **IDEA Part C** early intervention. → Emotional
pull is A+, but **willingness-to-pay is the #1 thing to validate.** Likely resolutions:
(a) position as a **complement** (daily practice between mentor visits), and/or (b) monetize adjacent
segments with **no free alternative + proven WTP** (ASL students, healthcare orgs, general learners),
using the parent story as mission/tech proof. **This is the crux the demand test must resolve.**

### Market Landscape (segment comparison)
Beachhead = parents (mission/tech proof). Money likely = general learners + healthcare/education.
The pricing probe A/B-tests WTP across these rather than betting only on parents.

| Segment | Est. size | WTP | Free-alt risk | Sales motion | Verdict |
|---|---|---|---|---|---|
| **General adult learners** (students, hobbyists, friends/coworkers of Deaf) | Largest; underpins $3–10B economy; Lingvano/ASL Bloom monetize at ~$10–13/mo | **High (proven)** | Low | B2C self-serve | 💰 Primary revenue engine; most crowded |
| **Healthcare workers/orgs** (nurses, ER, first responders, clinicians) | Large B2B; compliance/health-equity budgets | **High (budgeted)** | Low | B2B2C, longer cycle | 🎯 Best B2B; fits founder cred |
| **Educators / school staff** (teachers, aides for Deaf/HH students) | Institutional; district/grant funded | **Med–High** | Low–Med | B2B / institutional | 🎯 Grant-fundable adjacency |
| **Extended family** (grandparents, siblings) | Adjacent to parents; smaller | **Med** | **Low** (not covered by early-intervention) | B2C emotional | ➕ Same product, fewer free substitutes than parents |
| **Parents of deaf children** (chosen beachhead) | ~7–11K new families/yr; several hundred K stock | **Low–Med (⚠️)** | **High** (Deaf Mentor, Gallaudet, IDEA Part C — all free) | B2C emotional / grant | ⭐ A+ mission & tech proof; monetize via complement or B2B/grant, not paid consumer |

### Other honest risks
1. **Incumbent "mirror" features blur our story** — must demo *specific* corrections, not comparison.
2. **Dynamic signs are hard** in 1–3 days → scope to **static fingerspelling alphabet** first.
3. **Deaf-community trust / "hearing-savior" optics** — frame as a *tool for learners*, ideally
   validated with Deaf educators; avoid claiming to replace Deaf teachers.
4. **Accuracy across skin tones / lighting / left-handed signers** — MediaPipe is fairly robust;
   still, demo in good light and acknowledge the roadmap.

---

## Validation Plan (1–3 days) — goal is market viability, not a product

The output is a **go/no-go read on demand + willingness-to-pay**, not a finished app. Three workstreams
run in parallel.

### 1. Demand test — fake-door landing + waitlist (highest priority)
- **Landing page:** "**Talk to the Hand** — help your child learn their first signs, with a coach that
  watches your hands and shows you how." CTA = **Join the waitlist / Get early access**.
- **Pricing probe (the key experiment):** on/after signup, show a "Which plan interests you?" step with
  price points (e.g., Free / $9 mo / $19 mo / "I'd want it free through my early-intervention program").
  This directly tests WTP vs. the free-alternative risk.
  - **B2B/grant A/B arm (LOCKED 2026-07-13):** run a second framing as an A/B arm — "sold to your
    program, not to you" (e.g., "I'd want my early-intervention program / school to provide this").
    One run then reads both consumer WTP *and* the "sold to programs, not parents" model, de-risking the
    #1 WTP risk and telling us which way to pivot if consumer WTP is weak.
- **Traffic (unpaid first, LOCKED 2026-07-13):** parent communities — r/deaf, r/ASL, Facebook groups
  for parents of deaf kids, **Hands & Voices** chapters, Deaf-parenting forums. **Unpaid traffic runs
  first.** Paid boost is capped at **$50–100** total (Meta/Reddit ad set to a lookalike parent audience)
  and is spent only *after* the community-access checklist (see Open Questions) is confirmed, to get a
  clean conversion rate.
- **Instrument:** track visits → signups → price-tier selection. Build = a static one-page site on
  **Netlify/Vercel** + a lean form service for capture (see §Stack decision); no backend needed.

### 2. Qualitative — 5–10 parent interviews
- Recruit from the same communities. 15-min calls. Ask: *What do you use today? (mentor program? apps?)
  What's missing? Would automated practice feedback help? **Would you pay — and if a free Deaf mentor is
  available, why would you still want this?*** ← the WTP crux, asked to real humans.

### 3. Thin CV demo — credibility prop only (time-boxed, optional)
- One recorded 30–60s clip of the coach grading **1 sign** (recommend **ILY / "I love you"** — iconic,
  static, emotionally perfect) with encouraging feedback. Embed on the landing page to make the promise
  believable. **Do not** build the full app.
- If built: **MediaPipe Tasks Vision** (`@mediapipe/tasks-vision`) in-browser, 21 landmarks, **heuristic**
  handshape check (finger-extended + thumb flags) — no model training. Recommend **3–5 static
  first-signs** max (per user's choice), but 1 solid one is enough for the video.

### Success metrics / kill criteria (LOCKED 2026-07-13 — measured over the 1–3 day run window)
These are the committed bars, not illustrative. Read the outcome after the run window closes.
- **Go signal:** ≥ **30%** landing→signup among targeted parent traffic, **≥ 100 signups** in the
  1–3 day window, AND ≥ **30%** of signups selecting a **paid** tier — OR ≥ half of interviewed
  parents expressing genuine WTP despite free options.
- **Pivot signal:** strong signups but tier selection skews *free / through their program* → validate an
  adjacent paying segment (students / healthcare / B2B-grant) instead. The pricing probe's B2B/grant
  arm (see below) is the built-in read on which way to pivot.
- **Kill signal:** low signup (**< ~15%** landing→signup) AND parents uniformly satisfied with free
  mentors → idea (as a paid consumer product for this segment) is not viable; reconsider.

### Stack decision — deferred/lean (updated 2026-07-13)
Secondary to the goal. Default: **static landing page deployed to Netlify/Vercel** (build as portable
static files) + **optional** thin MediaPipe clip. **Data capture** = lightest form service that fits,
chosen at build time (Tally/Formspree-class); keep it a deferred build decision, not a locked tool, and
note in the build where the form / analytics key gets dropped in. Revisit a real backend/app only
*after* demand is proven.

---

## Pitch narrative (draft spine)
- **Hook:** "Half a million Americans sign as their first language — and the people who love them are
  stuck learning alone in front of a mirror."
- **Problem:** the Mirror Limit — practice with no feedback → no confidence.
- **Insight:** every app gives you a *mirror*; none give you a *coach*.
- **Demo:** watch it catch my thumb and coach me to a perfect "B."
- **Why now:** in-browser CV (MediaPipe) makes real-time hand coaching free and instant.
- **Why me:** healthcare founder — this is health equity (early language access), not a toy.

---

## Immediate setup step (do first, on approval)
- Create project directory **`/Users/darshparikh/Documents/personal-github/talk-to-the-hand`** and
  run `git init` inside it (unblocks the Ultraplan cloud handoff, which requires a git repo).
- Copy this plan into the repo as `PROJECT.md` so the doc, cloud agent, and any build share one home.

## Decisions locked (2026-07-12)
1. **Wedge:** hearing **parents of deaf children** (mission/beachhead).
2. **Goal:** validate **market viability + WTP** — demand test, not a product build.
3. **Demo vocab:** 3–5 **static first-signs** (lead with ILY), used as a credibility prop only.
4. **Stack:** lean/no-code; real build deferred until demand is proven.

### Decisions locked (2026-07-13)
5. **Go/pivot/kill thresholds:** committed (see §Success metrics) — Go ≥30% signup + ≥100 signups +
   ≥30% paid-tier; Kill <~15% signup + free-mentor satisfaction.
6. **Ad budget:** unpaid parent-community traffic first; paid boost capped at **$50–100**, spent only
   after the community-access checklist is confirmed.
7. **Pricing probe:** includes a **B2B/grant A/B arm** alongside consumer price points.
8. **Hosting:** **Netlify/Vercel** static deploy (build as portable static files).
9. **Data capture:** lightest form service that fits, **chosen at build time** (deferred, not locked);
   note where the form / analytics key drops in.

## Pivot thesis (2026-07-12) — parents-first, by design
**Parents = deliberate starting wedge, not a bet-the-company choice. The idea is highly pivotable.**
- **Permanent asset (moat):** the CV hand-pose **coaching engine** (MediaPipe landmarks + handshape
  grading + encouraging feedback). Segment-agnostic.
- **Swappable per pivot (cheap):** vocabulary pack (parents "milk/more/love" → healthcare
  "pain/where/medicine" → students A–Z), landing copy + pricing, and go-to-market channel.
- **Pivot type:** concentric-circles (same core, adjacent audience) — a content + positioning swap,
  **not a rebuild**. Ready segments teed up in the Market Landscape table.
- **Why parents first:** highest-empathy validation of whether coaching truly helps + mission/press/
  grant access + learn the engine's real limits on varied live users. The pricing probe is the
  built-in **pivot trigger** (e.g., parents love it but want it free → expand to healthcare/learners).
- **Build constraint to preserve optionality:** keep tech + brand **segment-neutral under the hood**
  (no hard-coded "baby signs" in the architecture) so pivoting stays a swap.

## Open Questions — RESOLVED (2026-07-13)
1. **Kill/go thresholds + ad budget** → RESOLVED. Thresholds locked in §Success metrics; ad budget
   capped at **$50–100** with unpaid community traffic first (Decisions #5, #6).
2. **Which parent communities can the user access without spam-flagging?** → Converted to a
   **pre-run user-action checklist** (blocks paid spend): before the run, the user confirms which of
   r/deaf, r/ASL, Deaf-parenting Facebook groups, and **Hands & Voices** chapters they can post in
   without being flagged. ⬜ *User action — confirm before any paid boost.*
3. **A/B a B2B/grant framing?** → RESOLVED: **yes.** Added as an A/B arm of the pricing probe
   (Decision #7, §Demand test).

---

## Session Log (resume point)
- **2026-07-12** — Kickoff + full research pass. Findings: (a) incumbents address the *feeling* of the
  Mirror Limit, not true CV pose grading → wedge = real corrective coaching; (b) MVP tech is trivially
  buildable via in-browser MediaPipe; (c) **market sized** — ~7–11K new deaf/HH families/yr, several
  hundred K stock, $3–10B broader economy; (d) **critical risk surfaced** — parent beachhead is
  saturated with FREE human/subsidized alternatives → WTP is the crux. Locked 4 decisions and rewrote
  plan into a **1–3 day validation experiment** (fake-door landing + pricing probe + parent interviews
  + thin demo clip) with go/pivot/kill criteria. **Next:** on approval — (1) set up "Talk to the Hand"
  recall memory, (2) stand up landing + pricing probe, (3) recruit interviews, (4) record ILY clip.
- **2026-07-13** — Cloud handoff session. Decision: **refine the plan, do not build yet.** Sharpened the
  doc into an execution-ready brief: (a) **locked** the go/pivot/kill thresholds (removed the "example"
  hedging; Go ≥30% signup + ≥100 signups + ≥30% paid-tier, Kill <~15% signup); (b) resolved all three
  Open Questions — ad budget capped at **$50–100** (unpaid traffic first), community-access converted to
  a pre-run user-action checklist, and a **B2B/grant A/B arm** added to the pricing probe; (c) recorded
  build preferences — **Netlify/Vercel** static hosting + **decide-at-build** data capture (lean form
  service). **Next:** a build session stands up the landing + pricing probe (incl. the B2B/grant arm),
  but only *after* the user confirms which communities they can post in (Open Q #2 checklist).

## Sources
- Half Baked hackathon: https://www.gethalfbaked.com/hackathon-terms-and-conditions
- ASL apps landscape: https://preply.com/en/blog/apps-to-learn-sign-language/ ; https://www.aslbloom.com/blog/best-asl-app
- MediaPipe ASL feasibility: https://arxiv.org/pdf/2305.05296 ; https://www.mdpi.com/1424-8220/25/7/2138
- Market size: https://www.aslbloom.com/blog/how-many-people-use-asl ; https://gallaudet.edu/president/how-sign-language-is-driving-a-multi-billion-dollar-inclusive-economy/
- Deaf/HH children prevalence: https://headstart.gov/publication/hearing-screening-fact-sheet ; https://pmc.ncbi.nlm.nih.gov/articles/PMC10686551/
- Free parent alternatives (WTP risk): https://clerccenter.gallaudet.edu/earlyintervention/ ; https://wesp-dhh.wi.gov/outreach/servicesresources/dmp/ (state Deaf Mentor programs)
