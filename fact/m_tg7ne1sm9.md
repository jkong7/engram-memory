---
id: "m_tg7ne1sm9"
kind: "fact"
scope: "global"
title: "~/dev/chartside — ambient AI clinical scribe (Next 16), private jkong7/chartside; main fully pushed 2026-09-28; branch…"
tags: ["claude-memory","chartside-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.418Z"
updated: "2026-10-08T00:46:35.418Z"
source: "claude-code"
---

# ~/dev/chartside — ambient AI clinical scribe (Next 16), private jkong7/chartside; main fully pushed 2026-09-28; branch…

~/dev/chartside is a full-stack ambient clinical scribe, first built 2026-09-27 after deep research on the top 10 scribes (docs/research, docs/COMPETITIVE-ANALYSIS.md).

State as of 2026-09-27: 36 commits pushed to the private repo jkong7/chartside. Built by then: speech (Deepgram), revenue cycle, SMART on FHIR, orgs/RBAC/SSO, and a revenue lifecycle on official code sets.

**2026-09-28 session: feature-gap buildout.**
- Research lives in docs/research/feature-gaps-2026.md, a ranked list of 20 features.
- Added, all with unit and e2e tests:
  - co-signature and addenda
  - Inbox (patient messages, tasks)
  - dictation, voice commands, snippets, and vocabulary
  - note detail levels
  - letters/forms and a PDF writer
  - CMS eCQM quality measures
  - calculators and an evidence library
  - inpatient suite (census, progress notes, discharge, I-PASS, 99221–99239)
  - nursing flowsheets and a nurse role
  - public API /api/v1, webhooks, and OpenAPI
  - TOTP MFA, idle timeout, sessions, and SCIM
  - behavioral health pack
  - note revision history
  - schedule import and a scheduling queue
  - Note QA
  - outside records (C-CDA and PDF)
  - Chrome extension in extension/
  - telehealth dual-channel capture
  - later the same day: ED mode and track board, oncology pack (CTCAE, ECOG, lines of therapy), psychiatry add-on codes, GIRP, group therapy with per-member notes, colleague and external (email OTP) sharing
- Test counts as of the latest commit: 248 unit tests and 86 e2e tests (e2e also runs mock SendGrid+Phaxio on 3295 and mock MLLP on 3294; axe a11y scan).
- Publishing: on 2026-09-28 at about 23:40 CDT the user said to skip the interval pusher and push everything. The pusher was killed and main was pushed in full (main == origin/main at 3f0f4b2).
- Full handoff notes are in ~/dev/chartside/.context/HISTORY.md (local only).

**2026-09-28/29 overnight: "Chartside Line", the ghost interface (branch `interface/ghost`, 173 commits at 06:05 CDT 2026-09-29, pushed to origin 2026-09-30 at 090864b, not merged to main).**
- The bet: "Your scribe is a phone number." Call, set the phone down, hang up, and a PHI-free text links to the note. The web app becomes the back office.
- Docs: docs/INTERFACE-PLAN.md (plan and status), docs/research/interface-market.md plus 7 `_raw-*.md` reports, interface-feasibility.md.
- Report artifact: https://claude.ai/artifact/7WHRHN9ov4zedMqNjhhDpa
- Doors:
  - phone line: Twilio Media Streams to `server.ts`, a custom tsx server with a WebSocket upgrade; the telephony code is in src/lib/server/telephony/*
  - browser phone /go/phone (autopilot demo)
  - text the line (/api/sms/incoming, cron nudges and morning brief)
  - one-tap /go
  - Chrome extension recording
  - iPhone Shortcut
  - Android share target
  - the Stack /go/stack
  - Ask
  - Web Push
  - /line landing with video, pocket card /line/card
  - Admin → Line
- Built with a second session, dev-dc. It went "waiting" on a permission prompt around 01:00 CDT and stayed stuck.
- Final run at 06:05 CDT 2026-09-29: 368 unit and 154 e2e, all green, tsc clean. User-facing "stack" wording is now "To review" (the SMS keyword "stack" still works). `scripts/eval-line.mjs` runs 8 live calls against real Deepgram and Claude; they passed after each round of fixes.
- Run e2e only via `scripts/e2e-locked.sh`.
- The e2e server runs `NODE_ENV=production npx tsx server.ts` against data/e2e.
- Local live testing used data-live/ on port 3150.
- The auto-mode classifier BLOCKED IAM grants and a cloudflared tunnel, so nothing is hosted.
- Deploy is ready for Jonathan:
  - Run deploy/gcp-grant.sh, then gcp-deploy.sh, then gcp-scheduler.sh.
  - Project persona-onboarding-jk, service chartside, SA chartside-run.
  - Secrets already created: CHARTSIDE_SECRET, VAPID, CRON.
  - One stray grant went through: the default compute SA can read CHARTSIDE_SECRET, and gcp-grant.sh removes it.
- There is no Twilio number yet. Admin → Line can connect one.
- Five independent reviews were run, all findings fixed:
  - 15 findings in the phone code
  - 12 in newer code
  - 10 in PIN-by-phone and idempotency
  - 7 cross-cutting security issues, including a guest-merge account takeover and WebSocket exhaustion
  - 8 regressions
- A layman usability walk-through found 15 friction points; the high-impact ones were fixed.
- Keypad on the line:
  - 2 record, 3 Chartside asks the patient, 9 Spanish, 0 decline
  - 4 pause, 5 end, 1 ready
  - 8 next patient (same call), 7 text the patient after signing
  - 6 set a PIN (confirmed on a texted link by typing it again)
  - * skips the PIN, # finishes it

- **Licensed data:** NCCI/MUE/LCD contain AMA CPT content. The operator runs `npm run codesets:licensed -- --accept-cms-ama-license`. Never accept that license yourself.
- **Local Postgres for tests:** 127.0.0.1:5499, user chartside, database chartside_test.

**Why:** portfolio project with natural-looking history; the user keeps asking to push further toward a real scribe startup.

**How to apply:**
- Commit per component. No comments in code. No Claude trailers.
- Push only when the user asks.
- Claude is optional (ANTHROPIC_API_KEY); the offline engine is the default.
- .env.example is deny-listed, so document env vars in the README.

Related: [[git-no-claude-attribution]], [[code-style-no-comments]], [[vigil-repo]]

**Hosted 2026-09-30:** Jonathan ran deploy/gcp-grant.sh himself (the classifier blocks IAM grants for Claude; the first run hit SA propagation lag, so rerun). Claude then ran gcp-deploy.sh and gcp-scheduler.sh.
- Cloud Run service `chartside` in us-central1, deployed from `interface/ghost`. URL: https://chartside-792894733520.us-central1.run.app, alias https://chartside-3zllbxrjya-uc.a.run.app, which is the value set as CHARTSIDE_PUBLIC_URL.
- Litestream backs up to gs://persona-onboarding-jk-chartside-data/chartside/.
- Scheduler job chartside-nudges runs at "5 * * * *" America/Chicago.
- To redeploy: run `sh deploy/gcp-deploy.sh`. It needs no IAM changes.
- Still missing: a Twilio number (connect it in Admin → Line), and the licensed code sets, which only the operator can accept.

**2026-09-30 overnight "wave 2" (Jonathan asked to make it more viral, with faster onboarding and something novel; full permissions; test end to end and by hand).**
- Research: docs/research/_raw-{niches,messaging,new-interfaces,onboarding}-2.md.
- Five branches (pushed 2026-09-30):
  - interface/patient
  - interface/practice
  - interface/memo
  - interface/onboard
  - interface/wave2, which merges all four plus fixes
  - fix/memo-review, fix/patient-review and fix/practice-review, all merged into wave2
- Worktrees:
  - ~/dev/chartside-wt/{patient,memo,onboard,wave2}
  - practice lives at .claude/worktrees/agent-a1ca6b60729dcd98c
- Overview: docs/WAVE-2.md on wave2.
- Final wave2 run: 565 unit and 192 e2e, all green. Live checks with real Claude and Deepgram passed.
- After the build, 4 independent security reviews found 4 highs:
  - phone-account email hijack
  - OIDC login CSRF
  - password email-squatting
  - patient offer link claimable by anyone
- All findings were fixed and merged into wave2 (SECURITY-GHOST findings 30 to 51). The fix branches were fix/{memo,patient,practice}-review.
- Password sign-up now confirms the email with a code first when email is configured, and accounts track email_verified_at.
- The bets:
  - Bring your own scribe (patient records, clinician gets a draft)
  - Chartside Practice (AI standardized patient plus a graded scorecard)
  - Text it in (MMS memos) plus a WhatsApp lane for non-HIPAA orgs plus Barn Line for vets
  - Front-door onboarding (passwordless, NPI fill, style match, time zones)
- Gotchas:
  - Passwordless sign-up needs an email provider. Without one, /register falls back to a password.…
