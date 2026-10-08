---
id: "m_y3hrb1qg3"
kind: "fact"
scope: "project:~/dev/blackbox"
title: "Nanosecond timestamps stored as REAL"
tags: ["sqlite","otlp","timestamps"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T02:56:40.044Z"
updated: "2026-10-08T02:56:40.044Z"
source: "claude-code claude-code:c9e8d63e-6ff3-4f80-b662-57da7ca4f394"
---

# Nanosecond timestamps stored as REAL

blackbox stores OTLP nanosecond timestamps in REAL-affinity columns because reading them back from SQLite as integers overflows JavaScript safe integers.
