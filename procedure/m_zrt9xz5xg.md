---
id: "m_zrt9xz5xg"
kind: "procedure"
scope: "project:~/dev/burner"
title: "Deploying Burner to Cloud Run"
tags: ["deploy","gcp","gotchas"]
importance: 6
trust: "extracted"
status: "active"
created: "2026-10-10T22:54:38.916Z"
updated: "2026-10-10T22:54:38.916Z"
source: "claude-code claude-code:e93bf3b6-8bdc-49bd-822e-3c5c15b165e2"
---

# Deploying Burner to Cloud Run

1. Store DATABASE_URL from .env.local in Secret Manager as burner-database-url in project persona-onboarding-jk, then grant the service access. 2. Set Next's outputFileTracingExcludes to drop data folders, scripts and test builds, or the standalone output reaches about 1.5 GB. Narrow the .next-* exclude to the specific dev folders, since it also catches test builds. 3. Build with Cloud Build and deploy to Cloud Run with max instances 1. 4. Add a Cloud Scheduler job every 5 minutes that calls the background tick with the cron secret. 5. Add the live URL to Supabase's Site URL and redirect settings.
