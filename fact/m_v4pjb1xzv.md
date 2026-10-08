---
id: "m_v4pjb1xzv"
kind: "fact"
scope: "global"
title: "~/dev/blackbox local LLM/agent observability + eval tool (built 2026-10-07); 33 commits local, GitHub drip publisher st…"
tags: ["claude-memory","blackbox-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T01:33:37.583Z"
updated: "2026-10-08T02:04:01.880Z"
source: "claude-code"
---

# ~/dev/blackbox local LLM/agent observability + eval tool (built 2026-10-07); 33 commits local, GitHub drip publisher st…

~/dev/blackbox: local "flight recorder and judge" for AI agents, built 2026-10-07 after deep research (report: ~/dev/reports/LLM observability and eval market.md, notes in ~/dev/research_notes/LLM observability and eval market/).

Stack: Node 26 TS (no build), node:sqlite + FTS5, Vite/React UI in ui/ (build with `npm run ui:build`). Ports 7777 UI/API/OTLP, 4318 OTLP, 7778 LLM proxy. Data in ~/.blackbox by default. 50 tests pass.

Ingests OTel GenAI, OpenInference, OpenLLMetry, Vercel AI, OpenAI Agents, Claude Code traces+events (verified on real Claude Code 2.1.293), proxy (merges onto claude_code.llm_request via traceparent), MCP stdio wrapper, TS + Python SDKs, MCP server for agents. 17 label-free signals, 10 LLM judges via `claude -p` (telemetry stripped, daily cap) or API key, rules, calibration, datasets/experiments.

Finding worth telling Jonny: his Claude Code sends ~168-213 tool definitions (~66-119k tokens) on every call, so a haiku bug-fix task cost $0.24-0.34.

Git: 33 commits authored only Jonathan Kong, no Claude mentions (verified). Private repo github.com/jkong7/blackbox. Jonny ran .git/publisher/START.sh himself on 2026-10-07 20:18: launchd agent com.jkong7.blackbox-publisher pushes one SHA at a time with a random 600 to 5400s wait, log .git/publisher/publish.log, stops after the last queued commit. On 2026-10-07 20:47 it was fixed: zsh turned "$sha:refs/heads/main" into a bad refspec (the :r modifier), so nothing had pushed. The refspec is now "${sha}:..." and the queue was rebuilt to 37 commits (4 Codex/integration commits added). Stop: launchctl bootout gui/$(id -u)/com.jkong7.blackbox-publisher.

Related: [[code-style-no-comments]], [[git-no-claude-attribution]], [[vigil-repo]]
