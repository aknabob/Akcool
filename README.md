# FGGCEFON Cooperative — Management System

Static web app (React + Firebase Realtime Database) with **Chrome Install** support (PWA).

## Deploy on GitHub Pages

1. Create a new GitHub repository (e.g. `coop-manager`).
2. Upload these files to the **root** of the repo (or a `docs/` folder):
   - `index.html`
   - `manifest.webmanifest`
   - `sw.js`
   - `pwa-icons/` (folder with icons)
3. On GitHub: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: `main` (or `master`), folder: `/ (root)` — or `/docs` if you put files there
4. Wait 1–2 minutes, then open:
   `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

## Install on Chrome (desktop or Android)

1. Open the live GitHub Pages URL in **Chrome** (must be HTTPS — Pages provides this).
2. Chrome shows an install icon in the address bar, **or** menu → **Save and share → Install page as app…** / **Install Coop Manager**.
3. The app opens in its own window (standalone) like a native app.

### Requirements for install
- Served over **HTTPS** (GitHub Pages)
- Valid **manifest** + **service worker** (included)
- User engagement (visit the site once)

## Local test

Use any static server from this folder, e.g.:

```bash
npx serve .
# or: python3 -m http.server 8080
```

Then open `http://localhost:8080` — note: Chrome may limit install on localhost but the app still runs.

## Firebase

The app already points at your Firebase Realtime Database project. Ensure Firebase **Realtime Database rules** allow your intended access (and prefer Auth for production).
