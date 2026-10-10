---
id: "m_zrs3jyteg"
kind: "fact"
scope: "project:~/dev/burner"
title: "Live and test servers for Burner"
tags: ["burner","testing"]
importance: 6
trust: "extracted"
status: "active"
created: "2026-10-10T22:54:37.486Z"
updated: "2026-10-10T22:54:37.486Z"
source: "claude-code claude-code:e93bf3b6-8bdc-49bd-822e-3c5c15b165e2"
---

# Live and test servers for Burner

Jonny's live Burner world runs on port 3007 and must not be used for testing. Tests run on a separate server on port 3008. Since 2026-10-10 both servers use the same Supabase database, so the 3008 test life starts empty.
