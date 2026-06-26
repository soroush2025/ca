# Article Digest — Soroush Gholami
# Proof Points, Case Studies & Portfolio Evidence

<!-- This file supplements cv.md with detailed proof points.
     Evaluations read this file for richer evidence mapping.
     Update whenever you ship something new, publish an article,
     or want to add context to a proof point. -->

---

## BNPL Platform — Shahr-e-Aghsat (shahr-aghsat.com)

**Type:** Production system · Full-stack ownership  
**Stack:** Laravel 10, Next.js 14, MySQL, Redis, BehPardakht/Mellat Bank gateway, Docker  
**Architecture:** Porto SAP (Containers/Ship), 12 independent modules  
**Scale:** 100B+ IRR/year in live transactions

### What was built
A complete Buy Now Pay Later (BNPL) / installment purchasing system for digital goods, built solo from scratch:

- **Wallet system** — user balance, credit allocation, transaction history
- **Loan management module** — credit scoring, loan origination, approval workflows
- **Installment scheduler** — configurable payment plans (3/6/12 months), automated reminders
- **Payment gateway integration** — BehPardakht (Mellat Bank), full error handling, idempotency, webhook validation, transaction reconciliation
- **Order management** — cart, checkout, BNPL flow, fulfillment tracking
- **User credit scoring** — rule-based scoring engine with manual override
- **Admin dashboard** — Next.js frontend, real-time reporting, fraud flagging
- **Notification system** — Redis-queued SMS/email for payment reminders, confirmations

### Key proof points to deploy
- "Single-handedly architected and shipped a 12-module BNPL platform — now processing 100B+ IRR/year in live transactions"
- "Zero payment failures over 6 months of live operation — idempotent gateway integration with full reconciliation"
- "Applied Porto SAP architecture (Containers/Ship pattern) — each module independently maintainable, zero cross-module coupling violations"
- "Redis queue workers for async installment processing — reduced notification latency from 30s to under 2s"

### When to use
- Fintech / payment roles: lead proof point
- Backend architecture roles: Porto + DDD evidence
- Full-stack roles: Laravel backend + Next.js frontend end-to-end ownership
- Scale questions: 100B+ IRR/year, concurrent transactions, queue processing

---

## AWS Enterprise Cloud Migrations (Amazon Web Services, Singapore)

**Type:** Enterprise delivery · Cloud architecture  
**Period:** Nov 2015 – Sep 2018 (3 years)  
**Scale:** 25+ enterprise applications, 20+ organizations, Southeast Asia  
**Cloud services:** EC2, S3, RDS, SQS, ElastiCache, Lambda, CloudFront, VPC, IAM

### What was done
Migrated enterprise clients from on-premise infrastructure to AWS across Malaysia, Singapore, and Vietnam:

- Designed cloud security architecture (VPC, security groups, IAM policies, encryption)
- Architected high-availability setups (multi-AZ RDS, Auto Scaling groups, load balancers)
- Migrated databases (Oracle, SQL Server → RDS), file systems (on-prem NAS → S3), and compute
- Provided technical onboarding and documentation for each client's engineering team
- Maintained 99.9% SLA during live migration windows

### Key proof points to deploy
- "Migrated 25+ enterprise applications to AWS across Southeast Asia — maintaining 99.9% SLA during live migration windows"
- "Designed cloud security and resilience architectures for 20+ organizations: VPC segmentation, IAM, multi-AZ RDS, Auto Scaling"
- "3 years embedded at Amazon Web Services — systems-level AWS knowledge from the inside"

### When to use
- Cloud/AWS roles: primary evidence
- Scale/reliability questions: SLA maintenance, enterprise complexity
- Backend systems roles: distributed systems awareness, infrastructure thinking
- Senior/Staff-level positioning: working at AWS itself is a strong signal

---

## Porto Architecture Practitioner

**Type:** Architectural methodology · Applied in 2 production systems

### What it is
Porto (Software Architectural Pattern — SAP) is a modular monolith pattern that organizes Laravel applications into:
- **Containers** — isolated business domain modules (Orders, Payments, Users, etc.)
- **Ship** — the framework core, shared infrastructure, and request dispatching
- **Actions** — single-responsibility use cases
- **Tasks** — reusable atomic operations
- **Repositories** — data access layer

### Where applied
1. **Shahr-e-Aghsat (BNPL platform)** — 12 containers (Wallet, Loans, Installments, Gateway, Orders, etc.), zero cross-container direct calls
2. **Sinapse (health AI platform)** — re-architected existing Laravel codebase from MVC spaghetti into Porto containers; separated health modules from AI integration contracts

### Key proof points to deploy
- "Porto Architecture practitioner — applied in 2 separate production systems (Shahr-e-Aghsat BNPL, Sinapse health AI)"
- "Converted legacy Laravel MVC codebase to Porto SAP at Sinapse — improved testability, reduced coupling, enabled parallel team development"
- "Porto's Container/Ship pattern is the real-world equivalent of DDD Bounded Contexts in Laravel — a direct match for Insider's modular monolith approach"

### When to use
- Modular monolith / DDD roles: direct evidence (Insider specifically uses this pattern)
- Code quality / architecture discussions: shows systematic thinking, not just "I've used Laravel"
- Tech lead interviews: architectural decision-making evidence

---

## IranSampler — Multi-tenant SaaS Survey Platform (iransampler.com)

**Type:** Product leadership · Full-stack delivery · Team lead  
**Stack:** Laravel, Vue.js, MySQL  
**Team:** Led up to 14 engineers  
**Product:** B2B SaaS survey/questionnaire platform (comparable to PorsLine / Typeform)

