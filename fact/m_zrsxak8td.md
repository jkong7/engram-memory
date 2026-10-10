---
id: "m_zrsxak8td"
kind: "fact"
scope: "project:~/dev/burner"
title: "Burner data lives in Supabase"
tags: ["database","supabase"]
importance: 7
trust: "extracted"
status: "active"
created: "2026-10-10T22:54:38.519Z"
updated: "2026-10-10T22:54:38.519Z"
source: "claude-code claude-code:e93bf3b6-8bdc-49bd-822e-3c5c15b165e2"
---

# Burner data lives in Supabase

Burner's player worlds, characters, diaries and push subscriptions are stored in Supabase Postgres. The app connects through the session pooler on port 5432, since port 6543 rejected the new password on 2026-10-10. The public Data API is off and row-level security is on.
