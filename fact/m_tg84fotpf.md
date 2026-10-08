---
id: "m_tg84fotpf"
kind: "fact"
scope: "global"
title: "Jonathan's Claude Code launch shortcuts live in ~/.local/bin, bound to Cmd+1/2/3 by skhd (not Raycast)"
tags: ["claude-memory","raycast-claude-shortcuts"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:36.031Z"
updated: "2026-10-08T00:46:36.031Z"
source: "claude-code"
---

# Jonathan's Claude Code launch shortcuts live in ~/.local/bin, bound to Cmd+1/2/3 by skhd (not Raycast)

Claude Code launch shortcuts live in `~/.local/bin/` (shared worker in `lib/claude-open-tiled.py`), open sessions in **Terminal.app** via `osascript`, and are bound by **skhd** in `~/.config/skhd/skhdrc`: ⌘1 `claude-dev` (fresh session in ~/dev), ⌘2 `claude-last-session` (most recent ~/dev session not already open in a window, via `--skip-open`; default size), ⌘3 `claude-last-3-tiled` (3 most recent ~/dev sessions tiled in thirds), ⌘4 `claude-apply` (Terminal session in ~/dev/jobsearch, prompt in `lib/apply-prompt.md`: fills pending Instinct `handoffs/` packets, then the top 15 queue rows by priority, in Chrome, one tab at a time, stops before Submit, ends with a needs-you Todoist task), ⌘⇧O `caffeinate-toggle` (background `caffeinate -d` on/off with a notification, PID in `~/.cache/caffeinate-toggle.pid`; added 2026-10-05). Jonny 2026-10-04: nothing runs automatically, every apply run starts from an explicit ⌘4 press (a launchd watcher was blocked by the auto-mode classifier and he chose hotkey only). Sessions are ranked by transcript mtime in `~/.claude/projects` and scoped to ~/dev.

Moved off Raycast script commands on 2026-09-19 (the old `~/raycast-scripts/` folder is deleted) because Raycast hotkeys can only be assigned by hand in its UI, while skhd is a config file.

**Why:** he asks for these by hotkey number and wants the whole thing configurable from files, not a GUI.

**How to apply:** add new shortcuts as executable scripts in `~/.local/bin` plus a line in `skhdrc`, then `skhd --restart-service`. The config is `~/.config/skhd/skhdrc` only; there is no `~/.skhdrc` (a binding written there on 10/5 silently never loaded). Two gotchas learned the hard way: a Terminal spawned from inside a Claude session inherits `CLAUDECODE`/`CLAUDE_CODE_SESSION_ID` and the nested Claude exits instantly (scrub that env with `env -u`), and window-to-session matching must read Terminal window titles, since tty numbers get recycled.
