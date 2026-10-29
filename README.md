[README.md](https://github.com/user-attachments/files/34134002/README.md)
# STRIDE v1.6 — Visual Motion UI

## Features
- English interface with four tabs: Home, Live, Settings, Sessions.
- Live waveform in the main Live tab.
- Animated walking figure synced to detected steps and cadence, not a true skeletal tracker.
- Relative phone tilt (DeviceOrientation when permitted), experimental lateral motion proxy, and rhythm labels.
- Voice language, voice selection, speaking speed and Wizard-of-Oz simulation moved to Settings.
- Existing sensor tracking, English/Korean TTS and CSV export retained.

## Update GitHub Pages
Replace the repository root `index.html` and commit. `README.md` replacement is optional. Reload Safari and test.

## Scientific limitations
The animated figure is a visualization driven by sensor-derived estimates. The phone does **not** detect full-body pose, spinal alignment, pelvic alignment or plantar pressure. Relative tilt uses the phone's initial angle as a reference; changing the phone position invalidates it. Lateral motion proxy varies with phone orientation. The step counter is exploratory and not clinically validated. Keep the phone secured near the waist for tests.
