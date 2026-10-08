---
id: "m_tg8arj375"
kind: "fact"
scope: "global"
title: "~/dev/verse-medical DME platform replica (private jkong7/verse-medical); built 2026-09-27, publishing via timed queue"
tags: ["claude-memory","verse-medical-clone"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:36.266Z"
updated: "2026-10-08T00:46:36.266Z"
source: "claude-code"
---

# ~/dev/verse-medical DME platform replica (private jkong7/verse-medical); built 2026-09-27, publishing via timed queue

~/dev/verse-medical is complete as of 2026-09-27: a replica of the public Verse Medical marketing site plus a platform designed independently from public descriptions. It has provider, patient, partner, analytics, payor and manufacturer portals (apps/web), the "Verse OS" ops console (apps/ops), and a Flask/Ariadne/Postgres API with an ML and coverage-rules layer (apps/api). Tests: 102 Playwright e2e, 648 pytest, 143 web vitest, 28 ops vitest. Seed: `python -m verse.cli seed --scale full` (150k orders); demo password `VerseDemo!2026` for demo.provider@verse.local and admin@verse.local.

Publishing: ~/dev/.verse-publisher/publish.sh (launchd-parented, started by the user) commits queue.tsv entries 20–30 min apart to the private repo jkong7/verse-medical and stops at the STOP line. Its progress is in the `state` file and `publish.log`.

**Why:** the user wanted small incremental commits with no Claude co-author lines ([[git-no-claude-attribution]]).
**How to apply:** the auto-mode classifier blocks Claude from launching the publisher and from appending to queue.tsv, so hand the user tab-safe `printf '%s\t%s\n'` commands to run. Don't use Verse's proprietary source maps or the schema derived from them; that use was blocked earlier. Open items: duplicate WorkItems in verse_development (the code fix is in), and the Claude extraction engine has never run against the real API.
