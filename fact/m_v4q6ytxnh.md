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
updated: "2026-10-08T02:04:02.351Z"
source: "claude-code"
---

# ~/dev/engram universal agent memory (MCP + hooks + daemon), installed live 2026-10-07; what is wired, what is pending,…

~/dev/engram (local git only, not pushed) is Jonny's cross-harness memory layer, built 2026-10-07 after research in ~/dev/research_notes/Agent memory systems/ (report: ~/dev/reports/Agent memory systems.md).

Live on the Mac since 2026-10-07: `engram` on PATH (~/.local/bin), daemon under launchd com.engram.daemon on 127.0.0.1:7432, data in ~/.engram (engram.db, mirror/ git, backups/, token). Claude Code: engram hooks + MCP REMOVED 2026-10-07 by Jonny's choice (Claude auto-memory is the more token-efficient source for Claude Code; engram stays for other harnesses; backup ~/.claude/settings.json.bak-engram; daemon transcript tailer still ingests Claude Code transcripts). cleanupPeriodDays raised to 365. Codex: [mcp_servers.engram] + ~/.codex/hooks.json, but Codex login was revoked and hooks need /hooks approval. Claude Desktop MCP on. ~/brain indexed as a docs source (journal, daily, inbox, health excluded). Extraction uses claude CLI Haiku, capped 20/hour.

Published: Jonny chose PUBLIC on 2026-10-07. History was rewritten to strip personal data (fictional persona Sam Rivera in fixtures, user name from config user.name) and Claude mentions from commit messages; public repo github.com/jkong7/engram; drip publisher launchd com.jkong7.engram-publish (~/dev/engram/.git/drip-publish.sh, queue .git/drip-queue, log ~/Library/Logs/engram-publish.log) pushes 46 commits one at a time with random 600-5400s gaps, started 2026-10-07 20:59 CT, expected done around 2026-10-09 midday. New commits after that need appending to the queue; never rewrite main while it runs. Pending: codex hooks approved; remote tunnel never exposed by Claude.

**Why:** he wants one persistent memory of him across Anthropic, OpenAI and Cursor tools.
**How to apply:** `engram doctor` for health, `engram uninstall <harness>` to undo, ENGRAM_DISABLE=1 to silence hooks. The harness session dev-a0 builds loom (~/dev/loom) against engram's REST/hook contract. Related: [[second-brain-architecture]], [[code-style-no-comments]]
