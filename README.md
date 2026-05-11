# soundoffcaptions.app

Marketing + support site for [Sound Off](https://soundoffcaptions.app), the on-device caption app for iPhone.

Plain HTML / CSS, no JavaScript, no build step. Hosted on GitHub Pages with a custom Hover domain. Three pages:

- `index.html` — landing
- `privacy.html` — privacy policy
- `support.html` — support + FAQs

Visual system: dark + amber palette matching the iOS app, Geist + Instrument Serif via Google Fonts. Tokens defined as CSS variables in `styles.css`; lifted from the app's design handoff.

## Updating the watermark text reference

The export watermark string is `Sound Off Captions` — the App Store listing name — for in-video discoverability. Anywhere copy references it (`support.html`, the app's own docs), keep that exact string. Source of truth: `SoundOff/Sources/Export/WatermarkLayer.swift` in the app repo.

## DNS

Hover → `soundoffcaptions.app` →
- `ALIAS @` → `ashleymills.github.io.`
- `CNAME www` → `ashleymills.github.io.`

GitHub Pages auto-issues an HTTPS cert once DNS propagates.
