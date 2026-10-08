---
id: "m_tg7z1pdc3"
kind: "fact"
scope: "global"
title: "Mac folder layout after 2026-09-21 cleanup (~/dev for all code, ~/projects symlink, screenshots, Documents/Career) and…"
tags: ["claude-memory","local-machine-layout"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.849Z"
updated: "2026-10-08T00:46:35.849Z"
source: "claude-code"
---

# Mac folder layout after 2026-09-21 cleanup (~/dev for all code, ~/projects symlink, screenshots, Documents/Career) and…

Layout set 2026-09-21 (new Mac, set up 2026-09-17):
- All code lives in ~/dev (jobsearch, resume). ~/projects is a HIDDEN symlink to ~/dev kept for old hardcoded paths (jobsearch merge scripts); don't delete it.
- ~/dev/resume is now backed up to private GitHub jkong7/resume.
- Screenshots save to ~/Pictures/Screenshots (defaults com.apple.screencapture location).
- ~/Documents/{Career,School,Personal}; resumes + transcript in Career.
- Removed on the user's OK: iMovie, GarageBand (+ /Library sound libraries), Keynote/Pages/Numbers Creator Studio. Trash emptied. Kept ChatGPT, Codex, Cursor.
- Messages attachments are 26 GB (iCloud sync, mostly .MOV). The user asked to see the largest; left in place, and they should be pruned through System Settings > Storage > Messages, never by deleting files directly.
- ~/Library/Application Support/Claude/vm_bundles (11 GB) is the Claude desktop VM; keep.

**Why:** the user wants dev work consolidated in ~/dev and a tidy Finder. Related: [[raycast-claude-shortcuts]], [[jobsearch-pipeline]]
