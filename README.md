[README.md](https://github.com/user-attachments/files/34257775/README.md)
# STRIDE v2.0 — Participant Interface

Use the existing **config.js** from your working v1.9 GitHub deployment. Do not replace it with a placeholder. Replace **index.html** only.

## Changes
- Prominent circular Stop button at top of Live; Start there too
- Friendlier labels for the movement display and walking consistency
- Summary tab with totals and an in-app steps chart; no CSV buttons in participant UI
- Profile tab with Supabase-authenticated display name (`auth.updateUser` user metadata), on-device light/dark preference, expandable voice coaching settings, account, sign out
- Preserves Supabase login, cloud save and session history, bilingual coaching and motion detection

## Notes
- No additional database SQL is needed. Display names are stored in Supabase Auth user metadata, not in `walking_sessions`.
- Theme persists on this device/browser only.
- The Summary aggregates up to the latest **100 sessions**, matching the existing query limit. It is not an all-time total for users with more than 100 sessions.
- Phone angle and side-to-side movement are device-based estimates, not posture measurements. The walking animation is illustrative.
- Browser testing on iPhone Safari is still required.
