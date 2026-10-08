---
id: "m_y5p5o5tgn"
kind: "fact"
scope: "global"
title: "Agents cannot read burner .env keys"
tags: ["cue","burner","environment"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T02:58:22.922Z"
updated: "2026-10-08T02:58:22.922Z"
source: "claude-code claude-code:f44417fd-b49b-44ce-9eab-ff7322d77b46"
---

# Agents cannot read burner .env keys

A deny rule blocks agents from reading ~/dev/burner/.env, so Cue has never run against real Claude or Deepgram keys. Keys must be supplied another way for live tests.
