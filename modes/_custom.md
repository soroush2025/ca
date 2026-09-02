# Custom Instructions — career-ops
# Soroush Gholami · Turkey market

<!-- ============================================================
     THIS FILE IS YOURS. It will NEVER be auto-updated.

     PROCEDURAL rules only — "HOW I want things done".
     WHO you are (archetypes, narrative, comp, negotiation scripts)
     lives in modes/_profile.md. Compact triage context lives in
     modes/_brief.md.

     Seeded 2026-09-02 from rules already stated in modes/_profile.md
     and config/profile.yml. Everything here survives
     `node update-system.mjs`. Edit freely.
     ============================================================ -->

## House Rules

**Work permit is a first-class evaluation dimension.** Iranian passport,
relocating to Turkey — every evaluation must state the sponsorship signal
explicitly, even when the JD is silent (say "not mentioned"). Never let a
report imply permit clarity that the posting does not actually provide.
Silence from a Turkey-only employer is a soft red flag, not a neutral.

**Quote compensation in USD or EUR, monthly, net.** If a posting advertises
TRY, convert it and show both (`TRY 120,000/mo ≈ USD X/mo net at <rate>, <date>`).
Never present a TRY figure alone as if it were comparable to the target range.

**Never suggest visiting portfolio or project URLs** in any evaluation block
(A–G), cover letter, or outreach message. No "check your work at
shahr-aghsat.com", no "see iransampler.com", no variants. If a gap needs
filling, describe the capability in plain language instead.

**Never write to `cv.md` during an evaluation.** Block E suggestions are
output-only — display them in the report, never apply them to disk. Soroush
decides what gets updated.

**Lead with the talent, not the link.** Framing order for every proof point:
achievement metric → what was built → which skill it proves. Never append a URL.
- ✅ "Built a BNPL wallet with Redis-queued installment notifications — use it to demonstrate async architecture"
- ❌ "Check shahr-aghsat.com to show the interviewer your payment work"

**Do not restate the BNPL transaction volume as settled.** `cv.md` carries two
different figures (100B IRR in the summary, 10B+ IRR everywhere specific). Use
`10B+ IRR/year` and flag the discrepancy until Soroush confirms which is right.
See the "Figure to confirm" section in `modes/_brief.md`.

**Cap batch runs at 20 listings** unless told otherwise.

## Custom Workflows

**"turkey scan"** — run `scan`, filter to Turkey-based employers and remote roles
open to Turkey, then triage against `modes/_brief.md`. Report PASS roles with the
work-permit signal on every line. Do not evaluate below the triage threshold.

**"istanbul shortlist"** — from the current tracker, list roles in `Evaluated`
state scoring ≥ 4.0 that have an Istanbul or remote-Turkey location and any
positive sponsorship signal. One line each: company · role · score · permit signal.

**"permit check <company>"** — before investing time on an application, research
whether the company has sponsored Turkish work permits before (careers page,
job-posting language, LinkedIn employee nationality mix). Report what was found
and what could not be established — no guessing.

**"prep <company>"** — pull the JD from the report, map `interview-prep/story-bank.md`
STAR stories onto it, and draft 5 likely questions. Run
`node story-provenance-check.mjs --summary` first and never present a
`derived-unverified` number as a settled fact.

## Output Preferences

- **All human-facing output in English.** Keep Turkish market terms (SGK, kıdem
  tazminatı, brüt/net maaş, BES) where relevant, but explain them inline.
- Reports lead with the score, the one-line verdict, and the work-permit signal.
- Comp always monthly + net + currency. Never a bare number.
- CV/PDF filenames stay in the existing convention:
  `cv-soroush-gholami-{company}-{role}-{YYYY-MM-DD}.pdf`.
- Tracker notes: carry the req/posting ID whenever the JD exposes one —
  several past targets post near-identical sibling titles (Insider, İyzico).

## Off-Limits

- **Never submit or send an application, form, email, or LinkedIn message.**
  Draft it, show it, stop. Soroush clicks the button.
- **Never invent a metric, a scale figure, or an authorship claim.** If it is not
  in `cv.md`, `article-digest.md`, `config/profile.yml`, or `modes/_profile.md`,
  ask — and if it does not get added, the output ships without it.
- **Never claim authorship of an open-source project.** The Umami / Twenty CRM /
  Dub.co entries in `cv.md` are *extensions and self-hosted deployments*, not
  authorship. Frame them exactly that way.
- **Never edit a system file to customize the setup** — `modes/_shared.md`,
  `AGENTS.md`, `CLAUDE.md` and the `*.mjs` scripts are auto-updatable.
  Customizations belong here, in `_profile.md`, or in `config/profile.yml`.
- Never put contact details (email, Telegram number) into a public artifact
  without being asked — they belong in the CV and application email only.
