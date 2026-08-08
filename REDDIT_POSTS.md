# Reddit posts — one per channel (all 17 maker subs + ICP)

Rules recap (from `OUTREACH_KIT.md` §6): warm up first · 1–2 subs/day · never paste identical
text across subs (these are all distinct on purpose — keep them that way when you tweak) ·
reply to every comment · log removed posts in `DAILY_LOG.md`.

Fit tiers: 🟢 post as-is · 🟡 check sub rules first / adapt · 🔴 high removal risk, skip unless
you've read the sub and found an angle that fits.

---

## 🟢 r/SideProject — `?ref=reddit_sideproject`

**Title:** I built a webcam ASL coach that grades your hand shape in real time — now testing whether
the idea is even viable as a profitable product (its competitor is free)

> My thesis: ASL apps hit a "Mirror Limit" — they show you a video of the sign, you copy it into your
> webcam or a mirror, and... nothing tells you if you're actually doing it right.
>
> So I built a coach instead of a mirror. It runs entirely in the browser (MediaPipe hand tracking, no
> GPU, nothing uploaded), watches your hand, and gives live feedback — "so close, lift your pinky 🤙".
> It even grades *moving* signs: for "milk" it counts your open-close squeezes 🍼.
>
> Try it (free, ~30 seconds, needs a webcam): https://talk-to-the-hand.vercel.app/?ref=reddit_sideproject
>
> The part I'd love feedback on: I'm deliberately **not** building more product yet. The target buyer
> (hearing parents of deaf kids) has free state-subsidized alternatives, so before writing more code I'm
> running a validation test — landing page → demo → book-a-call funnel, with pre-committed go/pivot/kill
> thresholds. If parents won't commit 15 minutes, they won't commit $15/mo.
>
> Happy to share the validation setup, the hand-tracking approach, or anything else. Roast welcome.

---

## 🟢 r/ClaudeAI — `?ref=reddit_claudeai`

**Title:** Built a real-time ASL coach with Claude Code — in-browser hand tracking, motion-sign
detection, and it debugged a camera bug I couldn't see

> Sharing a project built almost entirely with Claude Code: a webcam ASL coach that gives live feedback
> on your signing (not just showing you a video to copy). All in-browser — MediaPipe hand landmarks +
> geometric heuristics Claude wrote (finger extended = fingertip farther from wrist than its middle
> joint), no GPU, nothing uploaded.
>
> The parts Claude did that impressed me:
> - **Motion signs, not just static poses.** For "milk" (open-close squeeze) it designed a continuous
>   "hand openness" measure driving a state machine that counts reps, gated on palm orientation so a
>   waving open hand doesn't false-trigger.
> - **A bug I'd never have found:** flipping the phone camera twice silently killed detection while the
>   UI looked fine. Claude traced it to `detectForVideo()` throwing on the brief 0×0 frame during the
>   camera swap — the throw happened before the next `requestAnimationFrame`, so the loop died
>   permanently. Fix: guard the frame, always reschedule.
> - Wrote synthetic-hand-pose unit tests for the detection math when the sandbox couldn't access a camera.
>
> Live demo (free): https://talk-to-the-hand.vercel.app/?ref=reddit_claudeai — try "milk", it's the
> fun one. Happy to answer anything about the workflow.

---

## 🟢 r/vibecoding — `?ref=reddit_vibecoding`

**Title:** Vibe-coded a webcam sign-language coach — the first sign took a weekend, making it stop
false-triggering took weeks

*(v3 — first draft tripped the rule-check for Rule 3 "no shilling" + Rule 2 "dev tools approval."
Rule 3's fine print WELCOMES project posts that include: tools used, process/workflow, build
insights — so this version names the stack explicitly and leads with the build story. Rule 2's
X-community approval path is only needed for promoting it as a startup/tool — separately worth
doing for the one sanctioned intro post; see note below.)*

