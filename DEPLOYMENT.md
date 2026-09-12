# 🚀 Deployment Guide

## GitHub Pages Automatic Deployment

This project is automatically deployed to GitHub Pages using GitHub Actions CI/CD pipeline.

### How It Works

1. **Push to Main Branch** - When you push code to the `main` branch, the GitHub Actions workflow is triggered automatically
2. **Automated Build** - The workflow checks out your code and uploads it to GitHub Pages
3. **Live Deployment** - Your site is immediately available at: `https://hariompatidar04.github.io/seattle-day-planner/`

### Deployment Status

Check the deployment status by visiting:
- **Actions Tab**: https://github.com/hariompatidar04/seattle-day-planner/actions
- **Live Site**: https://hariompatidar04.github.io/seattle-day-planner/

### Manual Workflow Trigger

If you need to manually trigger a deployment:

1. Go to the **Actions** tab in your repository
2. Select the **"Deploy to GitHub Pages"** workflow
3. Click **"Run workflow"**
4. Select the branch (usually `main`)
5. Click **"Run workflow"**

### Repository Settings

GitHub Pages is configured to deploy from:
- **Source**: GitHub Actions
- **Branch**: `main`
- **Directory**: `/` (root)

### What Gets Deployed

All files in the repository root are deployed, including:
- `index.html` - Main application file
- `README.md` - Documentation
- All static assets

### Environment Variables

No environment variables are required for this deployment. The workflow uses GitHub's built-in permissions for Pages deployment.

### Troubleshooting

**Issue**: Site shows 404 error
- **Solution**: Ensure the workflow has completed successfully by checking the Actions tab

**Issue**: Changes not reflecting on live site
- **Solution**: Wait 1-2 minutes for GitHub Pages to cache and serve the new content

**Issue**: Workflow failed to deploy
- **Solution**: Check the workflow logs in the Actions tab for detailed error messages

### Manual Local Testing

To test the site locally before pushing:

```bash
# Clone the repository
git clone https://github.com/hariompatidar04/seattle-day-planner.git
cd seattle-day-planner

# Open in your browser
open index.html
# or
start index.html  # Windows
```

### Making Updates

1. Make changes to your files
2. Commit and push to the `main` branch:
   ```bash
   git add .
   git commit -m "Update: Description of changes"
   git push origin main
   ```
3. The workflow will automatically deploy your changes
4. Check GitHub Pages in 1-2 minutes at: https://hariompatidar04.github.io/seattle-day-planner/

### GitHub Actions Workflow File

The deployment workflow is defined in `deploy.yml`:
- Triggers on every push to `main` and pull requests
- Uses GitHub's official Pages actions for reliable deployment
- Provides automatic rollback on failure

### Support

For issues with GitHub Pages deployment, visit:
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Actions Documentation](https://docs.github.com/en/actions)

---

**Happy Deploying! 🎉**
