# Portfolio site

A single static page (no build tools, no framework) listing your projects as
"positions" on a trading-blotter-style table, with a live link to each one.

## Files
- `index.html` — page content/structure
- `style.css` — all styling

## Before you publish — replace these placeholders
1. In `index.html`:
   - `https://huggingface.co/spaces/REPLACE-ME/sentiment-dashboard` → your real Hugging Face Space URL once deployed
   - `mailto:REPLACE-ME@example.com` → your email
   - `linkedin.com/in/REPLACE-ME` → your LinkedIn
   - `github.com/REPLACE-ME` → your GitHub
2. Update the hero text/about copy if you want a different framing.

## Deploy with GitHub Pages (free, no separate hosting needed)

1. Create a new GitHub repo, e.g. `portfolio`.
2. Add `index.html` and `style.css` to the repo root and push:
   ```bash
   git init
   git add index.html style.css
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/portfolio.git
   git push -u origin main
   ```
3. On GitHub: go to the repo → **Settings → Pages** → under "Build and
   deployment", set **Source: Deploy from a branch**, branch: `main`,
   folder: `/ (root)`. Save.
4. After a minute, your site is live at:
   ```
   https://YOUR-USERNAME.github.io/portfolio/
   ```

That URL is what you'd share with an interviewer. It links out to your live
Streamlit/Hugging Face app, so each project keeps running on the platform
that's right for it instead of being crammed into one deployment.

## Using your own domain (optional)
If you already own a domain (or buy one later):
1. In the repo, add a file named `CNAME` containing just your domain, e.g.
   `minh.dev`
2. At your domain registrar, add a `CNAME` record pointing to
   `YOUR-USERNAME.github.io`
3. Back in GitHub Pages settings, enter the custom domain and enable
   "Enforce HTTPS"

## Adding more projects later
Duplicate the `.row-link` block in `index.html` (the one with `SENT` as the
symbol) for each new project — give it a new ticker symbol, name, type, and
link. The empty "OPEN" row below it is just a placeholder; you can delete it
once you have a second real project, or keep it as a visual cue that more is
coming.
