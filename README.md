# RadiFind static mirror

This repository hosts a static copy of the RadiFind landing page for publishing via GitHub Pages.

## Local structure

- `index.html` — main entry file (cleaned of browser injection content)
- `RadiFind_files/` — saved assets (images, CSS, JS bundle)

Note: Some icons reference absolute URLs (e.g. `/icons/spritemap.svg`) from the original site. Those icons may not render unless you also mirror those assets.

## Publish to GitHub Pages

1) Create a new repository on GitHub (public or private with Pages enabled).

2) From this folder, initialize git and push:

```bash
git init
git checkout -b main
git add .
git commit -m "Initial commit: static site"
git remote add origin https://github.com/<your-username>/<your-repo>.git
git push -u origin main
```

3) Enable Pages:

- In your GitHub repo: Settings → Pages
- Source: “Deploy from a branch”
- Branch: `main` and folder `/ (root)`
- Save

GitHub will provide a Pages URL like `https://<your-username>.github.io/<your-repo>/` after it builds.

## Optional: Custom domain

If you own a domain, add a `CNAME` file at the repo root with your domain (e.g. `example.com`), then point your DNS to GitHub Pages per the GitHub docs.

## Notes

- The JS bundle was saved by the browser with a `.download` suffix; a `.js` copy is provided and referenced by `index.html`.
- External assets (favicons, fonts) still load from the original host. To make this repo fully self-contained, download and update those references to local files.


