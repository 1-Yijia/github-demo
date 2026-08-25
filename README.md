# GitLab Pages Test

A minimal static site to test GitLab Pages deployment.

## Structure
- `public/index.html` — the page GitLab serves (Pages requires the `public/` folder)
- `.gitlab-ci.yml` — pipeline that publishes `public/` as a Pages artifact

## Deploy
1. Create an empty project on your company GitLab.
2. From this folder:
   ```
   git init
   git remote add origin <your-gitlab-project-url>
   git add .
   git commit -m "Test GitLab Pages deployment"
   git push -u origin main
   ```
3. Watch the pipeline: **Build → Pipelines**.
4. Once it passes, find the live URL under **Deploy → Pages**.

## Notes
- Deploys only on the default branch (see `rules` in `.gitlab-ci.yml`).
- Page visibility (public vs. group-only) is controlled in **Settings → General → Visibility → Pages**.
