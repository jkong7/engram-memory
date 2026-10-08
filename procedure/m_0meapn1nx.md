---
id: "m_0meapn1nx"
kind: "procedure"
scope: "global"
title: "Split a commit-heavy repo into per-component commits without touching the working tree"
tags: ["git","procedure"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T04:07:21.197Z"
updated: "2026-10-08T04:07:21.197Z"
source: "claude-code claude-code:1d834580-b9c9-47d6-895d-32f97b724493"
---

# Split a commit-heavy repo into per-component commits without touching the working tree

1. Back up the current branch tip to a local backup branch and do not push it. 2. Build new commits with a temporary index (GIT_INDEX_FILE=<tmp>), using git read-tree, update-index and write-tree per component, then git commit-tree with the original author. 3. Point the branch at the final commit with update-ref. 4. Verify the final tree matches the original tree (git diff --quiet against the old HEAD). 5. Scan tracked files for secrets and check for attribution trailers before any push. The working folder stays unchanged, so a running server is not disturbed.
