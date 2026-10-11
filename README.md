# Video Link Downloader PWA

A free, static Progressive Web App for previewing and saving direct video file URLs. It requires no OpenAI API key and no custom backend.

## Run locally
Service workers and PWA installation require a secure context: HTTPS or localhost. Opening `index.html` directly with `file://` will not enable install/offline features.

With Python installed, open a terminal in this folder and run:
```bash
python -m http.server 8000
```
Then visit http://localhost:8000.

## Publish free
1. Create a GitHub repository.
2. Upload `index.html`, `manifest.webmanifest`, `sw.js`, and `icon.svg` to the repository root.
3. In repository Settings → Pages, enable deployment from the main branch and root folder.
4. Open the HTTPS URL GitHub Pages provides. In a supported browser, use the browser's Install app / Add to Home Screen option.

## Limits
- The app works with direct, browser-accessible video file URLs, not arbitrary social-media page URLs.
- A host may block cross-origin playback/downloads or force playback instead of downloading.
- The app does not bypass logins, paywalls, DRM, or platform restrictions.
- The app shell is cached for offline opening; video retrieval needs an internet connection.
