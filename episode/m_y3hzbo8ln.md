---
id: "m_y3hzbo8ln"
kind: "episode"
scope: "global"
title: "blackbox build and publisher setup"
tags: ["claude-code"]
importance: 3
trust: "extracted"
status: "active"
created: "2026-10-08T02:56:40.221Z"
updated: "2026-10-08T02:56:40.221Z"
source: "claude-code claude-code:c9e8d63e-6ff3-4f80-b662-57da7ca4f394"
---

# blackbox build and publisher setup

Jonny asked for deep research on AI agent observability and eval market leaders, then a local build without interruption. The agent wrote a market report at ~/dev/reports/LLM observability and eval market.md and built blackbox, a local flight recorder and judge with SQLite storage, OTLP and Claude Code telemetry ingest, a proxy, an MCP wrapper, SDKs, a React UI, and an eval engine. Ingest was optimized from about 244 to 7,800 spans/s, and an independent review found 13 backend bugs that were then fixed. Jonny then asked how to start the publisher, and the agent set up a launchd job that pushes the 33 queued commits to the private repo jkong7/blackbox one at a time.
