---
id: "m_tg82m1ojc"
kind: "preference"
scope: "global"
title: "Never apply to a company Jonathan has already applied to, even for a different role"
tags: ["claude-memory","one-application-per-company"]
importance: 8
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.967Z"
updated: "2026-10-08T00:46:35.967Z"
source: "claude-code"
---

# Never apply to a company Jonathan has already applied to, even for a different role

**One application per company, ever.** If Jonathan has already applied anywhere at a company, do not queue, pack, or fill a second role there, even a different team, track, or location.

**Why:** He said it directly and in caps: "IF I VE ALREADY APPLIED TO THE COMPANY DONT DO IT AGAIN EVEN IF ANOTHER ROLE." A second application at the same company looks like spray-and-pray to a recruiter, and it can put two different graduation dates in front of one employer, which the repo already bans separately. This is stricter than the older "never send one company both tracks" rule in `~/dev/jobsearch/CLAUDE.md`, and it supersedes it.

**How to apply:** before sourcing or packeting, build a company blocklist from `~/dev/jobsearch/state/queue.json` covering every entry with status `done`, `deferred`, `pending` or `blocked`, plus companies that only exist in the ledger artifact or arrived through inbound outreach (Ab Initio came in by LinkedIn InMail, never through a board). Match on a normalized company name, not the queue key, because board rows spell the same company differently ("WhatNot" vs "Whatnot", "WeRide.ai" vs "WeRide", "Superhuman" vs "Superhuman Platform Inc"). When a role is killed by this rule, set the queue status to `superseded` with a note naming the earlier application. Expect this to cut a batch hard: on 2026-09-23 it killed 5 of 10 picks (Persona, Superhuman, SingleStore, Whatnot, DoorDash).

**Check the ledger itself right before filling any form**, not just `state/company_blocklist.json`: the blocklist lags behind submissions. On 2026-09-28 I re-filled Divergent and Instead because the blocklist missed them while the ledger already showed them Applied that day under a slightly different company name. Query the ledger `applications` collection for any row whose company matches (normalized, prefix-tolerant) with a status other than To apply or Ready to submit, and treat a Jonathan-marked Skipped (e.g. Varda) as a no too. After a history sync, refresh the blocklist from the ledger (all Applied, Rejected, Online assessment, Interviewing, Withdrawn, Outreach sent, Bounced rows plus Jonathan's skips).

Related: [[jobsearch-pipeline]], [[browser-one-tab-per-application]]
