# BabyBuLL ($BBULL) Website

Static one-page site for the BabyBuLL memecoin. No build step needed — just
`index.html` + the `assets/` folder.

## Deploy with GitHub Pages (free)

### Option A — Using GitHub website only (no terminal needed)
1. Go to https://github.com and log in (create a free account if you don't have one).
2. Click the **+** icon (top right) → **New repository**.
   - Repository name: `babybull-website` (or anything you like)
   - Set it to **Public**
   - Click **Create repository**
3. On the new repo page, click **uploading an existing file**.
4. Drag in **both**: `index.html` and the whole `assets` folder (keep the folder structure — don't flatten it).
5. Scroll down, click **Commit changes**.
6. Go to the repo's **Settings** tab → **Pages** (left sidebar).
7. Under "Build and deployment" → Source: **Deploy from a branch**.
   - Branch: `main`, folder: `/ (root)` → **Save**.
8. Wait 1–2 minutes, then refresh the Pages settings — you'll see a live URL like:
   `https://<your-username>.github.io/babybull-website/`

That link is public and shareable with anyone.

### Option B — Using git in a terminal
```bash
cd bbull-site
git init
git add .
git commit -m "Initial BabyBuLL website"
git branch -M main
git remote add origin https://github.com/<your-username>/babybull-website.git
git push -u origin main
```
Then enable Pages the same way as steps 6–8 above.

## Updating the site later (e.g. adding the real CA)
1. Edit `index.html` (or ask Claude to do it for you again).
2. On GitHub, open the file → click the pencil (Edit) icon → paste the new content → **Commit changes**.
   - Or, if using git: edit locally, then `git add . && git commit -m "add CA" && git push`.
3. GitHub Pages auto-redeploys within a minute or two — no extra steps.

## Who can edit the live site?
Only people with **write access to this GitHub repository** (i.e. you, or anyone
you explicitly invite as a collaborator). Visitors to the website can only view
it — viewing "page source" in a browser does not let them change your actual
files on GitHub.

## Custom domain (optional)
If you buy a domain later (e.g. babybull.com), add a `CNAME` file with your
domain name in the repo root, then point your domain's DNS to GitHub Pages —
GitHub's docs walk through this: https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site
