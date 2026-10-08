---
id: "m_tg7p94k0k"
kind: "preference"
scope: "global"
title: "Never write code comments or docstrings; one commit per component in public repos"
tags: ["claude-memory","code-style-no-comments"]
importance: 8
trust: "agent"
status: "active"
created: "2026-10-08T00:46:35.504Z"
updated: "2026-10-08T00:46:35.504Z"
source: "claude-code"
---

# Never write code comments or docstrings; one commit per component in public repos

Never put comments or docstrings in code I write for the user ("NO COMMENTS EVER", 2026-09-21). Usage docs go in the README or argparse help instead. The only exception is metadata that tools parse to function, such as Raycast `# @raycast.*` headers, and it must be kept to the required lines.

For public repos, build history as separate commits per component (and push each), so the history "adds up" and reads well, rather than one big initial commit.

**Why:** the user's stated style preference, and they care how public GitHub history looks.
**How to apply:** strip comments before committing; plan commits component-by-component. Related: [[flow-kit-repo]]
