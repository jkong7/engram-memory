---
id: "m_tg7jkmrou"
kind: "preference"
scope: "global"
title: "Jonathan adopts stack technologies and MCP servers as concrete needs arise, not preemptively"
tags: ["claude-memory","purpose-driven-tooling"]
importance: 8
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.299Z"
updated: "2026-10-08T00:46:35.299Z"
source: "claude-code"
---

# Jonathan adopts stack technologies and MCP servers as concrete needs arise, not preemptively

Jonathan prefers to build purpose-first and pull in stack technologies, MCP servers,
and services only when a real need surfaces — not to pick a stack or install tooling up front.
Decided 2026-09-19 while setting up a new machine, after declining to choose a
deploy target / database / service set in advance.

**Why:** Committing to a stack before the problem is understood installs tools that
go unused, and every idle MCP server costs context on every request.

**How to apply:** Don't front-load stack decisions or offer long menus of services.
Build with what's installed, and when a task genuinely needs a capability
(a database, a deploy target, error tracking), propose that one thing at that moment
with the reason it's needed now. See [[machine-setup-2026-09]].
