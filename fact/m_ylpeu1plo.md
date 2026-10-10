---
id: "m_ylpeu1plo"
kind: "fact"
scope: "global"
title: "~/dev/verdict fragrance shelf verdict app (working name), Swift package + iOS app target, local only, state as of 2026-…"
tags: ["claude-memory","verdict-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-10T22:21:54.172Z"
updated: "2026-10-10T22:51:52.510Z"
source: "claude-code"
---

# ~/dev/verdict fragrance shelf verdict app (working name), Swift package + iOS app target, local only, state as of 2026-…

~/dev/verdict is the fragrance "judge" app from the build spec at ~/dev/reports/Fragrance score app build spec.md. "Verdict" is a working name Claude picked, not approved by Jonny. Local git only, no remote (2026-10-10).

Layout: Swift package with VerdictCore (scoring, daily pick, blind-buy, roast, seed catalog), VerdictUI (SwiftUI screens + share card), verdict-card CLI (renders card PNGs to out/), App/ + project.yml (XcodeGen).

**Why:** capped 60-day creator-distribution test; fallback is running the same test on [[burner-repo]].

**How to apply:**
- This Mac has only Command Line Tools, no Xcode (checked 2026-10-10). Run tests with `./test.sh` (plain `swift test` cannot find the Testing framework). The iOS app has never been built or run; that needs Xcode installed, then `xcodegen generate`.
- Seed catalog (56 bottles) holds Claude-written accord estimates as a dev fixture, not licensed data. Fragella terms section 3.3 bars caching large portions without plan permission; licensing email was drafted, not sent.
- Added 10/10: blind test mode (judge ranks lettered strips, agreement % card), crowding penalty, buy-next picks, FragellaSource live catalog client (reads FRAGELLA_KEY or VERDICT_CATALOG_URL env; never run against the real API, no key yet). `swift run verdict-mac --demo` opens the app as a Mac window. After changing VerdictCore types, `rm -rf .build` if tests segfault (stale incremental build).
- Jonny declined to email Fragella (10/10). His 16 bottles come from fragrantica.com/@jkong "Perfumes I Have".
- Web version added 10/10: `swift build -c release --product verdict-server && .build/release/verdict-server` serves Web/ + JSON API on http://localhost:7420 (Mac only, uses Network framework and SwiftUI card rendering). Test it with Playwright (own browser). Never screen-capture or script Jonny's desktop to test the Mac window. Blind tests append to data/blind_tests.jsonl. Paywall is a demo unlock, no billing.
- Known scoring flaw: a 6-bottle shelf can score 95 A+ and beat a 16-bottle shelf; small shelves score too easily.
- Not built yet: camera/OCR scan, Cloud Run proxy (Claude roast + recognition), paywall (isUnlocked is a debug toggle), WeatherKit, onboarding quiz, friend head-to-head.
- Bottle ranking uses averaged (Shapley-style) contributions instead of the spec's plain leave-one-out, because leave-one-out gave zeros and negatives on duplicate-heavy shelves.
