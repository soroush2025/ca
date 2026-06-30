# Story Bank — Master STAR+R Stories

This file accumulates your best interview stories over time. Each evaluation (Block F) adds new stories here. Instead of memorizing 100 answers, maintain 5-10 deep stories that you can bend to answer almost any behavioral question.

## How it works

1. Every time `/career-ops oferta` generates Block F (Interview Plan), new STAR+R stories get appended here
2. Before your next interview, review this file — your stories are already organized by theme
3. The "Big Three" questions can be answered with stories from this bank:
   - "Tell me about yourself" → combine 2-3 stories into a narrative
   - "Tell me about your most impactful project" → pick your highest-impact story
   - "Tell me about a conflict you resolved" → find a story with a Reflection

## Stories

---

### [Architecture] Building the BNPL Platform from Scratch
**Source:** Report #005 — Insider Backend PHP/Laravel · Report #006 — Insider Full-Stack  
**Best for:** "Complex system you architected" · "Own a project end-to-end" · "DDD/modular architecture in practice" · "High-throughput systems"

**S:** Hired as sole architect and developer for a new BNPL e-commerce platform (Shahr-e-Aghsat) — no existing codebase, no team, tight deadline.  
**T:** Design and build 12 modules including wallet, loan management, installment scheduling, and live BehPardakht/Mellat Bank payment gateway integration.  
**A:** Applied Porto SAP architecture (Containers/Ship) to isolate each business domain. Built Laravel 10 backend with DDD-influenced module boundaries — each Container owned its own Actions, Tasks, Repositories with zero cross-module coupling. Implemented Redis-based queue workers via Laravel Horizon for async installment processing. Integrated BehPardakht API with idempotent request design, retry logic, webhook validation. Used Claude AI to accelerate complex refactoring under deadline pressure.  
**R:** Platform shipped on time. Now processing 10B+ IRR/year in live transactions. Zero payment failures over 6 months of production operation.  
**Reflection:** Porto forced domain boundaries early — made the payment module completely replaceable when we needed to swap gateway configurations. Next time: add contract tests between modules from day one rather than retrofitting them.

---

### [Scale] AWS Enterprise Migrations (Amazon Web Services, Singapore)
**Source:** Report #005, #010 — Insider · Report #008 — Insider Fullstack  
**Best for:** "Significant technical scale" · "Cloud infrastructure experience" · "SLA maintenance during migrations" · "Cross-functional collaboration"

**S:** At Amazon Web Services Singapore — migrating enterprise clients from on-premise to AWS across Southeast Asia (Malaysia, Singapore, Vietnam). 25+ applications, 20+ organizations.  
**T:** Maintain 99.9% SLA during live migration windows, design cloud security/resilience architectures, onboard client engineering teams.  
**A:** Designed VPC segmentation, IAM policies, encryption per client. Architected multi-AZ RDS, Auto Scaling, load balancers. Ran phased migration windows with database replication lag monitoring. Wrote runbooks and technical documentation. Adapted architecture per client's stack (Oracle, SQL Server, PHP, .NET).  
**R:** 25+ applications migrated, 99.9% SLA maintained. 20+ organizations onboarded across 3 countries over 3 years. Zero critical incidents during migration windows.  
**Reflection:** The migration plan matters less than the rollback plan. Every smooth migration happened because I had a tested rollback procedure — not because the migration itself went perfectly.

---

### [Refactoring] Porto Re-Architecture at Sinapse Under Deadline
**Source:** Report #005 — Insider Backend PHP/Laravel  
**Best for:** "Refactoring a large legacy codebase" · "Tackling technical debt" · "Tight deadlines on complex technical work" · "AI tools in development workflow"

**S:** Joined Sinapse — inherited a Laravel health AI platform with MVC spaghetti. Business logic scattered across controllers, no separation between health domain and AI integration. Tight deadline to stabilize for product expansion.  
**T:** Re-architect the backend into Porto SAP without breaking the running system.  
**A:** Audited codebase, identified 6 primary Containers. Extracted Actions and Tasks layer by layer, starting with the most isolated domain. Used Claude AI to identify coupling violations and generate migration checklists. Defined clean API contracts with the AI/ML team so models could be swapped without touching business logic.  
**R:** Full Porto re-architecture delivered within project timeline. API response times reduced through query optimization during the refactor. AI/ML team could now iterate on models independently.  
**Reflection:** Underestimated implicit coupling in controllers. Next time: run PHPStan + custom dependency rules before starting — makes the extraction order obvious rather than discovered through trial.

---

