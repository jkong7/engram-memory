---
id: "m_y04ec12dy"
kind: "episode"
scope: "global"
title: "Burner Gemini playtest"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T02:54:00.823Z"
updated: "2026-10-08T02:54:00.823Z"
source: "claude-code claude-code:1f6c3b20-8176-4121-99e6-9253929479be"
---

# Burner Gemini playtest

Jonny asked for a concise status of the Burner project, which uses Gemini on Vertex after a switch in llm.json. The agent playtested Gemini in a test life on port 3008, confirmed live replies and crowd output were good, and found that the background loop stalled on a Google request with 111 overdue events. It added a timeout, and the backlog began draining. Smoke tests and typecheck passed. The session was cut off before the final report.
