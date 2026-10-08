---
id: "m_tg81r1g2m"
kind: "fact"
scope: "global"
title: "Jonny's everyday notes = separate Obsidian vault \\\"Notes\\\" in iCloud (~/notes, private repo jkong7/notes), Apple Notes…"
tags: ["claude-memory","notes-in-brain"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.935Z"
updated: "2026-10-08T00:46:35.935Z"
source: "claude-code"
---

# Jonny's everyday notes = separate Obsidian vault \"Notes\" in iCloud (~/notes, private repo jkong7/notes), Apple Notes…

On 2026-10-04 all 63 Apple Notes were copied to markdown, text exact, file mtimes = Apple last-edit date. Same afternoon he asked for them kept apart from the brain vault files, so they now live in their own Obsidian vault:

- Path: `~/Library/Mobile Documents/iCloud~md~obsidian/Documents/Notes`, symlink `~/notes`.
- Folders mirror Apple Notes: Career, Fitness, Journal, Lists, Notes, Personal, School, Thoughts, plus one root `Attachments/` (83 images, gitignored, synced by iCloud only).
- Backup: private repo jkong7/notes, pushed every 10 min by `~/.local/bin/notes-sync` (launch agent com.jkong.notes-sync). Git dir is `.git.nosync` (a `.git` file points to it) so iCloud skips it; gh CLI does not detect the repo there, use plain git.
- `~/brain` also moved into the same iCloud folder (symlink kept). Background jobs reading iCloud need /bin/zsh Full Disk Access, which he granted 2026-10-04.
- Raycast Notes was rejected (no folders, text only, UI automation unreliable). Raycast Obsidian extension is installed; its "Search Note" covers every vault unless its "Path to Vault" pref is set.

- Mac read/write path = custom Raycast extension "My Notes" (~/dev/raycast-notes, dev mode via `npx ray develop`): folder dropdown + sections like Apple Notes, Enter edits in a Raycast form, ⌘N new note, never opens Obsidian. He does NOT want Obsidian on the Mac ("the whole point was not to have another app"); Obsidian is only the phone app.

**Why:** he wants to stop using Apple Notes, stay lightweight, see his notes like Apple's folder list, and have everything synced to his phone.

**How to apply:** "my notes" means `~/notes`. Don't reorganize or rewrite them. `Journal/` there is private like brain's `journal/`: never quote it elsewhere. Related: [[second-brain-architecture]].
