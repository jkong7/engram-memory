---
id: "m_tg7owirfp"
kind: "fact"
scope: "global"
title: "How Jonathan's Claude Code cloud sessions get context (claude-kit synced plugin, repo CLAUDE.md/skills, Research env) a…"
tags: ["claude-memory","cloud-sessions-setup"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.479Z"
updated: "2026-10-08T00:46:35.479Z"
source: "claude-code"
---

# How Jonathan's Claude Code cloud sessions get context (claude-kit synced plugin, repo CLAUDE.md/skills, Research env) a…

Set up 2026-09-21.

- Personal context lives in private repo `jkong7/claude-kit` (`~/dev/claude-kit`), a plugin marketplace with plugin `jonathan` (skill `about-jonathan`). Added on claude.ai > Customize > Plugins > Add > Add marketplace, auto-sync on, so pushes reach every cloud and terminal session. Edit that repo, not claude.ai, to change what sessions know.
- `apply` skill moved into `jkong7/jobsearch` at `.claude/skills/apply`; `~/.claude/skills/apply` is a symlink to it. jobsearch has a CLAUDE.md (ground truth files, hard rules, cloud vs local split).
- Cloud environments: two empty "Default" (Trusted network; routines use one) and "Research" (Full network, no secrets, no setup script) for interactive sessions that fetch company pages.
- GitHub already connected (routines run on private jobsearch), so /web-setup was not needed.
- Remote Control launcher was NOT created: the auto-mode classifier blocked both starting `claude remote-control` from a session and writing a `~/.local/bin/claude-rc` script with `--permission-mode auto`. Jonathan must start it himself.

**Why:** multi-repo cloud sessions don't load any repo's .claude config, and cloud VMs never see ~/.claude, so synced plugins and single-repo .claude/ are the only reliable carriers.
**How to apply:** keep user-level skills/context in claude-kit or the relevant repo, never only in ~/.claude. Related: [[jobsearch-pipeline]], [[raycast-claude-shortcuts]]
