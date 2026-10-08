---
id: "m_tg89n1feq"
kind: "fact"
scope: "global"
title: "Todoist is Jonathan's single always-visible task list (free plan), wired to Claude via the official doist plugin; proje…"
tags: ["claude-memory","todoist-setup"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:36.221Z"
updated: "2026-10-08T00:46:36.221Z"
source: "claude-code"
---

# Todoist is Jonathan's single always-visible task list (free plan), wired to Claude via the official doist plugin; proje…

Set up 2026-10-02 as layer 1 of the second-brain architecture (research report: ~/dev/reports/Personal Jarvis stack on Mac.md).

- Account: jonathankong677@gmail.com, Todoist Free (5-project limit; Inbox + 4 used), timezone America/Chicago, week starts Sunday.
- Claude access: official plugin `todoist@doist` (marketplace doist/todoist-mcp, HTTP MCP at ai.todoist.net/mcp), user scope, OAuth done via /mcp.
- Projects: School, Career (sections Applications, Networking, Interviews), Projects (one section per repo: chartside, sessionside, sidebet, cooked, vigil, flow-kit, persona-onboarding), Life.
- Labels: from-email, rolled-over, waiting, quick, deep, claude.
- Recurring in Life: "Done for today" every day 9pm, "Weekly review" every Sunday 4pm.

**Why:** the Reddit/research consensus is one list with phone + Mac widgets, Claude keeps it current, Notion stays an archive.
Free plan has NO deadline field (API 403 PREMIUM_ONLY): put hard expiries in the task title, e.g. "(expires Sat 10/3 1:44pm)". Initial fill 2026-10-02: 25 Career tasks from ledger/Gmail, 11 Projects tasks from repo state. career-sync skill (~/dev/jobsearch/.claude/skills/career-sync) keeps Career in step with the ledger using a `ledger:<id>` marker on the last description line; the initial 25 tasks lack the marker.

**How to apply:** move dates with reschedule-tasks, never update-tasks (breaks recurrence). Never delete tasks without asking. Don't add a 5th project without checking the free limit. Related: [[jobsearch-pipeline]], [[no-morning-blocks]]
