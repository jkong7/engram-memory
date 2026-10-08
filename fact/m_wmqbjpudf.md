---
id: "m_wmqbjpudf"
kind: "fact"
scope: "global"
title: "Triage and Builder run as claude.ai routines"
tags: ["automation","infrastructure"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T02:15:38.378Z"
updated: "2026-10-08T02:15:38.378Z"
source: "claude-code claude-code:93915de0-1e68-4016-8a4d-db941390eaf5"
---

# Triage and Builder run as claude.ai routines

Jonny's Capture Triage (hourly, 7am to 1am CT) and Builder (every 2 hours at :30, noon to midnight CT, lab only) run as claude.ai routines, not as local launchd or cron jobs. Checking the Mac's local schedulers finds nothing.
