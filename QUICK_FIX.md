# Instructions to Enable GitHub Pages

Since the automated workflow setup has permission restrictions, here's how to manually enable GitHub Pages:

## Manual Steps to Deploy Your Site

### Step 1: Create the Workflow File Manually
1. Go to: https://github.com/hariompatidar04/seattle-day-planner
2. Click **"Add file"** → **"Create new file"**
3. Type this path: `.github/workflows/deploy.yml`
4. Copy and paste the workflow content below
5. Click **"Commit new file"**

### Step 2: Workflow Content to Paste

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches:
      - main
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

concurrency:
  group: "pages"
  cancel-in-progress: false

jobs:
  deploy:
    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}
    runs-on: ubuntu-latest
    
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Setup Pages
        uses: actions/configure-pages@v4

      - name: Upload artifact
        uses: actions/upload-pages-artifact@v3
        with:
          path: '.'

      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

### Step 3: Enable GitHub Pages
1. Go to **Settings** tab
2. Click **"Pages"** in the left sidebar
3. Under "Build and deployment":
   - **Source**: Select **"GitHub Actions"**
4. The workflow will automatically run

### Step 4: Access Your Site
After 2-3 minutes, visit:
- https://hariompatidar04.github.io/seattle-day-planner/

## Alternative: Use Branch Deployment (Faster)

If GitHub Actions source doesn't work:

1. Go to **Settings** → **Pages**
2. Under "Build and deployment":
   - **Source**: Select **"Deploy from a branch"**
   - **Branch**: Select **"main"** and **"/ (root)"**
3. Click **"Save"**

Your site should be live in 30 seconds at:
- https://hariompatidar04.github.io/seattle-day-planner/

---

**The quickest option: Use "Deploy from a branch" method (Step 3, Alternative)** - it requires no workflow file!
