---
id: "m_v4qflyfxq"
kind: "fact"
scope: "global"
title: "~/dev/loom model-agnostic agent harness (SDK + CLI/TUI + server) built on engram memory; local only, GitHub drip pendin…"
tags: ["claude-memory","loom-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T01:33:38.863Z"
updated: "2026-10-08T01:33:38.863Z"
source: "claude-code"
---

# ~/dev/loom model-agnostic agent harness (SDK + CLI/TUI + server) built on engram memory; local only, GitHub drip pendin…

~/dev/loom is the model-agnostic agent harness built 2026-10-07 from a brief relayed through dev-e0. It is TypeScript on Node 26 type stripping with zero runtime deps.

- Layers: ai/ (providers + registry + tool shim), agent/ (loop, hooks, permissions, sessions, compaction, snapshots), memory/ (MemoryProvider + EngramProvider, harness name "loom"), tools/, mcp/, runtime, cli/, server/.
- Research notes: ~/dev/research_notes/Agent harnesses/00-07. 07 is the build report.
- Engram added a loom transcript parser in 705615c.
- Status: 35 commits, local only. A drip publisher to jkong7/loom was requested by relay, but the permission classifier blocked it as persistence and the original brief said do not push.

**Why:** Jonny wants to stay ahead on harness, context and memory engineering ([[building]]). loom is the harness counterpart to [[engram-repo]].

**How to apply:** Publish only after Jonny approves directly. Plain `loom` runs write to his real engram unless --no-memory.
