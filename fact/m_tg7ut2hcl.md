---
id: "m_tg7ut2hcl"
kind: "fact"
scope: "global"
title: "~/dev/honey, Candy AI interface clone (companion chat), local only, built 2026-10-03"
tags: ["claude-memory","honey-repo"]
importance: 6
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.699Z"
updated: "2026-10-08T00:46:35.699Z"
source: "claude-code"
---

# ~/dev/honey, Candy AI interface clone (companion chat), local only, built 2026-10-03

~/dev/honey is a Next.js 16 clone of Candy AI's interface, branded honey.ai, built 2026-10-03. Local git only, no remote, not deployed.

Real: Claude chat streaming via /api/chat (needs ANTHROPIC_API_KEY in .env.local, otherwise demo replies). Mocked: auth, premium, tokens, checkout (localStorage). Images: Gemini 2.5 Flash Image via Vertex on GCP project persona-onboarding-jk (aiplatform API enabled 2026-10-03 with Jonny's OK, ~$0.04/image, billed to that project). Portraits cached in data/images (24 seeded ones committed); scene photos use the portrait as reference for face consistency. DiceBear is the fallback.

**Why:** Jonny wants to build consumer AI companion/escapism products ([[building]] in the brain vault). This is the UX base for that.
**How to apply:** Kept PG-13 on purpose (Claude can't do explicit, and payments/app stores block adult). If he wants the NSFW version, that changes the model, payment processor and hosting choices.
