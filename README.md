[Uploading README.md…]()
# STRIDE v2.4 — Fashion Technology Research Upgrade

Built on STRIDE v2.3; do not replace your working `config.js`.

## Install
1. Back up the working `index.html`.
2. If not already completed, run the **v2.3** migration to add avg_rhythm_cv, avg_tilt_deg, avg_side_signal, coaching_alerts.
3. Run **migration.sql** in Supabase SQL Editor (Database mode); it only adds JSONB columns. It does not drop records or RLS.
4. Replace **index.html** in the GitHub Pages repository root; leave `config.js` unchanged.
5. Verify sign-in, Live start/stop, phone sensor permission, audio, saved session, History, Analysis and simulated pressure controls.

## New features
- Six mobile-friendly tabs: Home, Live, Analysis, History, Sneaker, Profile.
- Live and saved-session cadence / rhythm graphs from measured estimates only.
- Visual history of steps, cadence, rhythm variability and duration; CSV remains available.
- User-defined step and duration goals, rhythm threshold, and coaching frequency; settings stored in Supabase Auth user metadata.
- Coaching event timestamps and cadence timeline stored as JSONB in each user's sessions.
- A clearly labeled *Simulation Mode* pressure heatmap (not real foot-pressure data).
- Premium vector sneaker concept with interactive proposed component list.
- No new APIs, paid services or external frameworks beyond existing Supabase JS dependency.

## What is experimental vs simulated vs future
- **Live experimental measurements:** browser accelerometer/orientation, detected step intervals, cadence and approximate phone motion.
- **Simulated ONLY:** left/right foot pressure heatmaps in the Analysis tab. Never collected or uploaded as sensor observations.
- **Future only:** in-shoe pressure matrix, shoe-based accelerometer, gyroscope, BLE, battery, orthopedic assessment.
- **Current coaching:** rules and thresholds, not a machine-learned model.

## Research limitations
- Phone orientation is not spinal or pelvic angle. Side-to-side motion is not validated gait symmetry.
- Step interval CV is exploratory and dependent on step detection and sensor placement.
- Historical new fields from old sessions remain missing, never invented.
- Browser background motion sensing and speech may stop when iPhone is locked.
- Coaching history records triggered events, not guaranteed playback.
- The app is not a medical device or a clinical gait assessment.
- Existing summary API uses up to 100 recent sessions.
