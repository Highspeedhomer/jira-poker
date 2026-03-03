# 🚀 Setup Guide — GitHub Pages Deployment

Your Jira Poker app will be live at:
`https://YOUR-USERNAME.github.io/jira-poker`

---

## Step 1 — Create a GitHub repo

1. Go to **github.com** → click the **+** in the top right → **New repository**
2. Name it: `jira-poker`
3. Set to **Public** (required for free GitHub Pages)
4. Leave everything else as default → click **Create repository**

---

## Step 2 — Push the files

In your terminal, navigate to this folder and run:

```bash
cd path/to/jira-poker-repo

git init
git add .
git commit -m "Initial commit — Jira Poker"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/jira-poker.git
git push -u origin main
```

Replace `YOUR-USERNAME` with your actual GitHub username.

---

## Step 3 — Enable GitHub Pages

1. Go to your repo on GitHub
2. Click **Settings** (top tab)
3. Click **Pages** in the left sidebar
4. Under **Source** → select **Deploy from a branch**
5. Branch: `main` · Folder: `/ (root)` → click **Save**

GitHub will show:
> ✅ Your site is live at `https://YOUR-USERNAME.github.io/jira-poker`

Takes about 60 seconds the first time.

---

## Step 4 — Share with your team

Send them the URL:
```
https://YOUR-USERNAME.github.io/jira-poker
```

They click it, enter their name and room code — done. No install, no account needed.

---

## Updating the app

Any time you get an updated `index.html`, just replace the file and push:

```bash
cp /path/to/new/jira-poker.html index.html
git add index.html
git commit -m "Update app"
git push
```

GitHub Pages redeploys automatically in ~30 seconds.

---

## Optional: Custom URL like `jirapoker.yourteam.com`

If you have a domain:
1. In GitHub Pages settings, enter your domain under **Custom domain**
2. Add a `CNAME` DNS record pointing to `YOUR-USERNAME.github.io`

---

## Troubleshooting

**Page shows raw HTML / 404?**
- Make sure the file is named exactly `index.html` (not `jira-poker.html`)
- Make sure `.nojekyll` file is in the repo root
- Wait 60–90 seconds for first deploy

**Firebase not connecting?**
- The Firebase config is already baked into `index.html` — nothing to change
- Make sure your Firebase Realtime Database is in **Test mode** (or has open read/write rules)

**Check deploy status:**
Go to your repo → **Actions** tab → you'll see the Pages deployment running or completed
