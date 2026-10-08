---
id: "m_tg7xs1ml2"
kind: "fact"
scope: "global"
title: "Where the job search automation lives and the decisions behind it (routines, ledger, packet spec, ATS creds)"
tags: ["claude-memory","jobsearch-pipeline"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.793Z"
updated: "2026-10-08T00:46:35.793Z"
source: "claude-code"
---

# Where the job search automation lives and the decisions behind it (routines, ledger, packet spec, ATS creds)

Job search repo: ~/dev/jobsearch (GitHub jkong7/jobsearch, private). Ground truth: PROFILE.md, STORIES.md, WRITING_RULES.md, PACKET_TEMPLATE.md. Shared role rules in rules.py.

Decisions (2026-09-21):
- One packet quality for every role, lean (research budget 4 fetches); 40 roles/day queued from daily + backlog boards.
- Internship first per company; new-grad posting noted in ledger (also_new_grad). He is enrolled in the concurrent BS/MS, so Master's internships are in scope.
- All US locations in scope; SF/NYC/Chicago priority; Chicago favored for off-season (he's in Evanston Winter/Spring 2027).
- Cover letters whenever a field exists. Fill forms in Chrome, stop before Submit.
- Voice: VOICE.md (built 2026-09-21 from his Drive writing and emails). Real behavioral stories live in STORIES.md; never invent new ones.
- Never mention Abridge return offers/extensions in any application; treat his Abridge feedback letter as private.
- Handshake (northwestern.joinhandshake.com) works only through his logged-in Chrome, not CI.
- ATS accounts: Claude never creates accounts or types passwords (safety rule). Jonathan signs in once per portal; shared password in Keychain via ats_creds.py for his use.

Routines: "Application Packets" trig_01JFmgbGnWNfwLHiYfukSaB8 (Opus 5, 10/run x4/day, writes ledger or state/ledger_outbox.json); "Daily Job Drops" trig_011PK7zL1yoCFEBobCwkAVqQ publishes boards. Ledger: https://claude.ai/artifact/9c6SB1fRo6xMSpaNrVFa6V collection `applications`.

Form filling (2026-09-21): tools/gh_plan.js (Greenhouse; stored in localStorage '__plan' per origin, EU boards separate), tools/ashby_plan.js + ashjs.py (Ashby, '__aplan'), Lever planner in '__lplan'. React-select needs real coordinate clicks; school/location lookups are slow. He submits and closes each tab himself, often closing the whole tab group, so open a new tab per role and recreate the group when it vanishes.

**Why:** user wants near-full automation at volume without bloated research.
**How to apply:** change the pipeline through these files, not ad hoc; flush ledger_outbox before apply sessions.
- Form-fill gotchas (2026-09-22): background Chrome tabs render stale frames, so take a tiny screenshot before each coordinate click; react-select needs real clicks; comboboxes/location work best with type, then Enter; localhost fetch is blocked in pages. Full playbook: ~/dev/jobsearch/HANDOFF_65.md
