---
id: "m_vuk0c1czc"
kind: "episode"
scope: "global"
title: "Burner architecture walkthrough"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T18:41:29.925Z"
updated: "2026-10-10T00:09:28.108Z"
source: "claude-code claude-code:e93bf3b6-8bdc-49bd-822e-3c5c15b165e2"
---

# Burner architecture walkthrough

On 2026-10-09 Jonny asked how Burner works in its current state, since it has a lot of state, before deciding what to build next. A dense overview did not land, so the assistant re-explained it as three parts: a per-player save file, a timed queue that drives events, and AI models that write text and make photos. Jonny then asked whether the save file holds the whole world, and the assistant answered that each player's file holds their own life while characters, diaries and generated media are shared. The assistant began a full layer-by-layer diagram, which was cut off. No code or config was changed.
