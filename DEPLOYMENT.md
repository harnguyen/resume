# Deployment Guide

This resume website is a static GitHub Pages site. It deploys the repository root directly, so there is no build command required.

## GitHub Pages Deployment

1. Create a GitHub repository, for example `resume`.
2. Push this folder to GitHub:

   ```bash
   git init
   git add .
   git commit -m "Create resume website"
   git branch -M main
   git remote add origin https://github.com/yourusername/resume.git
   git push -u origin main
   ```

3. In GitHub, open the repository settings.
4. Go to **Pages**.
5. Under **Build and deployment**, choose **GitHub Actions**.
6. Pushes to `main` or `master` will run `.github/workflows/deploy.yml`.

The website will be available at:

```text
https://yourusername.github.io/resume/
```

## Manual Branch Deployment Alternative

If you do not want GitHub Actions:

1. Open repository **Settings** -> **Pages**.
2. Choose **Deploy from a branch**.
3. Select branch `main`.
4. Select folder `/root`.
5. Save.

## Custom Domain

1. Add a file named `CNAME` at the repository root.
2. Put only your domain inside it, for example:

   ```text
   yourdomain.com
   ```

3. In your DNS provider, point the domain to GitHub Pages.
4. Enable **Enforce HTTPS** in GitHub Pages settings after DNS is ready.

## Resume PDF

The website currently lets visitors save the page as a PDF through the browser print dialog.

To provide a separate downloadable resume file, add it here:

```text
assets/resume.pdf
```

Then update the button in `index.html` to point to that file.
