# 🔧 GitHub Pages Setup Guide

## Issue: Site Shows 404

If you're seeing a 404 error when trying to access your site at:
`https://hariompatidar04.github.io/seattle-day-planner/`

Follow these steps to enable GitHub Pages:

## Manual Setup Steps

### Step 1: Go to Repository Settings
1. Navigate to your repository: https://github.com/hariompatidar04/seattle-day-planner
2. Click the **Settings** tab at the top
3. Scroll down to find **"Pages"** in the left sidebar

### Step 2: Configure GitHub Pages
1. Under **"Build and deployment"** section:
   - **Source**: Select **"GitHub Actions"**
   - This will use the automated workflow we created

2. If the "GitHub Actions" option isn't visible:
   - Check that you have the `deploy.yml` file in `.github/workflows/` directory
   - Ensure the workflow has proper permissions set

### Step 3: Trigger the Workflow
Option A - Automatic (after enabling GitHub Actions source):
- Make any small change and push to main branch
- The workflow will automatically deploy

Option B - Manual Trigger:
1. Go to the **Actions** tab in your repository
2. Find the **"Deploy to GitHub Pages"** workflow
3. Click the workflow name
4. Click **"Run workflow"** button
5. Select branch: **main**
6. Click **"Run workflow"**

### Step 4: Wait for Deployment
- The workflow will run (takes 1-2 minutes)
- You'll see a green checkmark when complete
- Access your site at: `https://hariompatidar04.github.io/seattle-day-planner/`

## Verify Deployment

After following these steps:
1. Check the Actions tab to confirm the workflow succeeded (green checkmark)
2. Wait 1-2 minutes for GitHub's CDN to cache
3. Visit: https://hariompatidar04.github.io/seattle-day-planner/
4. You should now see your World Time Zone Clock app!

## Troubleshooting

### Problem: Still seeing 404
**Solution:**
- Clear your browser cache (Ctrl+Shift+Delete or Cmd+Shift+Delete)
- Try in an incognito/private window
- Wait a few more minutes for GitHub's CDN to propagate

### Problem: Workflow shows failed
**Solution:**
1. Go to Actions tab
2. Click the failed workflow run
3. Click the "deploy" job
4. Read the error message
5. Common issues:
   - Missing permissions (should be fixed in deploy.yml)
   - Branch name mismatch (should be "main")

### Problem: Can't find Pages settings
**Solution:**
1. Make sure you're on the repo's Settings tab (not profile settings)
2. You should have admin permissions on the repo
3. Scroll all the way down - Pages is typically near the bottom

## GitHub Pages URL Format

Your site should be accessible at:
```
https://hariompatidar04.github.io/seattle-day-planner/
```

**Note:** The URL includes your username and repository name

## What Gets Deployed

The GitHub Actions workflow deploys:
- `index.html` - Main application
- `README.md` - Documentation  
- All other files in the repository root
- Static assets (CSS, JS are embedded in index.html)

## Support Resources

- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Actions Workflow Troubleshooting](https://docs.github.com/en/actions/monitoring-and-troubleshooting-workflows)
- [Configure a publishing source for your GitHub Pages site](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

---

**Once configured, your site will deploy automatically on every push to the main branch! 🚀**
