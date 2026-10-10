---
id: "m_zrte1fb01"
kind: "procedure"
scope: "project:~/dev/burner"
title: "Connecting Burner to Supabase and Gmail SMTP"
tags: ["supabase","email","gotchas"]
importance: 6
trust: "extracted"
status: "active"
created: "2026-10-10T22:54:39.094Z"
updated: "2026-10-10T22:54:39.094Z"
source: "claude-code claude-code:e93bf3b6-8bdc-49bd-822e-3c5c15b165e2"
---

# Connecting Burner to Supabase and Gmail SMTP

1. Create the Supabase project with the Data API off and automatic RLS on. 2. Use the session pooler on port 5432 in DATABASE_URL; the transaction pooler on 6543 rejected the new password. 3. Set the Site URL to localhost:3007 and add /auth/callback to redirect URLs. 4. For sign-in emails, set Supabase's SMTP to smtp.gmail.com port 465 with a Gmail app password, and raise the email limit from 2 to 30 an hour. 5. Keep Google and Apple buttons hidden until those providers are configured.
