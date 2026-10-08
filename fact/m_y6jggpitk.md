---
id: "m_y6jggpitk"
kind: "fact"
scope: "project:~/dev/burner"
title: "Burner dev server lifecycle"
tags: ["burner","dev-server"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T02:59:02.217Z"
updated: "2026-10-08T02:59:02.217Z"
source: "claude-code claude-code:1f5a085b-bd97-4878-8653-44e4af7a0e80"
---

# Burner dev server lifecycle

The Burner dev server runs on port 3007 (`npx next dev -p 3007`) inside the shell of the Claude session that started it. Closing that session stops the server, and it must then be restarted.
