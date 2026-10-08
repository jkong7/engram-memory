---
id: "m_zufnk13oz"
kind: "fact"
scope: "global"
title: "~/dev/prism live visualizer for loom + engram + blackbox runs (launchd com.prism.server on 127.0.0.1:7360), built 2026-…"
tags: ["claude-memory","prism-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T03:45:36.247Z"
updated: "2026-10-08T03:45:36.247Z"
source: "claude-code"
---

# ~/dev/prism live visualizer for loom + engram + blackbox runs (launchd com.prism.server on 127.0.0.1:7360), built 2026-…

~/dev/prism (local git only) visualizes everything behind a prompt for Jonny's own stack: it embeds loom as a library (patches Agent.prototype.prompt to subscribe to every agent incl. subagents and capture the exact request via onPayload), splits each request into labeled context segments, enriches memory ids from engram, replays blackbox traces, stores events in ~/.prism/prism.db and streams them over SSE to a React UI (Live story + loop ring + gauge, Context inspector with per-call columns/diff/raw, Timeline, Tools, Memory, Cost, Raw, simple/standard/expert, glossary, 6-step tour). Installed with `prism install` (PATH link ~/.local/bin/prism + launchd com.prism.server, port 7360); runs default to cwd ~/dev. Research in ~/dev/research_notes/Agent trace visualization/. Runnable models today: local Ollama (qwen3:8b/14b/32b) and mock; cloud models need API keys. blackbox is not a persistent service, so history only shows while it runs. The sibling Claude-Code-only visualizer is lantern (~/dev/lantern, port 7350, built by session dev-be).

**Why:** Jonny wants a layman-friendly, live view of the loop, context window, tools, memory and model behind each prompt.
**How to apply:** rebuild the UI with `npm run build` after UI edits and `launchctl kickstart -k gui/$(id -u)/com.prism.server` after server edits. Related: [[engram-repo]]
