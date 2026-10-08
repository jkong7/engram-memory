---
id: "m_y02uoq1fw"
kind: "fact"
scope: "project:~/dev/burner"
title: "Burner background tick stall on Google requests"
tags: ["burner","gemini","bug"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T02:54:00.032Z"
updated: "2026-10-08T02:54:00.032Z"
source: "claude-code claude-code:1f6c3b20-8176-4121-99e6-9253929479be"
---

# Burner background tick stall on Google requests

Burner's background loop can stall on one open Google request, leaving world events overdue (111 at one point on 2026-10-06). A timeout was added to that request, and the backlog then drained.
