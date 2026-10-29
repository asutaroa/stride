[README.md](https://github.com/user-attachments/files/34125479/README.md)
# STRIDE | Bilingual Voice Coaching Research Prototype (v1.1)

STRIDE is an English-language, mobile-friendly research web app. Its manually triggered coaching scenarios support **English and Korean spoken feedback** using the browser's Web Speech API.

## Publish on GitHub Pages

1. Create or open a public repository named `stride-research`.
2. Upload the included `index.html` to the **root directory**. If an older `index.html` is present, replace its contents or upload the revised file using GitHub's edit interface.
3. Go to **Settings → Pages → Build and deployment → Deploy from a branch**.
4. Set branch to `main` and folder to `/(root)`, then save.
5. Open `https://YOUR-USERNAME.github.io/stride-research/`.

## Test bilingual speech

1. Open **02 / Coaching Simulation**.
2. Select a simulated gait condition.
3. Set **Coaching voice language** to **English** or **한국어 (Korean)**.
4. Select **Play Voice Coaching**. Use **Stop Voice** to stop speech.

The interface remains English in both language modes. Available voice quality and pronunciation depend on the voices installed on your device and supported by the browser.

## Test device motion

Open the site over HTTPS on a smartphone and choose **Start Sensor / Request Permission**. Device/browser support varies, especially on iOS. Walking step counts and cadence are preliminary estimates, not validated measurements.

## Research and safety notes

- The live-motion view uses actual browser device-motion readings **if supported**.
- Right-foot loading and trunk-lean scenarios are **manual simulations**, not actual diagnoses or sensor detections.
- Coaching uses predefined decision rules and text-to-speech, **not a trained AI model**.
- No data is sent to any server by this HTML file. CSV export creates a local file.
- Do not look at the phone while walking. Not for clinical or medical use.
