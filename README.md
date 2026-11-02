[README.md](https://github.com/user-attachments/files/34257034/README.md)
# STRIDE v1.9 — Real Accounts with Supabase

Replaces participant profiles with Supabase email/password authentication and user-owned cloud session history. Existing gait visualization and audio logic retained.

## First-time setup
1. Create a project at https://supabase.com/dashboard.
2. In **SQL Editor**, paste `setup.sql`, then click **Run**. This sets up the `walking_sessions` table and per-user Row Level Security policies.
3. In **Project Settings → API Keys** (or **Connect** depending on dashboard version), copy **Project URL** and **publishable key** (`sb_publishable_...`) or legacy `anon` key. **Never use the secret/service_role key**.
4. Edit `config.js` and replace both placeholders with the two public values.
5. In **Authentication → URL Configuration**, set **Site URL** to the full GitHub Pages app URL, e.g. `https://YOURUSERNAME.github.io/stride-research/`. Add exactly the same URL to **Redirect URLs**. Keep the trailing slash.
6. In **Authentication → Providers → Email**, ensure email/password authentication is enabled. Keep email confirmation enabled. Supabase's default email delivery may have rate limits/recipient restrictions: test with your own email and configure a trusted SMTP provider before inviting a large group.
7. Upload `index.html`, `config.js`, and `README.md` to the root of your GitHub repository. You do **not** upload `setup.sql` unless you want to keep documentation. Commit and wait for Pages to deploy.
8. Open the deployed URL on iPhone Safari. Create an account. Confirm the email, sign in, start and stop a session, and check Sessions. Sign in on another browser to verify cloud history.

## Security and research privacy
- The Supabase publishable/anon key is **public**; this is normal. Data isolation is enforced in the database with RLS policies. Do not publish a secret/service_role key.
- Only signed-in users can select or insert their own sessions. Signed-out users cannot access session records.
- Store only non-diagnostic step counts, duration, cadence and rhythm CV. No raw motion data or personal health claims are uploaded.
- Email addresses are personal information. Obtain informed consent from research participants, provide deletion/retention instructions and obtain appropriate institutional review before recruitment. Supabase Auth users cannot self-delete accounts using only browser keys; an administrator must manage deletion or implement a secured backend deletion flow.
- Local participant-profile data from v1.8 is **not migrated** and the new version no longer uses it. Participants can delete old site storage after exporting their prior local records.
- If cloud insert fails, check `Sessions` for a clear status; the Motion CSV export remains available as a fallback.
- Disable public sign-up when recruitment is complete if you want to prevent uninvited users.

## Troubleshooting
- `Invalid API key`: check `config.js` values. Use a public publishable/anon key.
- `Email not confirmed`: click the confirmation link first, then sign in.
- Confirmation sends to the wrong website: correct Authentication URL Configuration.
- `permission denied` or `RLS`: run `setup.sql` and check the user is signed in.
- Supabase SDK did not load: check internet/CDN connectivity; GitHub Pages requires an internet connection.
