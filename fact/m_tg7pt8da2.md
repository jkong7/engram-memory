---
id: "m_tg7pt8da2"
kind: "fact"
scope: "global"
title: "jkong7/cooked — live 1v1 hot-take debate app (Go/SQLite/SSE, Claude judge + local fallback, browser MP4 clips)"
tags: ["claude-memory","cooked-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.518Z"
updated: "2026-10-08T00:46:35.518Z"
source: "claude-code"
---

# jkong7/cooked — live 1v1 hot-take debate app (Go/SQLite/SSE, Claude judge + local fallback, browser MP4 clips)

jkong7/cooked (private, created 2026-09-25): 1v1 debates on a rotating take, 3 rounds of 45s, crowd vote plus judge, Elo tiers (Chud/NPC/Cooker/Menace/Goat), a cookbot AI opponent after 12s in the queue, challenge links, OG cards, in-browser 1080x1920 MP4 clips, 18+ gate, moderation and reports. The Claude layer uses claude-opus-5 with server-side fallbacks ("default") and only turns on when ANTHROPIC_API_KEY is set. No key exists on this Mac yet, so it runs on the local brain. Not deployed (needs the fly CLI and login).

The prompt library came from peer sessions: dev-6d (YouTube comment-rate study) and dev-8f (Reels reply counts). Race and looks-roast topics are deliberately excluded.

**Why:** Jonathan wants viral consumer apps built on "human desires". This was ranked #1 after sidebet.
**How to apply:** go.mod and the Dockerfile Go versions must match (golang images don't auto-download toolchains). See [[sidebet-repo]] and [[vigil-repo]].
