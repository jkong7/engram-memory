---
id: "m_zrsb62kei"
kind: "preference"
scope: "global"
title: "Secrets pass through the clipboard"
tags: ["security","tooling"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-10T22:54:37.774Z"
updated: "2026-10-10T22:54:37.774Z"
source: "claude-code claude-code:e93bf3b6-8bdc-49bd-822e-3c5c15b165e2"
---

# Secrets pass through the clipboard

Jonny keeps service secrets out of the chat. When he copies a password or key, the agent gives him a ! shell command that reads the clipboard into .env.local, and the agent never sees the value.
