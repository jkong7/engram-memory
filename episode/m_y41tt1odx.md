---
id: "m_y41tt1odx"
kind: "episode"
scope: "project:~/dev/loom"
title: "Loom harness build and publishing"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T02:57:05.999Z"
updated: "2026-10-08T02:57:05.999Z"
source: "claude-code claude-code:d8484a11-5b9c-44ec-9729-6f9a615d5c50"
---

# Loom harness build and publishing

Over 2026-10-08 the agent built ~/dev/loom, a model-agnostic harness with 35 local commits and 69 passing tests, including real runs against qwen3:8b and the real engram daemon. A subagent review found 12 correctness issues, including permission bypasses, and these were fixed with tests. Jonathan approved a drip publisher to a private jkong7/loom repo after Claude auto mode blocked the repo creation and background job, so he ran the setup commands himself; the assistant reported the publisher started.
