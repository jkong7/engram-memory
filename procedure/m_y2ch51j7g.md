---
id: "m_y2ch51j7g"
kind: "procedure"
scope: "global"
title: "Zsh git refspec gotcha"
tags: ["git","zsh","gotcha"]
importance: 4
trust: "extracted"
status: "active"
created: "2026-10-08T02:55:46.509Z"
updated: "2026-10-08T02:55:46.509Z"
source: "claude-code claude-code:fffe3ce6-4669-4775-b8fb-d001e344a014"
---

# Zsh git refspec gotcha

In zsh, a refspec like "$sha:refs/heads/main" is misparsed because the :r history modifier strips the ':r' from 'refs', so git push fails. Brace the variable ("${sha}:refs/heads/main") in any push script, and dry-run the push before starting a publisher.
