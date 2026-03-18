# Deploy to GitHub Pages

## Quick Setup

1. Push this repo to GitHub:
   ```bash
   git remote add origin https://github.com/<your-username>/chula-mba-surveys-2026.git
   git push -u origin main
   ```

2. Go to your repo on GitHub → **Settings** → **Pages**

3. Under **Source**, select:
   - **Branch:** `main`
   - **Folder:** `/ (root)`

4. Click **Save**

5. Your site will be live at:
   ```
   https://<your-username>.github.io/chula-mba-surveys-2026/
   ```

It typically takes 1-2 minutes for the first deployment.

## Notes

- The site is a single `index.html` file with no build step or dependencies.
- Any push to `main` will automatically redeploy.
- To use a custom domain, add a `CNAME` file with your domain and configure DNS.

push