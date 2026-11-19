# Stillwater — Breathe & Meditate

A meditation web app: box breathing, 4-7-8, guided meditation timer, daily goal and progress tracking.
No build step, no server, no database. Just upload this folder to any static host.

## What's in this folder

| File | What it does |
|---|---|
| `index.html` | The whole app (HTML, CSS and JavaScript in one file) |
| `manifest.webmanifest` | Lets people install it on their phone or computer like an app |
| `sw.js` | Service worker: makes it load instantly and work offline |
| `icon.svg`, `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` | App icons |

Keep all files together in the same folder.

## Deploy in 2 minutes (easiest): Netlify Drop

1. Unzip `stillwater-app.zip`.
2. Go to https://app.netlify.com/drop
3. Drag the `stillwater-app` folder onto the page.
4. You get a live link like `https://something.netlify.app`.
5. Sign up / log in (free) and **claim the site**, otherwise it is deleted after a short time.
6. Optional: Site settings → Change site name → e.g. `stillwater-tanmay.netlify.app`.

**To update later:** open the site in Netlify → Deploys → drag the updated folder onto the drop area.

## Option 2: Cloudflare Pages (unlimited bandwidth)

1. Sign up free at https://dash.cloudflare.com
2. Workers & Pages → Create → Pages → **Upload assets** (drag and drop).
3. Name the project (this becomes `your-name.pages.dev`), drag in the folder, Deploy.

## Option 3: GitHub Pages (good if you already use GitHub)

1. Create a new **public** repository, e.g. `stillwater`.
2. Add file → Upload files → drag in everything from this folder → Commit.
3. Settings → Pages → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)` → Save.
4. After 1–2 minutes it is live at `https://<your-username>.github.io/stillwater/`.

## After deploying

- **Install it on a phone:** open the link in Chrome (Android) → menu → *Install app* / *Add to Home screen*.
  On iPhone: open in Safari → Share → *Add to Home Screen*. It then opens full-screen with its own icon.
- **Works offline** after the first visit.
- **Screen stays awake** during a session (on browsers that support it).
- History and settings are stored on each user's own device (browser storage). Nothing is sent to a server.

## Updating the app

If you change `index.html`, also change `VERSION` at the top of `sw.js`
(e.g. `stillwater-v1` → `stillwater-v2`) so returning users get the new version.

## Test it on your own computer first (optional)

```bash
cd stillwater-app
python -m http.server 8000
```
Then open http://localhost:8000
