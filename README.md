[README.md](https://github.com/user-attachments/files/34252751/README.md)
# STRIDE v1.7 — Dynamic Motion + Automatic Audio Alerts

## Changes
- Larger, more visible step-driven walker animation with improved leg/arm swing and step highlight.
- Always-on voice coaching during an active tracking session (no coaching checkbox).
- Short synthesized two-note chime before speech. Audio is unlocked by the Start action when supported by iOS Safari.
- Event-driven motion notifications: persistent rhythm variability and changes in device tilt.
- No fixed 30-second timer; each distinct alert episode may speak once, subject to a short 6.5-second anti-overlap guard.
- Existing English/Korean voice selection, Sessions, CSV exports, sensor data and settings remain.

## Important scientific limitation
The app **does not detect bad posture**, spinal alignment, pelvic imbalance, or foot pressure. Device tilt represents phone orientation; rhythm variability is experimental. Its thresholds are for prototype UX only, not clinical use. Alerts require continued sensor readings, screen awake and voice/audio permission.

## Deploy
Upload/replace `index.html` in the same GitHub Pages repository. README replacement is optional.

## Test
1. Open in iPhone Safari, tap Start Walking and grant motion/orientation permission.
2. While safely stationary, check movement UI by gently moving the secured phone; test walking only on a clear path.
3. Try a normally paced short walk and a deliberately variable *walking speed* (without unsafe movements).
4. Verify chime precedes voice. Check Events CSV for `motion-alert` records.
5. Verify Korean/English speech selection in Settings.
