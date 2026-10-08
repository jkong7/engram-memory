---
id: "m_tg888xso1"
kind: "fact"
scope: "global"
title: "~/dev/sessionside, \\\"Say it once. Sign a note Medicaid will accept.\\\" School SLP/OT/PT notes to Medicaid claims; privat…"
tags: ["claude-memory","sessionside-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:36.169Z"
updated: "2026-10-08T00:46:36.169Z"
source: "claude-code"
---

# ~/dev/sessionside, \"Say it once. Sign a note Medicaid will accept.\" School SLP/OT/PT notes to Medicaid claims; privat…

~/dev/sessionside was built 2026-09-28 across two passes.

**Research behind it (all in ~/dev/reports/):**
- Underserved AI niche opportunities.md
- Low interface AI design.md
- School therapy Medicaid market.md: competitors, Illinois go-to-market, state rules, practitioner pain, trust

**Stack.** Next 16, node:sqlite, Tailwind 4, Vitest (84 tests), Playwright (31 e2e, including axe WCAG 2.1 AA scans). Dev server runs on port 3400, e2e on 3401.

**Engines.** The offline rules engine is the default. Claude (claude-opus-5-5, structured output, fallbacks "default") is optional via ANTHROPIC_API_KEY.

**Built:**
- group dictation split into one note per student
- sourced rule packs for IL, NY, TX, and MI
- pre-claim checks, including a school attendance cross-check
- make-up minutes ledger and IEP progress reports
- draft-vs-final audit log and audit binder
- export profiles and CSV imports
- district overview (documentation and capture rates)
- trust page and full district data export
- immutable signed records, hashed sessions, and login lockout

**Positioning.** Lead with claim-ready notes and ending double entry, not "AI writes your notes" (r/slp has a strong anti-AI streak). Pricing idea from the report: $720 per provider per year, with pilots under Illinois' $35K bid threshold.

**Why:** portfolio project distinct from chartside that could become a startup. Validation path is Northwestern speech-therapy students and Illinois special ed co-ops.

**How to apply:**
- Private repo jkong7/sessionside on main; push only when asked.
- Commit per component, no comments, no Claude trailers, no em dashes.

**Not built yet:**
- SSO and OneRoster sync
- direct Frontline/EdPlan connectors
- California rules
- home-language parent summaries
- time study reminders
- a signed agreement with the AI provider

Related: [[chartside-repo]], [[code-style-no-comments]], [[git-no-claude-attribution]], [[no-em-dashes]]
