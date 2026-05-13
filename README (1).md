# Project YouTube — Focused Feed

> Your Watch Later playlist, organised by mood. No algorithm, no distraction.

---

## What it does

Takes your YouTube Watch Later playlist and automatically organises it into focus categories — so when you want to learn about health, you see only health videos. When you want news, only news. No algorithm pulling you in 10 directions.

**Features:**
- Auto-categorises your Watch Later using Gemini AI — categories derived from your actual content
- Click any video → plays embedded on the left, summary panel on the right
- Click Summarise → focused breakdown in the anchor's own style
- Timestamps in summaries are clickable — jumps the video to that exact moment
- Zero backend, zero data stored anywhere, completely private

---

## For users

1. Open the app at your GitHub Pages link
2. Sign in with Google — the account linked to your YouTube
3. Get a free Gemini API key at aistudio.google.com → Create API Key
4. Paste your key → click Load
5. Your Watch Later loads and gets categorised automatically

Your API key is stored only in your browser. Never leaves your device.

---

## For developers / self-hosting

### 1. Fork this repo

### 2. Create a Google OAuth Client ID

1. Go to console.cloud.google.com
2. Create a new project
3. Enable YouTube Data API v3
4. APIs & Services → OAuth consent screen → External → fill in details
5. Credentials → Create Credentials → OAuth 2.0 Client ID
6. Application type: Web application
7. Authorised JavaScript origins: https://YOUR-USERNAME.github.io
8. Copy the Client ID

### 3. Add your Client ID

Open index.html and find:
```
const GOOGLE_CLIENT_ID = 'YOUR_GOOGLE_CLIENT_ID_HERE.apps.googleusercontent.com';
```
Replace with your actual Client ID.

### 4. Enable GitHub Pages

Settings → Pages → Deploy from branch → main / root → Save

Live at: https://YOUR-USERNAME.github.io/project-youtube

---

## Privacy

- OAuth token stored only in browser session
- Gemini API key stored in browser localStorage only
- No analytics, no tracking, no backend, no server

---

## Tech stack

Pure HTML + CSS + JavaScript. No frameworks. One file: index.html

---

## License

MIT — use it, fork it, share it freely.
