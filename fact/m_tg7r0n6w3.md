---
id: "m_tg7r0n6w3"
kind: "fact"
scope: "global"
title: "~/dev/flow-kit public repo (jkong7/flow-kit); plugin v0.2.0 installed at user scope, skhd/Raycast/statusline not wired…"
tags: ["claude-memory","flow-kit-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.549Z"
updated: "2026-10-08T00:46:35.549Z"
source: "claude-code"
---

# ~/dev/flow-kit public repo (jkong7/flow-kit); plugin v0.2.0 installed at user scope, skhd/Raycast/statusline not wired…

Built 2026-09-21 at the user's request after a research sweep on popular Claude/Raycast/macOS flow-state automations. Public at github.com/jkong7/flow-kit. Contents:
- a Claude Code plugin with the notify / guard_bash / autoformat hooks, 6 skills (today, plan-day, followups, prep, weekly-review, triage-inbox), a `/push` command, and a statusline
- `bin/ask`, `bin/capture`, `bin/flow`
- Raycast script commands and an skhd example

State as of 2026-09-21:
- The plugin (flow-kit@flow-kit v0.2.0) is installed at user scope via its own marketplace. Update it with `claude plugin marketplace update flow-kit && claude plugin update flow-kit@flow-kit`.
- The six skills were commands until v0.2.0. `/push` deliberately stays a command.
- The user was asked to enable Raycast's Hyper Key (Caps Lock) in the Raycast UI; it has no config file.
- Not wired yet, and each needs the user's go-ahead: skhd bindings, the Raycast script directory, the statusline setting, and `~/.config/flowkit/flow.json`.

Related: [[raycast-claude-shortcuts]], [[code-style-no-comments]], [[git-no-claude-attribution]]


Update 2026-10-02 (v0.3.0, pushed and installed): added guard_tools.py (PreToolUse on mcp__.*: denies Gmail send/forward/reply and Drive share, asks on trash/delete/archive/label/spam, respond_to_event, and calendar invites to non-own emails via FLOWKIT_OWN_EMAILS), action_log.py (PostToolUse logs connector writes to ~/.local/state/flowkit/actions.jsonl), the `shutdown` skill, and `today` now reads Todoist + the ~/brain/daily handoff. Part of the second-brain build; see [[second-brain-architecture]].
