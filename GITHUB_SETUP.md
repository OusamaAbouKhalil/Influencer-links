# 🚀 Upload to GitHub - Quick Guide

Your local git repository is ready! Follow these steps to upload to GitHub.

---

## ✅ What's Already Done

- ✅ Git repository initialized
- ✅ All files committed
- ✅ .gitignore configured
- ✅ README files created

**Commit:** `Initial commit: OEG Referral Pages with auto-detection and UTM tracking`
**Files:** 10 files, 1972 insertions

---

## 📦 Step 1: Create GitHub Repository

### Option A: Using GitHub Website (Easiest)

1. **Go to GitHub:**
   - Visit: https://github.com/new

2. **Create Repository:**
   - **Repository name:** `oeg-referral-pages`
   - **Description:** `Professional influencer referral pages with auto-detection and UTM tracking for OEG app`
   - **Visibility:** 
     - ✅ **Public** (if you want to share)
     - ⚠️ **Private** (if you want to keep it confidential)
   - ❌ **DO NOT** initialize with README (we already have one)
   - ❌ **DO NOT** add .gitignore (we already have one)
   - ❌ **DO NOT** add license yet

3. **Click:** "Create repository"

### Option B: Using GitHub CLI

```bash
# Install GitHub CLI if not installed: https://cli.github.com/

gh repo create oeg-referral-pages --public --source=. --remote=origin
```

---

## 🔗 Step 2: Connect and Push

After creating the repo on GitHub, you'll see a page with instructions. Use these commands:

### In PowerShell (from referral-pages folder):

```powershell
# Add GitHub as remote
git remote add origin https://github.com/YOUR_USERNAME/oeg-referral-pages.git

# Rename branch to main (GitHub's default)
git branch -M main

# Push to GitHub
git push -u origin main
```

**Replace `YOUR_USERNAME` with your actual GitHub username!**

---

## 📋 Complete Command Sequence

Copy and paste these commands one by one:

```powershell
# 1. Add remote (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/oeg-referral-pages.git

# 2. Rename branch
git branch -M main

# 3. Push to GitHub
git push -u origin main
```

---

## 🎯 Expected Output

```
Enumerating objects: 10, done.
Counting objects: 100% (10/10), done.
Delta compression using up to 8 threads
Compressing objects: 100% (9/9), done.
Writing objects: 100% (10/10), 150.52 KiB | 7.53 MiB/s, done.
Total 10 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/YOUR_USERNAME/oeg-referral-pages.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
```

---

## ✅ Verify Upload

1. **Go to your GitHub repository:**
   ```
   https://github.com/YOUR_USERNAME/oeg-referral-pages
   ```

2. **You should see:**
   - ✅ All 10 files
   - ✅ README displayed on homepage
   - ✅ Commit message visible
   - ✅ Logo images
   - ✅ All folders (raphael, template)

---

## 🌐 Step 3: Enable GitHub Pages (Optional)

To host your referral pages for FREE on GitHub:

1. **Go to repository Settings**
2. **Navigate to:** Pages (left sidebar)
3. **Source:** Deploy from branch
4. **Branch:** Select `main` → `/root` → Save
5. **Wait 1-2 minutes**

Your pages will be live at:
```
https://YOUR_USERNAME.github.io/oeg-referral-pages/
```

**Test URLs:**
- Dashboard: `https://YOUR_USERNAME.github.io/oeg-referral-pages/`
- Raphael: `https://YOUR_USERNAME.github.io/oeg-referral-pages/raphael/`
- Template: `https://YOUR_USERNAME.github.io/oeg-referral-pages/template/`

---

## 🔐 Using SSH Instead of HTTPS (Advanced)

If you prefer SSH:

```powershell
# 1. Add remote with SSH
git remote add origin git@github.com:YOUR_USERNAME/oeg-referral-pages.git

# 2. Push
git push -u origin main
```

**Note:** Requires SSH key setup on GitHub.

---

## 🎨 Step 4: Customize Repository

### Add Repository Topics (Tags)

On GitHub repository page:
1. Click ⚙️ (settings icon near About)
2. Add topics:
   - `influencer-marketing`
   - `utm-tracking`
   - `landing-page`
   - `referral-system`
   - `mobile-apps`
   - `javascript`
   - `html-css`

### Update README

If you want to customize the GitHub README:
```powershell
# Edit README_GITHUB.md locally
# Then commit and push
git add README_GITHUB.md
git commit -m "Update README"
git push
```

### Add License

1. On GitHub repo page
2. Click "Add file" → "Create new file"
3. Name: `LICENSE`
4. GitHub will show license templates
5. Choose: MIT License
6. Commit

---

## 📝 Future Updates

When you make changes locally:

```powershell
# 1. Add changes
git add .

# 2. Commit with message
git commit -m "Updated Raphael's page design"

# 3. Push to GitHub
git push
```

---

## 🆘 Troubleshooting

### Error: "remote origin already exists"
```powershell
# Remove old remote
git remote remove origin

# Add new remote
git remote add origin https://github.com/YOUR_USERNAME/oeg-referral-pages.git
```

### Error: "failed to push"
```powershell
# Pull first (if repo has changes)
git pull origin main --allow-unrelated-histories

# Then push
git push -u origin main
```

### Error: "authentication failed"
- GitHub no longer accepts passwords
- Use Personal Access Token instead:
  1. GitHub → Settings → Developer settings
  2. Personal access tokens → Tokens (classic)
  3. Generate new token → Select "repo" scope
  4. Use token as password when pushing

---

## 🎉 What's Next?

After uploading to GitHub:

1. ✅ **Enable GitHub Pages** for free hosting
2. ✅ **Share repository** with your team
3. ✅ **Create Bitly links** pointing to GitHub Pages URLs
4. ✅ **Monitor analytics** in Firebase/Play Console
5. ✅ **Create more influencer pages** using the template

---

## 📞 Need Help?

- **GitHub Docs:** https://docs.github.com/en/get-started
- **Git Basics:** https://git-scm.com/book/en/v2
- **GitHub Pages:** https://pages.github.com/

---

**Repository Ready! 🚀**

Your referral pages are now version controlled and ready to share!

