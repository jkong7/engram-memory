---
id: "m_zy6kw1ghm"
kind: "fact"
scope: "global"
title: "Pushback publisher needs Mac awake"
tags: ["pushback","publishing"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T03:48:31.503Z"
updated: "2026-10-08T03:48:31.503Z"
source: "claude-code claude-code:86ba8e22-d8fe-4156-9f0a-cc2b17bcb738"
---

# Pushback publisher needs Mac awake

Pushback's publisher runs on Jonny's Mac, so commits only land while the Mac is awake and online. Sleep pauses its countdown, offline pushes fail and retry on the next cycle, and progress persists in .git/publish/state.
