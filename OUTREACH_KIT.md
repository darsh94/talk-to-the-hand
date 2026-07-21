# Talk to the Hand — Outreach & Interview Kit

Ready-to-use scripts for recruiting parents to the demand test. Goal = measure **demand + WTP**
(especially: would parents want/pay for this *given free Deaf-mentor programs exist?*).

Live link to share: **https://talk-to-the-hand.vercel.app**

---

## Ground rules (read first)

1. **Warm up before posting.** Join 2–3 groups, comment genuinely for a few days. Cold link-drops get
   you banned and taint the data. Check each group's self-promo rules; ask a mod if unsure.
2. **Be transparent.** You're building a tool and want honest feedback — don't pose as a parent if
   you're not one. Authenticity gets better data and respect.
3. **Respect the Deaf community.** Frame as a **practice aid *between* mentor visits — not a replacement
   for Deaf teachers/mentors.** Avoid "hearing-savior" language. If Deaf members push back, listen.
4. **It's free.** The test is a waitlist + free demo. Don't over-promise features that don't exist yet.
5. **No Reddit for now** (per plan). Channels: Facebook parent groups + Hands & Voices chapters.

---

## 1. Facebook parent-group posts

### Post A — value-first feedback request (primary)
> Hi all 👋 I'm building a **free** tool to help hearing parents practice ASL with their deaf/HH kids.
> It uses your webcam to give gentle, real-time feedback on your signing — so you're not just guessing
> in front of a mirror. Right now it coaches a couple of first signs (including "I love you" and "milk").
>
> It's early and completely free — I'd love honest feedback from parents actually living this: is this
> helpful, or not really? 👉 https://talk-to-the-hand.vercel.app
>
> (Mods — happy to take this down if it's not welcome. Not selling anything; just trying to build
> something genuinely useful.)

### Post B — short soft ask (for chattier groups)
> Quick question for parents learning to sign: when you practice at home, do you ever wish something
> could tell you if your handshape is actually *right*? I built a free little webcam coach that does
> exactly that (try "milk" — it counts your squeezes 🍼): https://talk-to-the-hand.vercel.app —
> would love to know if it's useful or a miss.

### Comment / DM snippet (1:1 follow-up)
> Thank you so much! If you have 15 min sometime, I'd love to hear how you practice today and what
> would actually help — totally optional, no pitch. Either way, I really appreciate you trying it. 🙏

---

## 2. Hands & Voices chapter outreach (email/DM to a chapter contact)

**Subject:** A free ASL practice tool for your families — would love your feedback

> Hi [Name],
>
> I lead [/ am building] a small project called **Talk to the Hand** — a free, browser-based tool that
> gives hearing parents real-time feedback on their signing as they practice at home (a coach, not just
> a mirror). It's meant to *complement* the mentor and early-intervention support families already get,
> not replace it.
>
> Before going further, I'd really value the perspective of a chapter that works with these families
> every day: is a practice-feedback tool like this something your parents would find useful? Would you
> be open to a quick look, or pointing me to a parent or two who might give candid feedback?
>
> Live demo (free, nothing is uploaded — all in-browser): https://talk-to-the-hand.vercel.app
>
> Thank you for the work you do — and for any thoughts you can share.
> [Your name]

---

## 3. Parent interview script (~15–20 min)

**Recruit** from the same channels ("15 min, no pitch, I'll listen"). Aim for **5–10 interviews.**

### Intro / consent (30 sec)
> Thanks for the time. I'm learning how parents practice ASL — there are no right answers, and I'm not
> selling anything today. Mind if I take notes? Feel free to be totally blunt.

### Their world (context)
1. Tell me about your journey learning to sign with your child — where are you now?
2. What are you using today? (early intervention? a Deaf mentor program? apps? YouTube? classes?)
3. What's the hardest part of practicing at home?

### The problem (validate the "Mirror Limit")
4. When you practice alone, how do you know if you're signing it *correctly*?
5. Has "not knowing if I'm doing it right" ever slowed you down or discouraged you?

### The WTP crux ⭐ (the most important part)
6. If a tool watched your hands and gave you gentle feedback + practice, would that help? How?
7. **You likely have access to a free Deaf mentor / early-intervention support. Given that, would you
   still want something like this? What would it need to do to be worth it *alongside* those?**