### [Leadership] Leading the IranSampler Team of 14
**Source:** Report #006 — Insider Full-Stack · Report #005 — Insider Backend  
**Best for:** "Leading a team through a complex project" · "Code reviews and technical standards" · "Management style" · "Growing engineers on your team"

**S:** Joined IranSampler as Team Lead — tasked with building a SaaS survey platform while managing a team of 14 engineers with inconsistent coding standards.  
**T:** Deliver the platform on time while establishing technical processes that would scale with the team.  
**A:** Introduced PR-based code review workflow with architecture review gates. Ran weekly architecture sessions. Created coding standards grounded in SOLID and Clean Architecture. Set up GitLab CI with PHPStan and automated tests. Mentored 3 junior developers through their first production PRs.  
**R:** Platform shipped. Multi-tenant architecture supporting 50+ enterprise clients. Junior developers adopted Clean Architecture patterns within 3 months.  
**Reflection:** Reviewing every PR myself created a bottleneck early. Fixed it by designating 2 senior developers as co-reviewers and explicitly defining what required architect review — freed me for higher-value architectural decisions.

---

### [Migration] Zero-Downtime WordPress → Laravel + React Migration
**Source:** Report #006 — Insider Full-Stack Backend Heavy  
**Best for:** "Successful migration project" · "Managing risk during live migration" · "Significant performance improvement" · "Remote work and async collaboration"

**S:** Innoghte (US-based e-learning platform) — entire product on WordPress/WooCommerce hitting scalability ceiling. Business needed a modern stack but couldn't take downtime.  
**T:** Migrate the full platform from WordPress to Laravel + React with zero downtime and no feature regression.  
**A:** Audited WordPress functionality for feature parity checklist. Built new Laravel + React stack in parallel with live site. Rebuilt each module one by one (courses, progress tracking, subscriptions). Used feature flags to gradually route traffic. Final cutover: DNS switch with 15-minute overlap where both systems ran live.  
**R:** Zero-downtime migration. Page load improved ~60% (WordPress overhead eliminated). All features rebuilt, no regression. Remote delivery for US client, fully async English-language collaboration.  
**Reflection:** Feature flags added significant complexity. For smaller projects: big-bang cutover with tested rollback. Feature flags only justify the overhead when regression risk is very high.

---

### [Reliability] Mellat Bank Gateway Integration — Zero Failures
**Source:** Report #005 — Insider Backend PHP/Laravel  
**Best for:** "Payment systems experience" · "Designing for failure" · "Reliability in financial software" · "Integration work"

**S:** Building the payment gateway integration for the BNPL platform — BehPardakht (Mellat Bank) API for a live payment flow where failures directly meant lost sales.  
**T:** Design an integration reliable enough for a financial product — zero duplicate charges, zero lost transactions, recoverable from any failure state.  
**A:** Designed idempotent request model (unique idempotency key per transaction). Built three-phase flow: initiate → gateway redirect → webhook confirmation with database state machine. Added webhook signature validation. Built nightly reconciliation job to catch transactions where gateway and database state diverged. Tested all failure modes: network timeout, webhook delivery failure, gateway downtime.  
**R:** Zero payment failures over 6 months of live operation. Reconciliation job caught 3 edge cases in the first month (all auto-recovered). No user-facing errors attributable to the integration.  
**Reflection:** The reconciliation job was the most valuable thing I built — not because failures were frequent, but because it gave confidence and an audit trail. I now add reconciliation to any financial integration by default.

---

### [Entrepreneurship] Co-founding CCBI Malaysia (9 years, MSC-status)
**Source:** Report #010 — Insider Senior SE PHP/Go  
**Best for:** "Building something from zero" · "Stakeholder management" · "Wearing multiple hats" · "Entrepreneurial background"

**S:** Co-founded Cloud Computing Business Innovation Sdn. Bhd. in Malaysia from zero — no clients, no team, no revenue. Target: government agencies and universities.  
**T:** Build a sustainable technology company, win government contracts, scale a technical team.  
**A:** Started self-funded with 2 co-founders. Won first government contract by outcompeting larger vendors on customization and responsiveness. Grew to 14 engineers over 9 years. Obtained MSC-Status certification. Delivered ZAR accounting platform, HR management systems with Malaysian payroll compliance, multi-tenant university portals.  
**R:** Company ran 2010–2019. Named Top Web Developer Southeast Asia 2019. MSC-Status certified. Clients: government, universities, private enterprises across Malaysia.  
**Reflection:** Was the technical bottleneck for too long — writing code, doing sales, and managing team simultaneously for the first 3 years. Delegating technical leadership earlier would have allowed faster growth. The lesson carried forward: build explicit technical processes from day one so delegation doesn't sacrifice quality.
