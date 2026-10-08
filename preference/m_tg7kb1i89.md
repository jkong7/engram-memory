---
id: "m_tg7kb1i89"
kind: "preference"
scope: "global"
title: "Application location fields: San Francisco, CA for every non-Chicago role; Evanston, IL only for Chicago-based roles (o…"
tags: ["claude-memory","application-location-default"]
importance: 8
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.323Z"
updated: "2026-10-08T00:46:35.323Z"
source: "claude-code"
---

# Application location fields: San Francisco, CA for every non-Chicago role; Evanston, IL only for Chicago-based roles (o…

On job application current location / city of residence fields: **San Francisco, CA** for every role that is not Chicago-based (Bay Area, California, NYC, everywhere else). **Evanston, IL** only when the role is Chicago-based. Relocation is a separate question (always yes).

**Why:** Jonathan, 2026-10-06 in a local Claude Code session: "use SAN FRANCISCO if the role is cali based ... and evanston ill if its CHICAGO based use SAN FRANCISCO for anything not chicago". Restores the 2026-09-23 rule and replaces the 2026-10-01 Evanston-for-everything rule.

**How to apply:** pick the location by the role's metro at fill time. PROFILE.md and tools/form_defaults.py still carry the older Evanston default until updated, so override by hand. Mailing-address-only fields keep the San Jose address. Related: [[jobsearch-pipeline]], [[one-application-per-company]]
