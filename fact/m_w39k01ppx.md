---
id: "m_w39k01ppx"
kind: "fact"
scope: "project:~/dev/jobsearch"
title: "Ledger writes via outbox file"
tags: ["job-search","workflow"]
importance: 5
trust: "extracted"
status: "active"
created: "2026-10-08T02:00:30.182Z"
updated: "2026-10-08T02:00:30.182Z"
source: "claude-code claude-code:e099b35c-082e-5d0c-8b80-129f07d3b9d8"
---

# Ledger writes via outbox file

Sessions without ledger access write rows to state/ledger_outbox.json in ~/dev/jobsearch. A session with ledger access copies them into the Application Ledger, typically by running /apply.
