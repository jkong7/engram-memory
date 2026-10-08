---
id: "m_wel0ga1uq"
kind: "procedure"
scope: "project:~/dev/chartside"
title: "Rolling back Chartside Cloud Run to the previous revision"
tags: ["deploy","rollback","gcp"]
importance: 6
trust: "extracted"
status: "active"
created: "2026-10-08T02:09:18.184Z"
updated: "2026-10-08T02:09:18.184Z"
source: "claude-code claude-code:f89b8479-212c-4c74-ba0d-2de8115ddb0e"
---

# Rolling back Chartside Cloud Run to the previous revision

Chartside's previous Cloud Run revision chartside-00002-h4c was kept as the rollback target when wave2 went live on 2026-09-30. To roll back, run: gcloud run services update-traffic chartside --to-revisions chartside-00002-h4c=100 --region us-central1 --project persona-onboarding-jk. Confirm the revision still exists before relying on it, because later deploys may have replaced it.
