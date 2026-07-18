# MVS Dashboard — Web Setup

This repo has two separate pages:

- **View (dashboard):** `index.html` — the live dashboard everyone looks at.
- **Edit (editor):** `editor.html` — where you enter data and publish updates.

## 1. Create the repo
1. On GitHub, create a new **public** repo named `mvs-dashboard` under `kavindyamaheshi303-beep`.
   (Must be public so the dashboard can read `data.json` via raw.githubusercontent.com.)
2. Upload these three files to the repo root: `index.html`, `editor.html`, `data.json`.

## 2. Turn on GitHub Pages
1. Repo → **Settings** → **Pages**.
2. Source: **Deploy from a branch** → Branch: `main` → folder: `/ (root)`.
3. Save. GitHub will give you a URL like:
   `https://kavindyamaheshi303-beep.github.io/mvs-dashboard/`

That's your **view** address (loads `index.html` automatically).
Your **edit** address is the same, plus `editor.html`:
`https://kavindyamaheshi303-beep.github.io/mvs-dashboard/editor.html`

Bookmark the edit URL — it's for you only. Share the view URL with everyone else.

## 3. Connect the editor to GitHub
1. Open the edit URL above (use Chrome — needed for Excel auto-watch linking).
2. In the "Connect GitHub" box, fill in:
   - **GitHub Personal Access Token** (fine-grained, with **Contents: Read and write** access on this repo only)
   - **GitHub Username / Org:** `kavindyamaheshi303-beep`
   - **Repository Name:** `mvs-dashboard`
3. Click **Save & Test Connection**.

Once connected, every publish from the editor updates `data.json` in this repo,
and the dashboard (polling every 20 seconds) picks it up automatically.

## Notes
- Both pages are now branded **MVS Dashboard** (page titles, headers, PWA name, notifications).
- `index.html` already points at this repo's `data.json` (`DATA_URL` is hardcoded — if you ever rename the repo again, update that one line too).
- `data.json` in this repo is a copy of your last published data, just so the dashboard has something to show immediately after setup.
- No app install needed — both pages work as normal websites. (The dashboard does still offer "Add to Home Screen" as an optional PWA install, but that's not required to use it.)
