---
id: "m_y3hpm11sy"
kind: "procedure"
scope: "project:~/dev/blackbox"
title: "SQLite FTS5 ingest: key rows by rowid, not span_id"
tags: ["sqlite","fts5","performance"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T02:56:39.942Z"
updated: "2026-10-08T02:56:39.942Z"
source: "claude-code claude-code:c9e8d63e-6ff3-4f80-b662-57da7ca4f394"
---

# SQLite FTS5 ingest: key rows by rowid, not span_id

Deleting FTS5 rows by span_id scans the whole table for every span because that column is unindexed, which made ingest quadratic (about 244 spans/s). Keying FTS rows by the span's rowid raised ingest to about 7,800 spans/s. Check delete paths for unindexed FTS columns before tuning anything else.
