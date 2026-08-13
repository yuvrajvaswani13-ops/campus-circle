[README.md](https://github.com/user-attachments/files/31040408/README.md)# Campus Circle — Student-run Community

A polished independent student community website with:
- public project/about pages
- student articles, events, clubs and creative-work sections
- private member-area entry point
- invitation-code based membership
- email/password authentication through Supabase
- pending/approved membership states
- moderation-first posts/comments
- clear independent/non-endorsed wording

## Important

This is **not an official school website**. Keep the disclaimer visible and do not use the school's logo, official branding, private directory, or official announcements without permission.

Because students may be minors, start with moderated posts/comments and **do not enable direct/private messaging until you have an appropriate safety and moderation process**.

## Publish

1. Create a free Supabase project.
2. In Supabase, open SQL Editor and run `supabase/schema.sql`.
3. Configure email verification in Supabase Auth.
4. Put the Supabase project URL and public `anon` key into `config.js`.
5. Upload the whole folder to a GitHub repository.
6. Enable GitHub Pages for the repository's `main` branch and `/ (root)`.
7. Your public website will be available at the GitHub Pages address shown by GitHub.

## Membership flow

1. Admin creates invitation codes in Supabase by storing SHA-256 hashes, not raw codes.
2. Student enters an invite code and creates an account.
3. Student verifies their email.
4. The account remains `pending` until an administrator approves it.
5. Only approved members can access community content.

## Admin safety

Keep administrator accounts limited to the student project team plus a trusted adult if appropriate. Never put a Supabase `service_role` key in `config.js` or in browser code.

Before launch, agree on:
- what content is allowed
- who moderates reports
- how quickly reports are reviewed
- what happens after repeated rule violations
- what personal information students must not post
- how students can request deletion of their content/account

## Custom domain

After GitHub Pages works, you can optionally buy a domain and connect it through GitHub Pages. Choose a name that does not imply official school ownership.

