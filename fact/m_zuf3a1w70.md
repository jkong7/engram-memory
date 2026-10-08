---
id: "m_zuf3a1w70"
kind: "fact"
scope: "global"
title: "~/dev/lantern live Claude Code visualizer (port 7350); launcher, data sources, what is pending"
tags: ["claude-memory","lantern-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T03:45:35.445Z"
updated: "2026-10-08T03:45:35.445Z"
source: "claude-code"
---

# ~/dev/lantern live Claude Code visualizer (port 7350); launcher, data sources, what is pending

~/dev/lantern (built 2026-10-07, 30 commits, 19 tests; private jkong7/lantern) is a live plain-English visualizer for Claude Code: agent loop, per-call context window to scale with "why is this here", exact API requests, tools, helpers, memory, side calls, cost. Server: `node ~/dev/lantern/src/cli.ts serve` on 127.0.0.1:7350. Full fidelity via `node ~/dev/lantern/src/cli.ts claude …` (uses --settings ~/.lantern/claude-settings.json: http hooks + OTel + OTEL_LOG_RAW_API_BODIES=file:~/.lantern/bodies). Transcript-only view works for every session with zero setup.

Drip publisher (started 10/7 22:43): launchd com.jkong7.lantern-publish, script .git/drip-publish.sh, queue .git/drip-queue (append SHAs for new commits), log ~/Library/Logs/lantern-publish.log, 10-90 min apart, pushes SHA to main; idles when drained, exits once .git/drip-done exists. Never start a second publisher.

**Why:** Jonny asked (via dev-e0) for a comprehensive live visualizer of everything behind a prompt; dev-e0 builds the loom/engram/blackbox equivalent.

**How to apply:** `lantern install` (global ~/.claude/settings.json, backed up, reversible with `uninstall`) was NOT run; it needs Jonny's OK. Research + data-source matrix in ~/dev/research_notes/Claude Code visualizer/. Key facts: first-party requests use server-side message threads (continue requests send deltas only); a proxy via ANTHROPIC_BASE_URL disables tool search, so avoid it. Related: [[blackbox-repo]], [[infra-stack-integration]].
