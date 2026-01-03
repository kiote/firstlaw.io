---
name: deploy
description: Deploy the Hugo site to production at firstlaw.io via GitHub Pages. Use when asked to deploy, publish, push to prod, or release the site.
---

# Deploy to Production

This skill deploys the Hugo static site to GitHub Pages at https://firstlaw.io/.

## Deployment Steps

1. **Build the site**
   ```bash
   hugo --minify
   ```
   This generates the static site in the `public/` directory.

2. **Create CNAME file** (if not present)
   ```bash
   echo "firstlaw.io" > public/CNAME
   ```

3. **Deploy to GitHub Pages using gh-pages branch**
   ```bash
   cd public
   git init
   git add -A
   git commit -m "Deploy site"
   git push -f git@github.com:kiote/firstlaw.io.git main:gh-pages
   ```

## Pre-deployment Checklist

- Ensure all content changes are committed
- Run `hugo server` locally to preview changes
- Check for draft posts (`draft: true` in frontmatter)
- Verify images and assets are in `static/` directory

## Troubleshooting

- **404 errors**: Ensure CNAME file exists in `public/` after build
- **Missing styles**: Check that theme submodule is properly initialized (`git submodule update --init`)
- **Build failures**: Run `hugo --verbose` for detailed error messages
