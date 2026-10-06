# The Poor Man's Library — static site

A permanent, self-hosted home for the library. No expiring links, and real
readership stats (pageviews + PDF downloads).

## What's in this folder

- `index.html` — the whole library: shelf, all five books readable online, journal
- `pdfs/` — the five book PDFs (linked with relative paths, so they work anywhere)

## Deploy — Option A: GitHub Pages (recommended, free forever)

1. Create a free account at https://github.com (email + password).
2. Create a **new public repository** named `poor-mans-library`.
3. On the repo page, click **"uploading an existing file"** and drag in
   `index.html` plus the five PDFs inside a `pdfs/` folder.
   (Or: `git push` if you use the command line.)
4. Go to **Settings → Pages** → under "Build and deployment" choose
   **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
5. Wait ~2 minutes. Your library is live at
   `https://<your-username>.github.io/poor-mans-library/`

## Deploy — Option B: Netlify Drop (fastest, no account needed)

1. Go to https://app.netlify.com/drop
2. Drag this entire folder onto the page.
3. You instantly get a live URL like `https://random-name-123.netlify.app`.
   (Claim it with a free account later if you want to rename it.)

## Readership stats — GoatCounter (free, no cookies, no tracking)

1. Sign up free at https://www.goatcounter.com — pick a **site code**
   (e.g. `poormanslibrary`). No credit card.
2. Open `index.html`, find `YOUR-GOATCOUNTER-CODE` (2 spots), replace both
   with your code.
3. Re-upload/redeploy `index.html`.
4. Your dashboard at `https://<your-code>.goatcounter.com` shows pageviews,
   and every PDF download is counted as an event under `/download/…`.

Until the code is set, the analytics snippet does nothing — the site works
fine without it.

## After deploying

Tell Rook the live URL. The old expiring-link system (the daily refresh job)
can then be retired, and the library link handed out becomes permanent.
