---
id: "m_tg83j1xhi"
kind: "fact"
scope: "global"
title: "Persona (yourpersona.com) take-home at ~/dev/persona-onboarding; conversational onboarding by text + voice call; stack,…"
tags: ["claude-memory","persona-onboarding-takehome"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.999Z"
updated: "2026-10-08T00:46:35.999Z"
source: "claude-code"
---

# Persona (yourpersona.com) take-home at ~/dev/persona-onboarding; conversational onboarding by text + voice call; stack,…

Take-home for Persona (Iris Assistant, Inc., yourpersona.com), assigned via Google Doc "PERSONA TAKE HOME" (owner julia.li.media@gmail.com, shared 2026-09-26). Build an onboarding that collects agent name (text), user name, Gmail and a help topic (attempted over a call), survives hangups, does not feel like a form, allows early "graduation". Web simulator with voice is enough.

**Location:** `~/dev/persona-onboarding`. Git repo with remote private `jkong7/persona-onboarding`. Fully synced on 2026-09-29 at his request (15 component commits, head 22d3953, no AI attribution). `.env`, `data/` and the voice cache are ignored. Push only when Jonathan asks.

**Decisions Jonathan made (2026-09-27):**
- Voice vendor: Deepgram Voice Agent (chose it over ElevenLabs on cost). Claude runs on our server as Deepgram's custom LLM endpoint.
- Models he chose: Claude Opus 5.5 for the text thread, Claude Sonnet 5 on calls. Final call model is Haiku 4.5 (decided 2026-09-28 on data): Sonnet 5 took 1.5 to 3 s to start answering on a weekday afternoon (reply gaps of 2.8 s, spikes of 5 to 6 s) versus a steady 1.6 s on Haiku. Sonnet is one setting away (`AGENT_VOICE_MODEL`). Local `.env` and the hosted service both say Haiku.
- Interface must stay light: a phone-style thread and call screen, not an app. Reviewer panel is hidden behind a "Reviewer tools" toggle.
- Quality bar: everything the doc asks for, no corners cut. He asked me to drive end-to-end testing myself and iterate.
- Funded Anthropic with $5 then $20 more. The credit ran out on 2026-09-28 around 20:30 UTC; Jonathan topped it up again by 2026-09-29. Suggest auto-reload and a spend limit, and state the cost before any model run.

**Why:** the reviewer said they will stress test it, naming call hangups.

**How to apply:**
- Run with `pnpm dev:voice` from the repo root (opens a cloudflared quick tunnel, serves the built page on :8787). The tunnel can take 1 to 2 minutes; wait for "tunnel: ready" before calling. Rebuild the page with `pnpm build:client`.
- Tests: `pnpm test` (server), `pnpm -C client test`. Simulated text suite: `pnpm eval --only <ids>` (about $0.15 to $0.20 per scenario). Live calls with synthesized speech: `pnpm eval:voice --only <ids>` under `caffeinate -i`, 16 scripts, about 25 minutes for all.
- Keys live in `.env` (Anthropic, Deepgram, CALL_TOKEN_SECRET). Never print them.
- Results on 2026-09-28: 370 server tests and 87 client tests pass; 16 of 16 live calls pass on the hosted copy with Haiku (median 1.6 s reply gap); simulated text suite 12 of 20 on the last full run. The final deployed revision is `persona-onboarding-00009-pjl`. Its last six fixes (sample-inbox rule in any language, no pushing the real account after choosing sample, name prompt in text, word budget reset after a lookup, no logging of asks for known items, outage wording) are unit-tested only. Once credit is back, run `pnpm eval:voice --base <host>` (16 calls) and `pnpm eval --only task_first,returns_hours_later,rambler,gmail_popup_closed,silence_on_call,typed_name_during_call,changes_mind,another_language` (about $0.70).
- Never send `thinking: disabled` for the call model: it made some requests start 2.5 s late. The call model leaves the thinking setting out (`AGENT_VOICE_THINKING` unset).
- Findings that mattered (2026-09-28): strict tool schemas slowed call replies by up to 1 s, so calls send tools without `strict`; Deepgram only speaks at sentence ends, so the speech filter sends whole sentences with a trailing space; names are confirmed implicitly (greet by name, server settles it on the next turn) instead of a read-back question; Opus 5.5 sometimes wraps text in tags or leaks a `<reasoning>` block, which a filter removes; Opus 5.5 text replies take 5 to 10 s.
- Hosted on Google Cloud Run since 2026-09-28: project `persona-onboarding-jk`, service `persona-onboarding` in us-central1, https://persona-onboarding-792894733520.us-central1.run.app. One always-on instance (min 1, max 1, CPU always allocated). SQLite is backed up by Litestream to the private bucket `persona-onboarding-jk-data` and restored on start. Keys are in Secret Manager; Jonathan runs `deploy/gcp-secrets.sh persona-onboarding-jk` himself. Deploy with `deploy/gcp-deploy.sh`. Live tests: `pnpm eval:voice --base <that address>`. Billing is a free trial ($300, 90 days from 2026-09-28, card on file for verification); never upgrade it to a paid account. Fly.io was tried first and removed at his request (its trial allows only 2 hours of runtime).
- On 2026-09-28 Jonathan gave standing permission to deploy to the host after each change without asking first. Run tests before deploying, avoid deploying mid-call, and tell him what went live. This does not cover pushing to GitHub: he asked to keep it off at first, then asked for a full sync on 2026-09-29, so ask before each later push.
- Gmail OAuth is live since 2026-09-28: Google Auth Platform app "Persona onboarding demo" in project `persona-onboarding-jk`, External, Testing, scope gmail.readonly, web client "Persona onboarding web" with origins for the run.app address and http://localhost:8787. Client id and secret are in `.env` and Secret Manager (Google shows the secret only once). Test users as of 2026-09-29: jonathankong677@gmail.com, julia.li.media@gmail.com and amandadiao16@gmail.com (Google showed an "ineligible account" notice for the last one on a repeated save, though it is on the saved list; recheck the spelling if she cannot connect). Real connection verified end to end on the hosted copy.
- Submitted to Julia Li on 2026-09-28 (ledger row persona-band-yourpersona-julia-li-intro now Applied, check in by 2026-10-01). Reviewers may test the hosted copy any time, so keep it up.
- Still open: Safari, Firefox and phones untested; disconnect untested against Google; set a spend limit in the Claude Console.
- Related rules: [[code-style-no-comments]], [[git-no-claude-attribution]], [[no-em-dashes]].

2026-10-04: briefly set min-instances 0, then restored to 1 (revision persona-onboarding-00012-f4n) because reviewers may test any time and billing is free-trial credit. Keep it always-on until Persona replies; only then scale to zero or delete. Check the memory before suggesting cost cuts here.
