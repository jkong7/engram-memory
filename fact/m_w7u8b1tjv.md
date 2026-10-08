---
id: "m_w7u8b1tjv"
kind: "fact"
scope: "global"
title: "loom + engram + blackbox wired together via OTel/traceparent on 2026-10-07; uncommitted in loom/blackbox, engram trace…"
tags: ["claude-memory","infra-stack-integration"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T02:04:03.171Z"
updated: "2026-10-08T02:04:03.171Z"
source: "claude-code"
---

# loom + engram + blackbox wired together via OTel/traceparent on 2026-10-07; uncommitted in loom/blackbox, engram trace…

On 2026-10-07 the three infra repos were integrated:

- loom: src/telemetry/ (OTLP JSON exporter with GenAI conventions, AsyncLocalStorage traceparent). The Agent emits run/llm/tool/memory spans. traceparent goes to engram REST and MCP (header plus params._meta). Config `telemetry` or OTEL_EXPORTER_OTLP_ENDPOINT. Tests: test/telemetry/otel.test.ts and test/e2e/stack.test.ts (real engram + blackbox from sibling checkouts). 74/74 pass.
- engram: src/trace.ts, request spans by memory op (recall/search/digest/create/ingest/capture), extractor traces, and the hook CLI forwards TRACEPARENT. dev-e0 owns the engram repo and was told to commit this as its own commit.
- blackbox: src/sources/codex.ts builds traces from Codex `codex.*` log events (before this, Codex showed 0 LLM calls). 52/52 pass.
- Verified with real models on an isolated stack: qwen3:8b via loom, Claude Haiku via Claude Code (`CLAUDE_CODE_PROPAGATE_TRACEPARENT=1` nests engram inside the Claude Code trace), and Codex. Memory written by one harness was recalled by the others, and blackbox judges (claude-cli) scored the loom trace.

**Why:** Jonny asked to make the memory layer, harness and LLM ops work together end to end and be startup-ready ([[engram-repo]], [[loom-repo]], [[blackbox-repo]]).

**How to apply:** Committed 10/7 as incremental commits (loom 8, blackbox 4) and queued on each repo's drip publisher. The live machine is not wired yet (Claude Code settings env, live engram config telemetry endpoint). Ask before changing those.
