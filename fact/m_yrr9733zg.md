---
id: "m_yrr9733zg"
kind: "fact"
scope: "global"
title: "~/dev/pushback, Pine (19pine.ai) rebuild, AI that phones companies to lower bills, cancel and get refunds; 29 local com…"
tags: ["claude-memory","pushback-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T03:15:31.723Z"
updated: "2026-10-08T03:45:36.707Z"
source: "claude-code"
---

# ~/dev/pushback, Pine (19pine.ai) rebuild, AI that phones companies to lower bills, cancel and get refunds; 29 local com…

~/dev/pushback is Pushback, built 2026-10-07 as the second consumer AI lane after [[cue-repo]]. Picked from a 10-startup SF scan (~/dev/reports "SF consumer AI shortlist 2026-10.md", teardown "Pine teardown 2026-10.md"). Pine won 24/25: agent that calls companies; its weaknesses are product ones (users did the work, re-asked info, surprise fees, black box).

Stack: Electron 44 + React 19 + node:sqlite + Anthropic TS SDK (claude-opus-5-5, low effort for live turns), ws, Twilio Media Streams + Deepgram nova-3/Aura-2 for real calls, cloudflared quick tunnel. No keys = rehearsal mode (scripted negotiator vs simulated menu/hold/retention rep). Secrets are {{placeholders}} filled locally, never sent to the model; limits enforced in code with approve/push-back pauses.

State 2026-10-07: 28 tests pass (sim calls, fake Twilio + fake Deepgram line, fake Anthropic API full call), typecheck and build clean, app verified hidden via offscreen capture (PUSHBACK_SNAPSHOT_DIR, PUSHBACK_AUTOCALL, PUSHBACK_SEED). Never tested against a real Twilio/Deepgram/Anthropic account or a real company.

Publishing: 29 per-component commits, Jonathan Kong only. Jonny (relayed by dev-3a) asked for a PUBLIC repo; jkong7/pushback was created public and empty with origin set. The classifier first blocked the publisher; Jonny then approved publishing publicly. Publisher at .git/publish/publisher.sh (29-commit queue, state file, stop file), plist ~/Library/LaunchAgents/com.jkong7.pushback-publisher.plist, log ~/Library/Logs/pushback-publisher.log. Dry-run push from env -i succeeded. Jonny bootstraps the plist himself.

**Why:** Jonny wants consumer, attention-native AI products; see [[cue-repo]] for the same loop.
**How to apply:** if asked to publish, model the publisher on ~/dev/cue/.git/publish/publisher.sh with label com.jkong7.pushback-publisher, braced "${sha}:refs/heads/main" refspec, and have Jonny run launchctl bootstrap himself.
