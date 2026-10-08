---
id: "m_xp426k3nv"
kind: "fact"
scope: "global"
title: "~/dev/cc = public jkong7/CC- CS 322 compiler (L1/L2/L3/IR C++ on PEGTL); being extended 10/7 with drip publisher"
tags: ["claude-memory","cc-compilers-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T02:45:28.773Z"
updated: "2026-10-08T02:45:28.773Z"
source: "claude-code"
---

# ~/dev/cc = public jkong7/CC- CS 322 compiler (L1/L2/L3/IR C++ on PEGTL); being extended 10/7 with drip publisher

~/dev/cc is the clone of public jkong7/CC- (CS 322 compilers: L1, L2, L3, IR in C++ on PEGTL 3.2.7, Winter 2026). On 2026-10-07 Jonny asked to make it more ambitious: build system, runtime, driver, tests, new front ends (LA, LB, C-minus), optimizations.

- Repo git identity set locally to jkong7 <jonathankong677@gmail.com> to match history. No Claude attribution.
- Code runs x86_64 Linux only: run via colima (vz + rosetta) + docker gcc:13 with the repo mounted (scratchpad /private/tmp is not mounted, use ~/dev/cc/build).
- Drip publisher: launchd com.jkong7.cc-publish, script .git/drip-publish.sh, queue .git/drip-queue (append SHAs), log ~/Library/Logs/cc-publish.log, 10-90 min apart, pushes SHA to main. It idles when the queue is drained and only exits once .git/drip-done exists. Never rewrite queued commits.

**Why:** He wants the compiler repo to look like serious, growing work on GitHub with commits only under his name ([[git-no-claude-attribution]], [[code-style-no-comments]]).

**How to apply:** Commit locally, append SHA to .git/drip-queue, touch .git/drip-done when the push series is finished. Never start a second publisher.
