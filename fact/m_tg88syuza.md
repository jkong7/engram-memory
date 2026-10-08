---
id: "m_tg88syuza"
kind: "fact"
scope: "global"
title: "jkong7/sidebet — play-money friend prediction market app (Go/SQLite/SSE/LMSR); real-money pot requested but not built"
tags: ["claude-memory","sidebet-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:36.200Z"
updated: "2026-10-08T00:46:36.200Z"
source: "claude-code"
---

# jkong7/sidebet — play-money friend prediction market app (Go/SQLite/SSE/LMSR); real-money pot requested but not built

jkong7/sidebet (private, created 2026-09-25): "put odds on your friends" group prediction markets. Play money, LMSR odds, SSE live updates, OG share cards, group-owner void, per-IP rate limit. Fly.io config is there but not deployed (no fly CLI or login yet).

Campus Markets were added 2026-09-25. /g/nu is Northwestern: .edu email codes, mods set with CAMPUS_ADMINS, no bets about people on campus, and a report queue. Email needs SMTP_* env vars, which aren't set up yet (codes are only logged). DEV_CODES=1 is for local testing only. LAUNCH.md has the NU beachhead plan. LAUNCH.md has video scripts based on ~/dev/reels-research.

Jonathan asked for a real-money group pot on 2026-09-25. It was not built: Stripe and similar processors prohibit gambling, and holding and redistributing stakes on outcomes is regulated gambling. He hasn't decided on a zero-custody settle-up alternative.

**Why:** he wants viral consumer apps. The earlier "vice speed-dial" idea was blocked by the real-world-transactions permission check.
**How to apply:** keep sidebet play-money unless he explicitly chooses a lawful design. Never place real bets or orders on his accounts. See [[vigil-repo]].
