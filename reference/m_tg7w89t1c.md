---
id: "m_tg7w89t1c"
kind: "reference"
scope: "global"
title: "Jonny's second agent \"Instinct\" (iMessage/WhatsApp/calls) submits applications and writes to jkong7/jobsearch; coordina…"
tags: ["claude-memory","instinct-agent"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.738Z"
updated: "2026-10-08T00:46:35.738Z"
source: "claude-code"
---

# Jonny's second agent "Instinct" (iMessage/WhatsApp/calls) submits applications and writes to jkong7/jobsearch; coordina…

Instinct is an invite-only personal AI agent Jonny texts or calls (iMessage/WhatsApp; web at app.instinct.com). Since ~2026-10-01 it runs his recruiting end to end: finds roles, fills AND submits applications, verifies receipts, and commits ledger/queue/blocklist/dossiers to jkong7/jobsearch main. The `phonemsg-...` ids in PROFILE.md are its records of his texts. It has Google Workspace (Gmail, Calendar, Drive, Tasks), not Todoist. It also handles reminders, food orders, cancellations.

Coordination (2026-10-02): `AGENTS.md` in jkong7/brain and jkong7/jobsearch splits ownership. Instinct hands Jonny to-dos via files in brain/inbox/ or email to jonathankong677+brain@gmail.com; the Capture Triage routine files them into Todoist/vault. Claude never submits applications.

**How to apply:** before touching application state, pull jobsearch and read the ledger/queue; expect Instinct commits. Don't duplicate its work. Related: [[jobsearch-pipeline]], [[second-brain-architecture]]

Errand lane (2026-10-04): Instinct reads Todoist read-only. Capture Triage routes errands (orders, purchases, cancellations, calls, "tell Instinct...") to Todoist project "Instinct" (id 6hgrvHg2rhqQQfrH). Instinct sweeps it hourly at :15, 7am-1am CT, and reports with `instinct-report: <done|need-you|failed>: <task title>: <line>` as a brain/inbox file or +brain email; triage completes or flags (needs-you) the task, and results reach the Brief/Digest. Rules are in brain/AGENTS.md. Jonny pastes the setup message to Instinct himself.

Messenger (2026-10-04): every routine (Morning Brief 8:55am CT, renamed from Afternoon Brief 2026-10-04 at his request for 9am, Career Sync 6pm, Digest 8:55pm, Weekly Sun 4pm, Builder per PR, Triage per finished research/draft/urgent/needs-you) also adds a `📬 Message: <kind>` task in project Instinct; Instinct iMessages the description verbatim at :15. Triage completes 📬 tasks older than 90 min. Claude app pushes kept on as backup; around 2026-10-11 ask Jonny whether Instinct delivered reliably and whether to turn the Claude pushes off.
