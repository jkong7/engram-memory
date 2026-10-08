---
id: "m_y7uvuyc4s"
kind: "fact"
scope: "project:~/dev/burner"
title: "Burner port layout for testing"
tags: ["burner","testing","dev-server"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T03:00:03.665Z"
updated: "2026-10-08T03:00:03.665Z"
source: "claude-code claude-code:51d0a4e1-e320-4c03-8676-2cd69dcd598e"
---

# Burner port layout for testing

Jonny's live Burner world runs on port 3007 and must not be used for testing. Tests run on a separate server on port 3008 with its own data folder, which holds Sam's world.
