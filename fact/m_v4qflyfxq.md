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
updated: "2026-10-08T02:04:03.670Z"
source: "claude-code"
---

# ~/dev/loom model-agnostic agent harness (SDK + CLI/TUI + server) built on engram memory; local only, GitHub drip pendin…

~/dev/loom is the model-agnostic agent harness built 2026-10-07 from a brief relayed through dev-e0. It is TypeScript on Node 26 type stripping with zero runtime deps.

- Layers: ai/ (providers + registry + tool shim), agent/ (loop, hooks, permissions, sessions, compaction, snapshots), memory/ (MemoryProvider + EngramProvider, harness name "loom"), tools/, mcp/, runtime, cli/, server/.
- Research notes: ~/dev/research_notes/Agent harnesses/00-07. 07 is the build report.
- Engram added a loom transcript parser in 705615c.
- Status: 43 commits. Drip publisher com.jkong7.loom-publish (.git/drip-publish.sh, queue .git/drip-queue, log ~/Library/Logs/loom-publish.log) has been running since 2026-10-07 20:20 and pushes to private jkong7/loom. It re-reads the queue each loop, so new commits are queued by appending SHAs. The 8 telemetry commits were appended 10/7 20:48.

**Why:** Jonny wants to stay ahead on harness, context and memory engineering ([[building]]). loom is the harness counterpart to [[engram-repo]].

**How to apply:** To publish new commits, append SHAs to .git/drip-queue; never start a second publisher. Plain `loom` runs write to his real engram unless --no-memory.