> Wanted to see how far pure vibe coding gets with computer vision. Answer: surprisingly far, with
> one catch.
>
> **Tools:** Claude Code (wrote ~all of it), MediaPipe Tasks Vision for hand landmarks, single
> self-contained HTML file, deployed on Vercel's free tier. No ML training, no GPU, no backend.
>
> **Workflow:** describe the sign in plain English → Claude turns it into geometric rules over the
> 21 hand landmarks. "Is this finger extended" = is the fingertip farther from the wrist than its
> middle joint. Moving signs (like ASL "milk", an open-close squeeze) use a hand-openness value
> driving a little state machine that counts reps, gated on palm orientation.
>
> What fought back: **thresholds**. Getting a sign to *detect* took an evening. Getting it to *not*
> detect when someone waves, or holds their hand at a weird angle, took weeks of tuning. Best bug:
> flipping the phone camera twice silently killed detection — the video element briefly reports 0×0
> during the swap, the detector throws, and the loop died before scheduling its next frame. UI looked
> totally fine the whole time.
>
> It's free in the browser if you want to poke at it (nothing gets uploaded):
> https://talk-to-the-hand.vercel.app/?ref=reddit_vibecoding
>
> Anyone else done CV by vibes? How do you tune detection thresholds when you can't write a proper
> eval?

**Rule 2 side-quest (optional but recommended):** join the Vibe Coding community on X
(x.com/i/communities/1898129646782497027), post the tool there for mod review. If approved you get
one sanctioned "shill" intro post in the sub + can post major feature updates after — a second,
legitimate bite at this audience.

---

## 🟢 r/IMadeThis — `?ref=reddit_imadethis`

**Title:** I made a webcam coach that teaches you real sign language — it watches your hand and
counts your reps 🍼

> Point your webcam at your hand and it coaches you through actual ASL signs in real time — checks
> each finger for "I love you" 🤟, and for "milk" it literally counts your open-close squeezes like a
> gym rep counter. Everything runs in your browser; no video leaves your machine.
>
> Free, no signup to try: https://talk-to-the-hand.vercel.app/?ref=reddit_imadethis
>
> Built for hearing parents of deaf kids who are learning to sign back. Would love to know if the
> feedback feels helpful or annoying.

---

## 🟢 r/apps — `?ref=reddit_apps`

**Title:** Free web app that teaches you sign language by watching your hands through the webcam

