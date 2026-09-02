# Soroush Gholami — Triage Brief

<!-- ============================================================
     THIS FILE IS YOURS. USER LAYER — never auto-updated.
     Derived 2026-09-02 from cv.md + config/profile.yml + modes/_profile.md.

     Compact context for first-pass triage (`modes/triage.md`).
     Keep it short — read once per role in a batch. Deep narrative,
     negotiation scripts and STAR stories stay in _profile.md / cv.md.
     ============================================================ -->

## Identity
Senior Full-Stack Developer — 15+ yrs (Malaysia · Singapore · Vietnam · Middle East · UK M.Sc.).
Currently Middle East (UTC+3:30), relocating to Istanbul (UTC+3), ready in 4–8 weeks.
**Iranian passport — requires employer-sponsored Turkish work permit.** English IELTS 7.0 (C1+).

## Target Archetypes

| # | Archetype | What they buy (your proof) |
|---|-----------|----------------------------|
| 1 | **Senior Full-Stack Developer** | Laravel + React/Next.js on real product platforms — built a 12-module BNPL system end-to-end (backend architecture *and* shipped UI) |
| 2 | **Senior Backend Engineer** | PHP 8/Laravel 10–11 or Node.js, REST/GraphQL, MySQL/PostgreSQL/Redis optimization, AWS + Docker |
| 3 | **Tech Lead / Lead Developer** | Led up to 14 engineers as co-founder/CEO (CCBI Malaysia); team lead at IranSampler; Porto/Clean Architecture practitioner |

**Analog titles that still count as hits** (score 4–5, not a miss): Senior PHP Developer · Senior Laravel Developer · Software Engineer (backend-weighted) · Full Stack Engineer · Platform Engineer · Senior Web Developer.

## Proof Points (use exact metrics in matching)
- **BNPL platform, solo architect** — 12 modules (wallet, loan management, credit scoring, installment scheduling), Laravel + Next.js, live BehPardakht/Mellat gateway. ⚠️ See "Figure to confirm" below before quoting the transaction volume.
- **AWS Singapore, 3 yrs** — migrated 25+ enterprise applications on-premise → AWS; onboarded 20+ organizations across Southeast Asia.
- **Co-founder & CEO, MSC-status IT company (Malaysia, 2010–2019)** — team of up to 14 engineers; accounting platform, HR/payroll with Malaysian tax compliance, multi-tenant portals.
- **Porto architecture in two production systems** — Sinapse (AI health platform re-architecture) and Shahr-e-Aghsat (BNPL).
- **WordPress → Laravel + React migration** for a US e-learning platform, end-to-end, zero downtime.
- **M.Sc. Software Engineering, Staffordshire University (UK)** — GPA 17/20, thesis on cloud-based distributed systems.

## Comp Strategy
Currency: **USD or EUR preferred** (avoids TRY volatility). All figures monthly, net.

| Target | Requirement |
|--------|-------------|
| USD 3,000–5,000 | Standard ask for Istanbul senior full-stack / backend |
| USD 5,000–6,000 | Top of range — high scope, lead/architect title, or strong equity |
| Below USD 3,000 | Under walk-away — MARGINAL at best, needs a compelling non-comp reason |

**Hard floor: USD 2,500/month net equivalent. Below that, FAIL regardless of other signals.**
For Istanbul on-site: relocation support (one-time flight + first month accommodation) is a negotiable line item, not a comp substitute.

## Location Scoring
- Remote, Turkey-based company → **5.0**
- Istanbul on-site or hybrid → **4.5**
- Remote, any country → **4.0**
- Ankara on-site → **3.5**
- On-site 5 days/week outside Istanbul/Ankara, no flexibility → **1.5**
- High travel (>25%) → deduct 0.5–1.0

## Work Permit Scoring (Turkey-specific — weight this, it is a real gate)
- JD explicitly mentions visa/work-permit sponsorship → **5.0**
- Multinational / 30+ countries / known relocation program → **3.5**
- Turkish SME, no mention → **1.5**
- JD states Turkish citizenship required → **DISQUALIFIER, score ≤ 2.0**

## Hard DQ Criteria — instant FAIL (< 3.0)
- Turkish citizenship required / explicitly no permit sponsorship
- Junior, entry-level, or internship
- Pure frontend / CSS / UI-design-only role
- PHP 5.x or legacy stack with no stated modernization plan
- Comp clearly below USD 2,500/month net equivalent
- Commission-only, equity-only, or freelance-only structure
- Core discipline outside scope: Data Scientist, ML Engineer, DevOps-only, QA, Scrum Master, Product Manager

## Quick Scoring Guide

Bands are relative to `triage_threshold` (`config/profile.yml → pipeline.triage_threshold`, default **3.5**).

| Score | Verdict | What it means |
|-------|---------|---------------|
| ≥ threshold (default 3.5) | **PASS** | Clears the bar — archetype + comp + location + permit signal all workable |
| 3.0 – (threshold − 0.1) | **MARGINAL** | Borderline — surface as one line |
| < 3.0 | **FAIL** | Filtered |

## Soft Red Flags (−0.5 each, additive)
- No mention of work-permit sponsorship at a Turkey-only employer
- Mobile-first role (iOS/Android hands-on) — real gap, not framable
- "Must have public GitHub / open-source portfolio" as a hard requirement
- TRY-denominated comp with no inflation adjustment clause
- WordPress-primary role (capability exists, but it is a downward framing)
- Agency / body-shop staffing model with undisclosed end client
- Team under ~5 engineers with no senior peer

## Priority Override List — always return PASS regardless of score
Turkish fintech named as a target in the exit narrative — surface these even on a weak JD.
- Papara — fintech, direct archetype match, already evaluated (report 001)
- İyzico — payments, direct archetype match (reports 002–004)
- Trendyol — e-commerce at scale (reports 011, 012, 016)
- Insider — SaaS, PHP/Go stack (reports 005–010)
- Moka / Moka United — payments
- Peak Games — already evaluated (report 017), gaming/backend at scale
- Getir, Dream Games — scale employers worth a look; sponsorship posture unverified, confirm in Block G

## ⚠️ Figure to confirm before it goes in any output

`cv.md` states the Shahr-e-Aghsat BNPL transaction volume **two different ways**:

| Where | Figure |
|-------|--------|
| Professional Summary | "over **100B IRR** in annual transactions" |
| Shahr-e-Aghsat experience bullet | "**10B+ IRR** in annual sales" |
| Shahr-e-Aghsat proof point | "now processing **10B+ IRR**/year" |
| Key Projects table | "**10B+ IRR** annual sales" |

`config/profile.yml` and `modes/_profile.md` inherit the same split (100B in the
proof-point lists and elevator pitch, 10B in the STAR story and framing table).

**Until Soroush confirms which is correct, triage and generated content use
`10B+ IRR/year`** — it is the figure attached to the specific role, and it
appears three times to the summary's one. Understating is recoverable;
overstating a transaction volume to a fintech interviewer is not.

Once confirmed, fix it in `cv.md` first (primary source), then `config/profile.yml`,
`modes/_profile.md`, and this file.
