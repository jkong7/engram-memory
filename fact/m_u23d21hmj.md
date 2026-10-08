---
id: "m_u23d21hmj"
kind: "fact"
scope: "global"
title: "~/dev/cue = Cue, improved Cluely rebuild (Electron overlay, me/them audio, memory, practice, calendar); 21 commits queu…"
tags: ["claude-memory","cue-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T01:03:35.957Z"
updated: "2026-10-08T01:03:35.957Z"
source: "claude-code"
---

# ~/dev/cue = Cue, improved Cluely rebuild (Electron overlay, me/them audio, memory, practice, calendar); 21 commits queu…

~/dev/cue: Cue, a real-time conversation copilot rebuilt from Cluely (picked 2026-10-07 from a 10-startup SF scan; reports in ~/dev/reports "SF AI startups shortlist 2026-10.md" and "Cluely teardown 2026-10.md").

State 2026-10-07: built and verified in rehearsal mode (17 tests pass, scripted calls end to end, calendar, dashboard). Not yet run with real keys: needs ANTHROPIC_API_KEY + DEEPGRAM_API_KEY in Settings or .env (I couldn't read burner's .env, deny rule). System audio uses native/cue-audio.swift (ScreenCaptureKit), tested working.

Git: 21 per-component commits on local main, all authored Jonathan Kong, no Claude mentions. Private repo github.com/jkong7/cue created with origin remote, nothing pushed. The random 10-90 min drip publisher (launchd) was blocked by the auto-mode classifier as persistence because the request came relayed from another session; needs Jonny's direct go-ahead.

Dev hooks: CUE_AUTOSTART=<playbook>, CUE_SCRIPT_SPEED, CUE_AUTOSTOP_MS, CUE_SNAPSHOT_DIR (captures only Cue windows, keeps them hidden), CUE_USER_DATA, CUE_CALENDAR_ICS.

Related: [[code-style-no-comments]], [[git-no-claude-attribution]], [[verse-medical-clone]]