### What was built
- Multi-tenant data model — per-tenant schema isolation, tenant onboarding flow
- Dynamic form builder engine — drag-and-drop question types, conditional logic, branching
- Role-based access control — per-tenant user roles, team management
- Response analytics dashboard — charts, export to CSV/Excel, real-time results
- API layer for third-party integrations

### Key proof points to deploy
- "Architected multi-tenant SaaS with per-tenant data isolation serving 50+ enterprise clients on a single Laravel instance"
- "Led 14-person engineering team — code reviews, sprint planning, technical roadmap, mentoring junior developers"
- "Built dynamic form builder with conditional logic — comparable to PorsLine/Typeform functionality"

### When to use
- Multi-tenant SaaS roles: direct evidence
- Tech lead / leadership roles: team size, roadmap ownership
- Full-stack roles: Laravel + Vue.js delivery

---

## Innoghte WordPress → Laravel + React Migration (innoghte.com)

**Type:** Full-stack migration · Remote delivery  
**Stack:** WordPress (legacy) → Laravel 10 + React (modern)  
**Client:** US-based e-learning platform

### What was done
- Assessed legacy WordPress codebase — identified migration scope and risk
- Rebuilt all e-learning features: course management, user progress tracking, content delivery, subscription system
- Migrated database schema from WooCommerce/WordPress tables to clean relational design
- Rebuilt frontend from WordPress themes to React component architecture
- Zero-downtime migration — phased rollout with feature flags

### Key proof points to deploy
- "Delivered end-to-end WordPress → Laravel + React migration for US-based e-learning platform — zero downtime, all features rebuilt"
- "Improved page load performance by ~60% post-migration (WP overhead eliminated)"
- "Remote delivery for US client — async collaboration across timezones, English-language technical communication throughout"

### When to use
- Full-stack roles: end-to-end project ownership
- Migration / modernization roles: legacy-to-modern stack experience
- Remote work credibility: proven remote delivery for international client

---

## Cloud Computing Business Innovation Sdn. Bhd. (Malaysia, 2010–2019)

**Type:** Entrepreneurship · Enterprise software delivery  
**Status:** MSC-Status certified company (Malaysia's tech company certification)  
**Team:** Up to 14 engineers  
**Clients:** Government agencies, universities, private enterprises (Malaysia)

### What was built / delivered
- **ZAR** — web-based accounting platform for SMEs (.NET, SQL Server)
- **HR Management System** — Malaysian payroll compliance, leave management, performance tracking
- **Multi-tenant client portals** — for university and government clients
- **Maid agency automation** — booking, compliance tracking, government reporting

### Key proof points to deploy
- "Co-founded and grew an MSC-status IT company in Malaysia — 9 years, up to 14 engineers, government and university clients"
- "Named Top Web Developer Southeast Asia 2019"
- "Built and delivered payroll-compliant HR systems for Malaysian enterprises — local regulatory compliance experience"

### When to use
- Leadership / co-founder positioning: business ownership at scale
- Enterprise software: government/university clients
- International experience: Malaysia, Singapore, Vietnam, UK, Middle East — genuine multi-market credibility

---

## AI-Augmented Development Workflows

**Type:** Tooling / methodology  
**Tools:** Claude AI (Anthropic), GitHub Copilot, Cursor IDE, ChatGPT

### How used in production
- **Porto re-architecture at Sinapse** — used Claude to accelerate complex refactoring cycles under tight deadlines; identified coupling violations automatically
- **BNPL installment logic** — used Copilot for boilerplate generation; used Claude for edge-case reasoning on payment reconciliation rules
- **Code review** — Cursor IDE for inline AI suggestions during development; catch static analysis issues pre-commit

### Key proof points to deploy
- "Active AI-assisted development workflows using Claude AI, GitHub Copilot, and Cursor IDE — measurable velocity improvement on complex refactoring tasks"
- "Used LLM-assisted coding to deliver Sinapse Porto re-architecture under tight deadline — AI as force multiplier, not crutch"

### When to use
- Any role mentioning AI tools as nice-to-have (increasingly common in 2025–2026 JDs)
- Insider specifically listed Claude Code, Copilot, Cursor as desirable — this is a direct match

---

## Open Source Contributions & Extensions

**Type:** Production deployments of open-source platforms with custom extensions  
**Period:** Past 2 years  
**Repos:** github.com/umami-software/umami · github.com/twentyhq/twenty · github.com/dubinc/dub

### What was extended

- **Umami Analytics** — self-hosted Google Analytics alternative (Next.js + PostgreSQL). Extended with custom event tracking modules, multi-tenant dashboard support, RTL layout. Integrated as analytics backbone for e-commerce and BNPL platforms.
- **Twenty CRM** — open-source Salesforce alternative (Node.js + GraphQL + React). Extended GraphQL API for bulk lead imports with linked task creation. Configured OpenResty reverse proxy + SSL. Built custom lead pipeline flows.
- **Dub.co** — link attribution and short-link platform (Next.js + Prisma). Self-hosted and extended for campaign tracking across e-commerce funnels. Integrated with platform analytics pipelines.

### Key proof points to deploy
- "Extended 3 open-source platforms (Umami, Twenty CRM, Dub.co) in production — custom modules, GraphQL extensions, multi-tenant support"
- "Self-hosted and extended Umami Analytics with RTL support and multi-tenant dashboards for BNPL platform — zero third-party analytics dependency"
- "Extended Twenty CRM's GraphQL API with bulk import flows and OpenResty SSL configuration — full-stack open-source contribution"

### When to use
- Roles asking for open-source contribution experience
- Roles needing GraphQL API experience (Twenty CRM extension)
- Companies that value self-hosting / data ownership culture
- Full-stack roles: shows Next.js, GraphQL, PostgreSQL, Node.js hands-on work beyond just Laravel
