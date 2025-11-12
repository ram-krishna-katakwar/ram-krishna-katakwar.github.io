# 🚀 Quick Start - Deploy in 5 Minutes

## 📝 What You Need to Do

Your portfolio website is ready to deploy to GitHub Pages! Here's the quickest way:

## Step 1: Enable GitHub Actions for Pages (One-time setup)

1. **Go to your repository settings:**
   ```
   https://github.com/ram-krishna-katakwar/ram-krishna-katakwar.github.io/settings/pages
   ```

2. **Under "Build and deployment":**
   - Find the **"Source"** dropdown
   - Select **"GitHub Actions"** (not "Deploy from a branch")
   
   ![Pages Settings](https://docs.github.com/assets/cb-47267/mw-1440/images/help/pages/publishing-source-drop-down.webp)

## Step 2: Commit and Push Your Code

Run these commands in your terminal:

```bash
# Make sure you're in the right directory
cd /Users/I0986/Code/ram-krishna-katakwar.github.io

# Add all the new configuration files
git add .

# Commit with a message
git commit -m "Setup GitHub Pages with automatic deployment"

# Push to GitHub
git push origin portfolio
```

## Step 3: Watch It Deploy! 

1. **Go to Actions tab:**
   ```
   https://github.com/ram-krishna-katakwar/ram-krishna-katakwar.github.io/actions
   ```

2. **You'll see:** A workflow called "Deploy to GitHub Pages" running

3. **Wait:** About 2-3 minutes for it to complete

4. **Visit your site:**
   ```
   https://ram-krishna-katakwar.github.io
   ```

## ✅ That's It!

Your portfolio is now live! 

Every time you push to the `portfolio` branch, it will automatically rebuild and redeploy.

---

## 🔄 Making Updates Later

After the initial deployment, updating your site is simple:

```bash
# 1. Make your changes to content/_index.md or templates

# 2. Commit and push
git add .
git commit -m "Update portfolio content"
git push origin portfolio

# 3. Wait 2-3 minutes - your site updates automatically!
```

---

## 🐛 Troubleshooting

**Q: The workflow is failing?**
- Check the Actions tab and click on the failed run to see error logs
- Make sure you selected "GitHub Actions" in Pages settings

**Q: Site shows 404?**
- Wait 5-10 minutes after first deployment
- Check that the workflow completed successfully

**Q: CSS looks broken?**
- This shouldn't happen with automatic deployment
- If it does, check the Actions logs for build errors

**Q: I don't see the workflow running?**
- Make sure `.github/workflows/deploy.yml` was committed
- Check that you pushed to the `portfolio` branch

---

## 📚 Need More Details?

See `DEPLOYMENT_CHECKLIST.md` for comprehensive instructions and troubleshooting.

---

**Good luck! 🎉**

