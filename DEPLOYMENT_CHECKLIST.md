# 🚀 GitHub Pages Deployment Checklist

## ✅ Pre-Deployment Steps

### 1. Repository Settings
- [x] Repository name: `ram-krishna-katakwar.github.io` ✓
- [x] Base URL configured in `config.toml` ✓
- [ ] Ensure you're on the `portfolio` branch

### 2. File Setup
- [x] `.gitignore` created ✓
- [x] GitHub Actions workflow created (`.github/workflows/deploy.yml`) ✓
- [x] README.md with instructions ✓

### 3. Build Configuration
- [x] `package.json` has build scripts ✓
- [x] `tailwind.config.js` configured ✓
- [x] Zola `config.toml` configured ✓

## 📝 Deployment Instructions

### Option A: Automatic Deployment (Recommended)

**This is the easiest method - GitHub will build and deploy automatically!**

#### Step 1: Enable GitHub Actions for Pages

1. Go to: https://github.com/ram-krishna-katakwar/ram-krishna-katakwar.github.io/settings/pages
2. Under **"Build and deployment"** section:
   - **Source**: Select **"GitHub Actions"**
   - (Don't select branch - we're using Actions)

#### Step 2: Commit and Push

```bash
# Make sure you're on the portfolio branch
git checkout portfolio

# Add all the new files
git add .

# Commit the changes
git commit -m "Add GitHub Actions workflow for automatic deployment"

# Push to GitHub
git push origin portfolio
```

#### Step 3: Monitor Deployment

1. Go to: https://github.com/ram-krishna-katakwar/ram-krishna-katakwar.github.io/actions
2. You should see a workflow running called "Deploy to GitHub Pages"
3. Wait for it to complete (usually 2-3 minutes)
4. Your site will be live at: https://ram-krishna-katakwar.github.io

#### Troubleshooting

If the workflow fails:
- Click on the failed workflow
- Check the logs to see what went wrong
- Common issues:
  - Permissions: Ensure Actions has Pages write permission (should be automatic)
  - Check that the workflow file is in `.github/workflows/deploy.yml`

---

### Option B: Manual Build and Deploy (Advanced)

**Only use this if you prefer to build locally or if Option A doesn't work.**

#### Prerequisites

Install Zola:
```bash
# macOS
brew install zola

# Or download from: https://github.com/getzola/zola/releases
```

#### Build Locally

```bash
# 1. Install dependencies
npm install

# 2. Build CSS
npm run build

# 3. Build site with Zola
zola build
```

#### Deploy to `main` branch

```bash
# The public/ folder contains your built site
cd public

# Initialize git in public folder
git init
git remote add origin https://github.com/ram-krishna-katakwar/ram-krishna-katakwar.github.io.git

# Commit and push to main
git checkout -b main
git add .
git commit -m "Deploy portfolio"
git push -f origin main
```

Then configure GitHub Pages to use the `main` branch:
1. Go to Settings → Pages
2. Source: Deploy from branch
3. Branch: `main` / `root`

---

## 🎯 Recommended Approach

**Use Option A (Automatic Deployment)** - It's much easier and more maintainable. You just push to `portfolio` branch and GitHub handles everything!

## 🔍 Post-Deployment Verification

After deployment, check:

- [ ] Site loads at: https://ram-krishna-katakwar.github.io
- [ ] Images load correctly
- [ ] CSS styling is applied
- [ ] Links work (GitHub, LinkedIn, Email)
- [ ] Contact form works
- [ ] Dark/light mode toggle works
- [ ] Responsive on mobile devices

## 🐛 Common Issues

### Issue: 404 Page Not Found
**Solution**: Wait 5-10 minutes after first deployment. GitHub Pages can take time to propagate.

### Issue: CSS Not Loading
**Solution**: Check browser console. Ensure Tailwind was built before Zola build.

### Issue: Images Not Loading
**Solution**: Images should be in `static/` folder. Zola copies this to `public/` automatically.

### Issue: Workflow Fails
**Solution**: 
1. Check Actions tab for error logs
2. Ensure package.json and package-lock.json are committed
3. Verify workflow file syntax

## 📱 Contact

If you encounter issues:
- Check GitHub Actions logs
- Review Zola documentation: https://www.getzola.org/documentation/
- Check GitHub Pages status: https://www.githubstatus.com/

---

**Ready to deploy? Start with Option A above! 🚀**

