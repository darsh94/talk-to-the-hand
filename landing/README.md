# Talk to the Hand — demand-test landing page

A single static file (`index.html`) that runs the demand test from `PROJECT.md`: emotional parent
hook → waitlist capture → **pricing probe with the B2B/grant A/B arm** in one submit. No backend.

## Deploy (Netlify or Vercel — pick one, both free)

**Netlify (drag-and-drop, fastest):** app.netlify.com → "Add new site" → "Deploy manually" → drag the
`landing/` folder in. Done.

**Vercel / Netlify from Git:** point it at this repo, set **base directory = `landing`**, framework =
"Other / static". Auto-deploys on push.

## Before it can collect data — 3 plug-ins (marked in `index.html`)

1. **Form endpoint (required).** Create a free form at **formspree.io** (or Tally). Paste its POST URL
   into `<form action="REPLACE_WITH_FORM_ENDPOINT">`. One submit captures `email` + `plan_interest`.
   - `plan_interest` values: `free_only`, `paid_9`, `paid_19`, `program_provided` (← the B2B/grant arm).
2. **Analytics (required for the conversion metric).** Add a Plausible/Umami/GA snippet in `<head>`
   (commented placeholder is there) so you can measure **visits → signups**.
3. **Demo clip (optional but converts).** Replace the `#demo` placeholder with the ILY clip.

## Reading the result — against the LOCKED thresholds (PROJECT.md §Success metrics)

Measure over the **1–3 day run window**:

| Signal | Bar |
|---|---|
| **GO** | ≥30% visits→signup **and** ≥100 signups **and** ≥30% picking a paid tier (`paid_9`/`paid_19`) |
| **PIVOT** | Good signups but selections skew `free_only` / `program_provided` → chase a paying segment (the B2B/grant arm tells you if "sold to programs" is the way) |
| **KILL** | <~15% visits→signup **and** parents satisfied with free mentors |

## Traffic (per plan)

Unpaid first: warm up in FB parent-of-deaf-kids groups + reach a **Hands & Voices** chapter contact
before posting (no link-dropping). Paid boost capped at **$50–100**, only after community-access is
confirmed. No Reddit for now.
