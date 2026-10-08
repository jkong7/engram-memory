---
id: "m_v4q6ytxnh"
kind: "fact"
scope: "global"
title: "~/dev/engram universal agent memory (MCP + hooks + daemon), installed live 2026-10-07; what is wired, what is pending,…"
tags: ["claude-memory","engram-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T01:33:38.401Z"
updated: "2026-10-08T01:33:38.401Z"
source: "claude-code"
---

# ~/dev/engram universal agent memory (MCP + hooks + daemon), installed live 2026-10-07; what is wired, what is pending,…

~/dev/engram (local git only, not pushed) is Jonny's cross-harness memory layer, built 2026-10-07 after research in ~/dev/research_notes/Agent memory systems/ (report: ~/dev/reports/Agent memory systems.md).

Live on the Mac since 2026-10-07: `engram` on PATH (~/.local/bin), daemon under launchd com.engram.daemon on 127.0.0.1:7432, data in ~/.engram (engram.db, mirror/ git, backups/, token). Claude Code: user-scope MCP "engram" + hooks in ~/.claude/settings.json (SessionStart, UserPromptSubmit, Stop, PreCompact, PostCompact, SessionEnd); cleanupPeriodDays raised to 365. Codex: [mcp_servers.engram] + ~/.codex/hooks.json, but Codex login was revoked and hooks need /hooks approval. Claude Desktop MCP on. ~/brain indexed as a docs source (journal, daily, inbox, health excluded). Extraction uses claude CLI Haiku, capped 20/hour.

Pending Jonny: `codex login` + approve hooks; remote (claude.ai/ChatGPT) needs `engram remote enable` + a tunnel, never exposed by Claude; GitHub drip publish was requested via another session's relay and blocked by the auto-mode classifier, so it needs his direct go-ahead (several commit messages mention Claude Code as an integration name and would need rewording first).

**Why:** he wants one persistent memory of him across Anthropic, OpenAI and Cursor tools.
**How to apply:** `engram doctor` for health, `engram uninstall <harness>` to undo, ENGRAM_DISABLE=1 to silence hooks. The harness session dev-a0 builds loom (~/dev/loom) against engram's REST/hook contract. Related: [[second-brain-architecture]], [[code-style-no-comments]]