> Most sign-language apps show you a video and hope you copy it right. This one actually *watches
> you* — real-time hand tracking in the browser tells you which finger to fix ("so close — lift your
> pinky") and counts your reps on moving signs.
>
> No download, no account, no video uploaded (all processing is local in the browser):
> https://talk-to-the-hand.vercel.app/?ref=reddit_apps
>
> Only knows three signs so far — it's an early test. Curious what this community thinks of
> camera-based coaching as an app category.

---

## 🟢 r/startups — `?ref=reddit_startups`

**Title:** Roast my validation design: $75, 14 days, and pre-committed go/pivot/kill thresholds —
before I write any more code

> Product: an AI webcam coach that grades ASL hand shapes in real time (working demo, 3 signs).
> Buyer: hearing parents of deaf kids — 90%+ of deaf children are born to parents who don't sign.
>
> The brutal part: state-subsidized programs give these parents human mentors for **free**. So instead
> of building, I'm running a demand test: ads + community posts → live demo → "book a 15-min founding
> call." Pass bar, committed in writing before launch: 600 reached → 90 demo → 45 complete a sign →
> 10 booked → 5 calls held, **and ≥3 of those parents already spend real money on learning to sign.**
> Miss it → pivot to adult learners or B2B healthcare training; the CV engine carries over.
>
> Demo if you want context: https://talk-to-the-hand.vercel.app/?ref=reddit_startups
>
> What holes do you see in the test design? Where would you expect it to give a false positive?

---

## 🟢 r/Entrepreneur — `?ref=reddit_entrepreneur`

**Title:** My target customer gets the alternative for free (government-subsidized). How I'm testing
whether they'll still pay — without building the product first

> I built a demo of an AI coach that teaches parents sign language through their webcam (real-time
> hand grading, works in any browser). Clear pain — most parents of deaf kids never learn to sign
> fluently — but the elephant: free state programs already offer human Deaf mentors.
>
> So the question isn't "is this useful," it's "will anyone pay when free exists." My test: drive
> parents to the live demo, then ask for a 15-minute call (their time = the currency). On calls I only
> ask about **past behavior** — what they've already spent money and hours on — never "would you pay?"
> Pre-committed thresholds decide go/pivot/kill in 14 days, on a $75 ad budget.
>
> The demo, for context: https://talk-to-the-hand.vercel.app/?ref=reddit_entrepreneur
>
> For those who've competed against free: what actually made customers pay you anyway?

---

## 🟢 r/founder — `?ref=reddit_founder`

**Title:** 10-day hackathon build → then I forced myself to stop coding. The validate-first playbook
I wish I'd used on my last idea

> Built during a hackathon: a webcam ASL coach — grades your hand shape live, counts reps on moving
> signs, all in-browser. The old me would now spend 6 months adding vocab, accounts, and a mobile app.
>
> Instead the rule this time is: **no more product until the market speaks.** Funnel is live (demo →
> book a founding call), every step instrumented with per-channel attribution, and the go/pivot/kill
> thresholds were written down *before* launch so I can't rationalize weak numbers later. Total spend
> so far: $75 of planned ads and a Vercel free tier.
>
> Demo: https://talk-to-the-hand.vercel.app/?ref=reddit_founder
>
> Founders who've done this: what's the failure mode of validate-first? Where did a "validated" signal
> still lead you off a cliff?

---

## 🟢 r/micro_saas — `?ref=reddit_micro_saas`

**Title:** Pre-revenue micro-SaaS where the incumbent alternative is free — here's the test I'm
running before writing more code

> Niche: hearing parents of deaf children learning ASL (~500K primary ASL users in the US, 6–7M
> signers total). Product: browser-based AI coach that grades hand shape/movement in real time —
> working demo, three signs, zero backend cost.
>
> The catch that makes this a validation problem and not a build problem: state early-intervention
> programs give these parents free human mentors. My wedge is "they give you a mirror, we give you a
> coach" — existing apps (Lingvano etc.) show you videos; none grade your actual hands.
>
> Current test: demo → book-a-founding-call funnel, $75 ads, per-channel `?ref=` attribution,
> pre-committed pass/fail numbers. Demo: https://talk-to-the-hand.vercel.app/?ref=reddit_micro_saas
>
> Anyone here validated a niche where free substitutes exist? What signal finally convinced you?

---

## 🟢 r/microsaas — `?ref=reddit_microsaas`

**Title:** Niche check: AI sign-language coach. Tiny TAM, huge mission, unknown willingness-to-pay —
would you build here?

> The market on paper: sign language is a $3–10B economy, but the beachhead I care about (hearing
> parents of deaf kids) is narrow and partially served by free subsidized programs. The tech is
> genuinely cheap to run — hand tracking happens in the user's browser, so my marginal cost per user
> is ~zero. Classic micro-SaaS economics *if* anyone pays.
>
> Rather than argue about it, I shipped a demo (3 signs, real-time grading) and a funnel that asks
> parents for a 15-min call instead of an email — time-commitment as the demand proxy.
>
> https://talk-to-the-hand.vercel.app/?ref=reddit_microsaas
>
> The micro-SaaS question: is "tiny niche + zero marginal cost + emotional urgency" enough to
> overcome "free alternative exists"? Would love takes from people who've priced against free.

---

## 🟢 r/marketing — `?ref=reddit_marketing`

**Title:** Live case study: marketing a paid product against a free, government-subsidized
alternative. My funnel + measurement design — critique welcome

> Product: an AI webcam coach for learning sign language (real-time hand grading — working demo).
> Audience: hearing parents of deaf kids. Competitor: **free** state mentor programs.
>
> Choices I'd love critiqued:
> - **Positioning:** "They give you a mirror. We give you a coach." — against video-library apps, not
>   against the free human programs (we frame as a *complement* to those).
> - **CTA:** killed the waitlist as primary; the ask is "book a 15-min founding call." Email = interest;
>   calendar time = demand.
> - **Measurement:** every channel gets a distinct `?ref=` (captured through the whole funnel into the
>   form + analytics events), so I get visits → demo-completions → bookings *per channel*, not blended.
> - **Interviews:** Mom Test rules — past spend only, no hypotheticals, end on a commitment ask.
>
> Funnel entry, if useful: https://talk-to-the-hand.vercel.app/?ref=reddit_marketing
>
> What would you change before I spend the (tiny, $75) paid budget?

---

## 🟢 r/juststart — `?ref=reddit_juststart`

**Title:** Progress report: 4 weeks in — demo shipped, funnel instrumented, $0 revenue by design.
Demand test starts this week

> Following the validate-before-build path and posting the receipts:
>
> - **Wk 1:** picked the niche (parents learning sign language for their deaf kids), wrote go/pivot/kill
>   thresholds down *first*, shipped a landing page + working webcam demo (browser-based hand grading).
> - **Wk 2:** added two more signs incl. motion detection; wired forms, analytics, per-channel `?ref=`
>   attribution end-to-end.
> - **Wk 3:** user feedback round → rewrote the landing page problem-first, fixed confusing instructions,
>   audited my interview script against The Mom Test (cut every hypothetical question).
> - **Wk 4 (now):** launch. $75 ads + community outreach → live demo → book-a-call. 14 days, then I read
>   the numbers against the thresholds and go, pivot, or kill.
>
> The live funnel: https://talk-to-the-hand.vercel.app/?ref=reddit_juststart
>
> Will post the results either way. Anything you'd add to the measurement before launch?

---

## 🟢 r/SaaSMarketing — `?ref=reddit_saasmarketing`

**Title:** I demoted my waitlist to a fallback and made "book a 15-min call" the primary CTA — the
reasoning + funnel design

> Context: pre-revenue validation of an AI sign-language coach (working browser demo). I realized my
> waitlist was about to hand me a vanity metric — emails measure interest, and my whole risk is
> willingness-to-pay against a free alternative.
>
> The redesign: primary CTA = book a founding call (Cal.com), waitlist demoted to "can't do a call?"
> with a pricing-probe question attached. Every traffic source carries a `?ref=` that persists across
> the landing→demo hop and lands in both the form data and the analytics events — so the read is
> bookings-per-channel, not blended traffic. Demo-start and demo-complete events close the mid-funnel
> blind spot.
>
> Funnel: https://talk-to-the-hand.vercel.app/?ref=reddit_saasmarketing
>
> Curious how others here have separated interest signals from demand signals pre-revenue.

---

## 🟡 r/appledevelopers — `?ref=reddit_appledevelopers`
*(Web, not native — lead with the iOS-Safari engineering story, not the product. Check rules.)*

**Title:** War story: getUserMedia + MediaPipe on iPhone Safari — the camera-flip bug that silently
killed my detection loop

> Shipped a webcam hand-tracking web app and iPhone Safari taught me some lessons:
>
> The nasty one: tapping my front/back camera flip button twice killed hand detection *silently* —
> video kept playing, UI said "camera running," detection just stopped. Root cause: during the stream
> swap the video element briefly reports 0×0, `detectForVideo()` throws on it, and the throw happened
> before the next `requestAnimationFrame` — so the loop died permanently with no error surfaced.
> Fix: guard on `readyState`/`videoWidth`, wrap detection in try/catch, and schedule the next frame
> unconditionally while running. Also: acquire the new stream *before* stopping the old one.
>
> The app (an ASL sign coach, runs fully client-side):
> https://talk-to-the-hand.vercel.app/?ref=reddit_appledevelopers
>
> Anyone else hit the 0×0-frame window on facingMode swaps? Curious if native AVFoundation has an
> equivalent gotcha.

---

## 🟡 r/iOSAppsMarketing — `?ref=reddit_iosappsmarketing`
*(It's a web app — frame as "validate on web before building native." Check rules.)*

**Title:** Validating demand with a mobile web demo before committing to a native app — funnel +
attribution setup

> Before building an iOS app for my sign-language coach, I shipped the whole experience as a mobile
> web demo (camera-based hand tracking works in Safari) and pointed all marketing at it. The logic:
> if parents won't try a zero-install web demo and book a call, an App Store listing won't save it.
>
> Setup that's been useful: per-channel `?ref=` tags that survive the landing→demo navigation and land
> in the signup form + analytics events; demo-start/demo-complete events so I can see where mobile
> users drop; book-a-call as the conversion (not installs or emails).
>
> The funnel: https://talk-to-the-hand.vercel.app/?ref=reddit_iosappsmarketing
>
> Has anyone here validated web-first and then launched native? Did the web numbers predict App Store
> performance?

---

## 🔴 r/macapps — `?ref=reddit_macapps`
*(Sub is for macOS apps; a web app will likely be removed. Recommend SKIP. If you must, comment on
relevant threads instead of posting, or use this only if the rules allow web apps:)*

**Title:** [Web] Free sign-language coach that uses your Mac's camera — all local, no install

> Not a native app (mods, remove if out of bounds) — but it's a tool I use on my Mac daily: open a
> browser tab, it tracks your hand through the webcam and coaches you through ASL signs with live
> feedback. All processing is local in the browser; nothing is uploaded.
> https://talk-to-the-hand.vercel.app/?ref=reddit_macapps

---

## 🔴 r/passive_income — `?ref=reddit_passive_income`
*(Poor fit — this project is the opposite of passive right now. Recommend SKIP. The only honest
angle is anti-hype:)*

**Title:** Before chasing "passive income" apps, I now run a $75 kill-test. Current one in progress —
here's the setup

> Lesson from past projects: the expensive part isn't building the app, it's spending months building
> for a market that won't pay. So before this app (an AI sign-language coach — demo already works, and
> its costs actually *are* near-zero since compute runs in the user's browser) gets another line of
> code, it has to survive a $75, 14-day demand test with pass/fail numbers written down in advance.
>
> If it passes, the economics look like the passive dream: static site, no servers, subscription
> pricing. If it fails, I killed it for $75 instead of six months.
>
> The test funnel: https://talk-to-the-hand.vercel.app/?ref=reddit_passive_income
>
> How do you pressure-test an income idea before building?

---

## 🟢 r/asl — `?ref=reddit_asl` *(ICP — Track A. Feedback ask, NOT a launch. Read sub rules first.)*

**Title:** I made a free practice tool that gives live feedback on your handshape — is this actually
useful, or a miss?

> When I practice a sign, I can copy a video into a mirror, but nothing tells me if my handshape is
> actually right. So I built a free browser tool that watches through the webcam and coaches in real
> time — e.g. for ILY it checks each finger and says things like "so close — lift your pinky."
> Everything runs locally in the browser; no video is uploaded anywhere.
>
> It only knows a few first signs so far (ILY, MILK, YES), and I want to know if this direction is
> even useful before going further — especially from people who actually sign. It's meant as practice
> *between* real instruction from Deaf teachers, never a replacement for it.
>
> https://talk-to-the-hand.vercel.app/?ref=reddit_asl
>
> Honest reactions welcome, including "this isn't it."

---

## Suggested posting order (1–2/day, weekday mornings ET)

| Day | Post |
|---|---|
| 1 | r/SideProject + r/IMadeThis |
| 2 | r/ClaudeAI |
| 3 | r/vibecoding + r/apps |
| 4 | r/startups |
| 5 | r/Entrepreneur + r/founder |
| 6 | r/micro_saas + r/microsaas |
| 7 | r/marketing + r/juststart |
| 8 | r/SaaSMarketing + r/appledevelopers (if rules allow) |
| 9 | r/iOSAppsMarketing |
| — | r/asl: separately, only after genuine warm-up in that community (Track A — handle with care) |
| — | r/macapps, r/passive_income: skip unless you've found a thread where they genuinely fit |
