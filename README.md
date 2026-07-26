# Latitude 54 — landing page

Single self-contained `index.html` (all CSS, JS, logo, and animations embedded).
Only external dependency: Google Fonts, so the viewer just needs to be online.

## Deploy to Vercel via GitHub

You'll do this once from a folder that contains `index.html`.

### 1. Put index.html in a folder and create the repo

**Option A — GitHub CLI (fastest, if you have `gh` installed):**
```bash
mkdir latitude54-site && cd latitude54-site
# move index.html into this folder first, then:
git init
git add index.html README.md
git commit -m "Latitude 54 landing page"
gh repo create latitude54-site --private --source=. --push
```

**Option B — plain git + GitHub website:**
1. On github.com click **New repository** → name it `latitude54-site` → **Create** (leave it empty, no README).
2. In your folder (with `index.html` inside):
```bash
git init
git add index.html README.md
git commit -m "Latitude 54 landing page"
git branch -M main
git remote add origin https://github.com/<your-username>/latitude54-site.git
git push -u origin main
```

### 2. Import into Vercel
1. Go to **vercel.com** → **Add New → Project**.
2. **Import** the `latitude54-site` repo.
3. On the config screen:
   - **Framework Preset:** Other
   - **Build Command:** leave empty
   - **Output Directory:** `.` (a single period)
   - **Install Command:** leave empty
4. Click **Deploy**. In ~20–30s you get a URL like `latitude54-site.vercel.app` — send that to the client.

### 3. Updating it later
Any change is one push:
```bash
git add index.html
git commit -m "update"
git push
```
Vercel auto-redeploys in ~20–30 seconds.

## Notes
- Deploy this as a **new** Vercel project — don't overwrite the existing `latitude54-website` production site.
- Free/Hobby tier is plenty. Custom domain can be added later for free.
- Tell the client to try it **on mobile** and to press the **Authorize** buttons (decision cycle + BHASM) — those interactions are the point.
- Draft status: founder bios/roles are placeholders and the **NETRA** name is unresolved — not things to react to yet.
