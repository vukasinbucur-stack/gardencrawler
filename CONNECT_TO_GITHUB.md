# Connect to Your GitHub Account

Using your existing GitHub account with Garden-Crawler.

---

## Step 1: Find Your GitHub Username & Email

1. Go to **github.com** and log in (you're already logged in probably)
2. Click your profile picture → **Settings**
3. Your **username** is at the top: `github.com/YOUR_USERNAME`
4. Go to **Emails** (left sidebar) — note your primary email

---

## Step 2: Configure Git Locally

Run this (replace with YOUR actual details):

```bash
git config --global user.name "Your Name"
git config --global user.email "your-github-email@example.com"
```

**Use the SAME email that's on your GitHub account.** This is important for commits to link to your profile.

---

## Step 3: Add Project Email (Optional)

If you want `crawlergarden@gmail.com` as project contact:

1. Go to GitHub → Settings → Emails
2. Click **Add email address**
3. Enter `crawlergarden@gmail.com` and verify
4. You can keep your main email as primary

Then in the repo, people can reach you at the project email without it being public.

---

## Step 4: Create the Repository on GitHub

1. Go to **github.com** → **+** → **New repository**
2. Fill in:
   - **Repository name:** `gardencrawler`
   - **Description:** `An open-source autonomous weeding robot for small farms`
   - **Visibility:** ✅ **Public**
   - **Don't** check README, .gitignore, or license (you have them)
3. Click **Create repository**

---

## Step 5: Connect and Push

GitHub will show you these commands. Run them:

```bash
cd /home/pi/proiectu/gardencrawler

# Add your GitHub repo as remote
git remote add origin https://github.com/vukasinbucur-stack/gardencrawler.git

# Push to GitHub
git branch -M main
git commit -m "Initial commit: Garden-Crawler open-source farm robot"
git push -u origin main
```

**Replace `YOUR_USERNAME` with your actual GitHub username.**

---

## Step 6: Verify It Worked

Visit: `https://github.com/vukasinbucur-stack/gardencrawler`

You should see your README, all the docs, and the full structure.

---

## Step 7: Quick Updates Before Pushing

Edit these files with your actual username:

### In `README.md` (line ~60):
```markdown
## Sponsor
If this project helps you, consider **[sponsoring on GitHub](https://github.com/sponsors/YOUR_USERNAME)**.
```

### In `.github/FUNDING.yml`:
```yaml
github:
  YOUR_USERNAME: [optional: replace with a tiered sponsor link]
```

### Add your email to README (optional, end of file):
```markdown
---

**Contact:** crawlergarden@gmail.com
```

---

## Step 8: Enable Sponsors (After First Push)

1. Go to your repo → **Settings**
2. Left sidebar → **Sponsors**
3. Click **Create Sponsors profile**
4. Fill in:
   - **Who are you:** Agronomist in Romania building open-source farm robots
   - **What you're working on:** Autonomous weeding robot for small farms (~€600)
   - **Goals:** You can set funding milestones if you want

---

## Commands Summary

```bash
# 1. Configure git (do once)
git config --global user.name "Your Name"
git config --global user.email "your-email@example.com"

# 2. Create repo on github.com (do in browser)

# 3. Push to GitHub
cd /home/pi/proiectu/gardencrawler
git remote add origin https://github.com/vukasinbucur-stack/gardencrawler.git
git branch -M main
git commit -m "Initial commit: Garden-Crawler"
git push -u origin main
```

---

## Once Live

1. **Pin the repo** to your profile (makes it prominent)
2. **Add topics:** `robotics` `agriculture` `open-source` `farming` `autonomous`
3. **Copy the URL** for your Substack footer

Your repo will be:
```
https://github.com/YOUR_USERNAME/gardencrawler
```

---

## Ready?

What's your GitHub username? I can update the files with it before you push.