8. If it genuinely helped, what feels fair — free, a few dollars a month, or something you'd expect your
   program/school to provide? (Listen for: consumer WTP vs. "should be free/through my program.")

### Demo reaction (if live)
9. *(Share the link, let them try it.)* What's your gut reaction? What's missing or confusing?
10. Whose "first words" would you most want to practice? (probes the real vocabulary need)

### Close
> This was hugely helpful. Anything I should have asked but didn't? — And may I follow up when there's
> more to show?

---

## 4. What to capture (for the Go/Pivot/Kill read)

Per interview, log: current tools used · biggest pain · **would they want it despite free options (Y/N +
why)** · **WTP signal** (free-only / would-pay / "through my program") · vocabulary they most want ·
demo reaction. Roll these up against `PROJECT.md` §Success metrics after the run window.

---

## 5. Recruiting-to-data checklist
- [ ] Warmed up in 2–3 FB parent groups (posting rules checked)
- [ ] Identified 1–2 Hands & Voices chapter contacts
- [ ] **Formspree endpoint wired** into the landing form (so signups are captured)
- [ ] **Analytics enabled** (visit→signup rate)
- [ ] Posts A/B live; interviews scheduled (target 5–10)
- [ ] Optional paid boost ($50–100) — only *after* the above

---

## 6. Channel playbook — Reddit & Facebook (how to actually do it)

### ⚠️ The #1 rule for BOTH: warm up, don't drive-by
Communities auto-filter/ban brand-new accounts and pure link-drops. Plan a **2–3 day warm-up** per
channel: join, read the pinned rules, and leave a few genuine comments *before* you ever post a link.
Reddiquette's rough guide is **~90% participation / 10% self-promo.**

### Track which channel converts — use a `?ref=` tag per post
Append a unique tag to the link so Vercel Analytics' referrer/UTM view tells you what's working:
- Reddit r/asl → `https://talk-to-the-hand.vercel.app/?ref=reddit_asl`
- FB parent group → `https://talk-to-the-hand.vercel.app/?ref=fb_parents`
- WhatsApp/Slack → `?ref=wa` / `?ref=slack`
(Optional upgrade: capture `ref` as a hidden field in the waitlist form for exact per-post attribution —
ask and I'll wire it.)

### Reddit
**Where:** r/asl and r/ASL (learners — most receptive), r/deaf (protective — read rules, consider
messaging mods first), r/HardOfHearing, r/slp (speech-language pathologists), r/ECEProfessionals /
r/Teachers (educators). Adjacent: r/parenting, baby-sign threads.

**How:**
- Use an **aged account with some karma** — fresh accounts get auto-removed.
- **Read each subreddit's rules.** Many ban self-promo outright → either post as a genuine
  *"I built a free tool, would love feedback"* discussion (not a "launch"), or **DM the mods** for the OK.
- **One subreddit at a time**, and **don't paste identical text** across subs (spam filter). Rewrite each.
- Add flair if required; post weekday mornings ET for reach.
- **Reply to every comment**, humbly. Expect skepticism — especially from Deaf users wary of hearing-built
  AI tools. Lead with "*complement to mentors, not a replacement*," and mean it.

### Facebook
**Where:** "Parents of Deaf/Hard of Hearing Children" groups, ASL-learning groups, Hands & Voices chapter
groups, and baby-sign-language groups (hearing parents already signing — strong adjacency).

**How:**
- **Join → answer the membership questions honestly** (many ask "why?"). Approval can take days.
- **Engage genuinely first**, then post the value-first copy from §1. Respect pinned rules — some ban
  promotion (look for a weekly "self-promo" thread, or ask an admin).
- Groups are higher-intent and less spam-sensitive than Reddit, but admins are strict — don't burn trust.

### Community-sensitivity note (ethics = strategy)
The Deaf community's principle is *"nothing about us without us."* A hearing-built ASL/AI tool will draw
scrutiny. Be humble, frame as practice *between* Deaf-mentor visits, invite critique, and ideally line up
a **Deaf advisor**. This protects the brand *and* gets you truer feedback.

### Cadence
1–2 channels/day, not a blast. Watch signups-by-`ref`, double down on what converts, and log dropped/
banned posts so "we tried everywhere" doesn't hide a channel that never actually ran.
