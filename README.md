[README.md](https://github.com/user-attachments/files/34127447/README.md)
# STRIDE v1.4 — Bottom Tab Navigation

## Changes
- Minimal home screen: centered STRIDE logo and Start Walking button
- Fixed bottom navigation inspired by the provided reference: Home, Live, Coach, Sessions
- Each navigation tab shows a separate screen, rather than exposing other sections by scrolling
- Start Walking opens Live and requests motion-sensor access on a direct tap
- Preserves step estimates, live rhythm feedback, English/Korean voice choice and rate, simulations, and CSV exports

## Deploy
Replace `index.html` in your existing GitHub Pages repository and commit. Updating README.md is optional. Refresh iPhone Safari after deployment.

## Testing
1. On Home, swiping should not reveal Live/Coach/Sessions.
2. Tap each bottom tab to switch screens.
3. Start Walking should move to Live and request sensor access (if needed).
4. Verify Stop Tracking, voice coaching, and CSV exports.

**Research note:** Device-derived step timing is experimental and not a diagnosis. Simulated load and posture situations are not sensor measurements.
