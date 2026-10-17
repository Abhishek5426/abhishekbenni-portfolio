# Deploy "Abhishek Benni Portfolio" to Vercel

Get your portfolio live at **https://abhishekbenni.vercel.app** (same as your friend's `vikas-portfolio-psi-six.vercel.app`).

> Name availability checked on deploy-prep day: `abhishekbenni.vercel.app` was FREE,
> `abhisheksportfolio.vercel.app` was TAKEN. If your chosen name gets claimed before
> you deploy, Vercel will auto-append a suffix — just pick another name in Step 2.3
> (e.g. `abhishekbenni-portfolio`).

---

## Option A — Deploy via GitHub (recommended, auto-updates later)

### 1. Push this project to a GitHub repo
```bash
# inside this project folder
git init
git add .
git commit -m "Abhishek Benni portfolio - initial release"
git branch -M main

# create an EMPTY repo on github.com first (name it: abhishekbenni), then:
git remote add origin https://github.com/<your-github-username>/abhishekbenni.git
git push -u origin main
```

### 2. Import into Vercel
1. Go to **https://vercel.com** → Sign up / Log in **with GitHub**
2. Click **"Add New..." → "Project"**
3. Find the `abhishekbenni` repo → click **"Import"**
4. In **"Project Name"** field, type exactly: `abhishekbenni`
   (this decides your URL: `abhishekbenni.vercel.app`)
5. Leave all other settings as auto-detected (Next.js is detected automatically)
6. Click **"Deploy"** — wait ~1 minute

### 3. Done
Your site is live at `https://abhishekbenni.vercel.app` 🎉

Every future `git push` to `main` auto-redeploys the site — no manual work.

---

## Option B — Deploy via Vercel CLI (no GitHub needed)

```bash
npm i -g vercel
cd <this-project-folder>
vercel

# When prompted:
#   Set up and deploy?            -> Y
#   Which scope?                  -> your account
#   Link to existing project?     -> N
#   Project name?                 -> abhishekbenni
#   In which directory is code?   -> ./  (just press Enter)
#   Modify settings?              -> N

# Then deploy to production:
vercel --prod
```

---

## Optional: custom domain (abhisheksportfolio.com style)

If you want `abhisheksportfolio.com` (or `.in` / `.me`):
1. Buy the domain (~₹500–900/yr) at Namecheap / GoDaddy / Cloudflare
2. In Vercel: **Project → Settings → Domains → Add** your domain
3. Point the domain's DNS records to Vercel (Vercel shows exact records to add)

---

## Notes
- Framework: Next.js 16 (static homepage — loads fast, cheap to host, free tier is plenty)
- No database or environment variables are required for the portfolio itself
- Resume PDF lives at `public/resume/Abhishek_Benni_Resume.pdf` (served at `/resume/Abhishek_Benni_Resume.pdf`)
- To update content later: edit `src/lib/portfolio-data.ts` → commit → push (auto-redeploys)
