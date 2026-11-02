[README.md](https://github.com/user-attachments/files/34272501/README.md)
# STRIDE v2.9 — Korean voice reliability

- Korean coaching selects only exact `ko-KR` voice matches, preferring enhanced/premium voices when available.
- Prevents wrong-language fallback when no Korean voice is exposed.
- Displays selected voice for troubleshooting; no manual voice picker.
- Uses a slightly slower Korean speech rate.
- All other v2.8 features retained.

Deploy by replacing `index.html` in GitHub Pages. Keep `config.js` and Supabase database unchanged.

On iPhone, if the Korean voice remains unnatural, try Settings > Accessibility > Spoken Content > Voices > Korean and download a higher quality available voice, then fully restart Safari. Available names and menu wording depend on iOS version. Browser speech cannot guarantee the same studio-natural voice on all devices.
