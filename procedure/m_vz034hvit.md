---
id: "m_vz034hvit"
kind: "procedure"
scope: "global"
title: "Restarting the engram daemon"
tags: ["engram","daemon","launchd"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T01:57:11.285Z"
updated: "2026-10-08T01:57:11.285Z"
source: "claude-code claude-code:a7c69623-88f0-4d50-9f5b-3f8b4f20f09a"
---

# Restarting the engram daemon

With the engram launchd agent installed, use `engram daemon start|stop|restart`, which routes through launchctl. A manually started daemon conflicts with launchd over port 7432.
