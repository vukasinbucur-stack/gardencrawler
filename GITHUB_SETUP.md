# GitHub Setup Guide

Your Garden-Crawler repository is ready! Here's how to get it on GitHub.

---

## Step 1: Configure Git (First Time Only)

Set your GitHub identity:

```bash
git config --global user.name "vook"
git config --global user.email "your-email@example.com"
```

**Use the same email you used for your GitHub account.**

---

## Step 2: Create the Repository on GitHub

1. Go to **github.com** and log in
2. Click the **+** → **New repository**
3. Settings:
   - **Repository name:** `gardencrawler`
   - **Description:** `An open-source autonomous weeding robot for small farms`
   - **Visibility:** ✅ **Public** (important for sponsors!)
   - **Don't** initialize with README, .gitignore, or license (you already have them)
4. Click **Create repository**

---

## Step 3: Connect Local Repo to GitHub

GitHub will show you something like this. Run these commands:

```bash
cd /home/pi/proiectu/gardencrawler

git remote add origin https://github.com/YOUR_USERNAME/gardencrawler.git
git branch -M main
git commit -m "Initial commit: Garden-Crawler open-source farm robot"
git push -u origin main
```

**Replace `YOUR_USERNAME` with your actual GitHub username.**

---

## Step 4: Verify

Visit: `https://github.com/YOUR_USERNAME/gardencrawler`

You should see:
- ✅ Your README
- ✅ All documentation files
- ✅ License file
- ✅ Folder structure

---

## Step 5: Enable GitHub Sponsors

1. Go to your repository on GitHub
2. Click **Settings** (top tab)
3. Scroll to **General** → left sidebar **Sponsors**
4. Click **Create Sponsors profile**
5. Fill in:
   - **Who you are:** Agronomist building open-source farm robots
   - **What you're working on:** Autonomous weeding robot for small farms
   - **Sponsors tiers:** Set up if you want, or skip for now

---

## Step 6: Update README Links

After creating the repo, update these links in `README.md`:

```markdown
# Line ~60: Replace with your actual username
https://github.com/sponsors/YOUR_USERNAME
```

---

## Step 7: Add to Your Substack Footer

Update your Substack posts to include:

```markdown
**GitHub:** https://github.com/YOUR_USERNAME/gardencrawler
```

---

## Repository Structure

```
gardencrawler/
├── .github/
│   ├── FUNDING.yml          # Sponsor link configuration
│   ├── ISSUE_TEMPLATE/      # Bug, feature, question templates
│   └── workflows/           # (for CI/CD later)
├── cad/                     # Fusion 360, STL files
├── docs/                    # All your documentation ✓
│   ├── BOM.md
│   ├── PHASE0_BOM.md
│   ├── SUPPLIERS.md
│   └── PROJECT_CONTEXT.md
├── firmware/                # Python control code
├── hardware/                # KiCad, Fritzing diagrams
├── images/                  # Project photos
├── .gitignore              # Files to exclude
├── CONTRIBUTING.md         # Contribution guidelines
├── LICENSE                 # GPL-3.0
├── README.md               # Project homepage
└── SECURITY.md             # Safety + vulnerability reporting
```

---

## Before You Push

Check that git is configured:

```bash
git config user.name
git config user.email
```

If these return nothing, run Step 1 again.

---

## Common Issues

### "Permission denied (publickey)"
You need SSH keys set up, OR use HTTPS with a personal access token.

**Easier for now:** Use HTTPS with GitHub's token authentication.

### "remote origin already exists"
```bash
git remote remove origin
git remote add origin https://github.com/YOUR_USERNAME/gardencrawler.git
```

### "failed to push some refs"
First time may require:
```bash
git pull --rebase origin main
git push origin main
```

---

## After First Push

Once your repo is live:

1. **Add a project logo** (when you have one)
2. **Pin the repo** to your profile (important!)
3. **Add topics:** robotics, agriculture, open-source, farming, autonomous, weeding
4. **Enable discussions** (optional, for community chat)
5. **Set up branches:** `main` is stable, `dev` for active work

---

## Your Repo URL

Once created, it will be:
```
https://github.com/YOUR_USERNAME/gardencrawler
```

Add this everywhere:
- ✅ Substack footer
- ✅ Reddit posts
- ✅ README file
- ✅ Your email signature (optional)

---

## Ready?

```bash
# Summary of commands to run:
git config --global user.name "vook"
git config --global user.email "your-email@example.com"
git remote add origin https://github.com/YOUR_USERNAME/gardencrawler.git
git commit -m "Initial commit: Garden-Crawler"
git push -u origin main
```

Then visit GitHub and admire your open-source project! 🚀
