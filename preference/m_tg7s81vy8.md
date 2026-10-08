---
id: "m_tg7s81vy8"
kind: "preference"
scope: "global"
title: "SUPERSEDED 2026-10-04 by write-in-jonny-voice: old answer bank is history; v6 is a reference voice, not a paste bank"
tags: ["claude-memory","frq-answer-bank"]
importance: 8
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.593Z"
updated: "2026-10-08T00:46:35.593Z"
sensitive: true
source: "claude-code"
---

# SUPERSEDED 2026-10-04 by write-in-jonny-voice: old answer bank is history; v6 is a reference voice, not a paste bank

**SUPERSEDED 2026-10-04:** Jonny's standing rules in `~/brain/me/voice.md` replace this. v6 (`~/dev/jobsearch/writing/essay-drafts-v6.txt`) is a reference voice, not a static answer bank, and cached answers are leads to recheck, never automatic pastes. Everything below is history. See [[write-in-jonny-voice]].

For free-response questions on applications, paste one of Jonathan's answers below **word for word** (keep his wording and typos). Do not write new FRQ answers. If none fits, leave the field for him.

**Why:** He asked on 2026-09-24: "use one of these answers if you can word for word in your frq replies, dont invent your own answers".

**Update 2026-09-28:** Jonathan relaxed this: "you DONT have to use the batch answer if it doesnt fit, for example 'why x company' ones dont match any well, make them good and personable and human sounding and not ai". So when a bank answer doesn't fit (especially company-specific why-us), write a short, specific, casual answer in his voice (see VOICE.md: plain words, a little enthusiasm, no em dashes, no polished AI cadence). Still use B1/B2/C/E/F word for word for project and experience questions.

**How to apply:** Why-us or why-role questions use A3 (generic). Project, proudest-work or technical-challenge questions use B1 or B2. "Two projects" questions use C. "Something not on resume" uses D. AI tools use E. Full-stack feature uses F. A1 and A2 are Rebar-specific; use them only for Rebar or a deterministic-harness question. Cover letters are separate (see WRITING_RULES). Related: [[one-application-per-company]].

A1 (harnessing): The main thesis is: extract as much deterministic verifiable actions as possible and provide them as rule-based pieces of code helpers for efficient token usage. When exhausted all rule-based harnessing possibilities, move to tweaking your system prompt. And that is an example of  good harnessing.

A2 (Rebar why): I was watching this talk, “Why Software Factories Fail”, and it put words to something I felt while working with AI coding tools at Abridge: writing code faster only helps if you still understand and care about what you ship. That’s part of what excites me about Rebar. You’re embracing AI tools while taking the craft seriously, and the product has real engineering challenges that estimators feel every day.

A3 (generic why): I'm super motivated by the simple motto of making things correct! I was watching this talk, “Why Software Factories Fail”, and it put words to something I felt while working with AI coding tools at Abridge: writing code faster only helps if you still understand and care about what you ship. I've recently experimented with various degrees of automation/human workflows. The one I found worked the best focused my attention on two areas: planning/architecture + FOCUSED review (ie maybe not the code line by line, but key evaluation metrics and end to end behavior). In all, there is still a long ways to go before being able to make frontier models deterministic WITH your full business domain context but I believe startups/companies with the best deterministic workflows will come out on top.

B1 (proudest project): I'm proudest of Query Engine, which I built this summer as a full-stack engineering intern at Abridge. The problem was that AI-drafted clinical notes sometimes left out details the bill depends on, so coders had to send clinicians follow-up questions days later when nobody remembered the visit. Query Engine catches those gaps before the note is signed. I built it as a Temporal pipeline that runs AFTER initial note gen. It fetches the patient's EHR history, builds context for each DX in the Assessment & Plan entry, detects what's missing with the LLM, and writes a one-click multiple-choice question into the note UI. As for the impact, I rolled it out on GKE starting with one alpha cohort and watching custom Datadog dashboards, then slowly (over 2 weeks) expanded it to all of our clinician partners. It reached 73% clinician acceptance and ~150 fewer billing follow-ups a month and is in production today!

B2 (project, hardest part): At Abridge, AI-drafted clinical notes sometimes left out details the bill depends on, so coders had to send clinicians follow-up questions days later when nobody remembered the visit. I built Query Engine to catch those gaps before signing. It's a Temporal pipeline that runs after note generation: it fetches the patient's EHR history, builds context for each DX Assessment & Plan entry, detects what's missing with the LLM, and writes a one-click multiple-choice question into the note UI. The absolute hardest part was that every false alarm costs clinician trust, so I built a LangSmith eval harness with cases that have known gaps and cases with none, and every prompt change had to pass it before shipping. Eventually, I rolled it out on GKE starting with a single kaiser alpha cohort. And after three weeks, it was live to all of our partners! (It's internal to Abridge, so I can't link to it)

C (two projects): 1. Query Engine at Abridge: I built a Temporal RAG pipeline that runs after an AI-drafted clinical note is generated, reads it against the patient's EHR history, and flags documentation gaps before the clinician signs. Since LLM output isn't deterministic, I built a LangSmith eval harness with cases that have known gaps and cases with none, and every prompt change had to pass it. I deployed it on GKE behind LaunchDarkly flags and Argo Rollouts and today it is live to all of our clinician partners!

2. Diagnosis Search performance at Abridge. Clinicians said search was slow, so I started with Amplitude data and found two causes: Postgres prefix matching missed abbreviations (e.g. "HTN" didn't find hypertension), and common diagnoses ranked below rare ones. I combined IMO's semantic-ranking API with a per-org popularity signal (a Postgres table incremented on each commit to the EHR and joined at read time). Eventually, median lookup time dropped from 19s to 7s across 300K monthly searches for our 12 largest partners!

D (something not on resume): My favorite thing ever was starting a local pickleball league in my hometown

E (AI coding tools): Every day, mostly Claude Code. At Abridge nearly everyone worked with coding agents so honestly, the hardest part was deciding what NOT to use AI with. I ended up pinpointing the most attention-needing parts like architecture and tradeoffs, testing and end-to-end verification, and deciding which PRs to hand to an agent and which ones to stay in the loop on. 

As an example of my AI efforts, I built Claude Code agentic workflows for the team's biggest bottleneck, end-to-end QA of recording-to-note flows. Tools would spin up preview environments and replay synthetic patient visits and then skill files describe dhow to check the resulting note. This also made it so that the team's QA knowledge was distributed and synced. Engineers could run it on their own PRs!

F (full-stack feature): "Level of Service" at Abridge. Every visit is billed at a level set by how complex the medical decisions were, and medical coders assigned it by hand after the visit. We wanted a way to make this more automated and own the computation at our own level. I owned this feature from the intitial design I shared at stand up to the backend logic, the UI in the note, tests, rollout and monitoring. The initial quick approach was to have the LLM read the note and output the level, but billing has to give the same answer every time and show why. So my solution was to have the LLM supplies structured diagnosis data, and a deterministic TypeScript layer applies the billing rules. I encoded the guideline tables as typed rules with a unit test for each, plus a regression set of encounters leveled by coding specialists.…
