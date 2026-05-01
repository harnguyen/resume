# Resume Website

A clean, professional one-page resume website designed for GitHub Pages.

This version is a static site: no backend, no build step, and no database. Edit the content directly in `index.html`, adjust styling in `style.css`, and use `script.js` only for small interactions such as the mobile menu.

## Files

```text
index.html          Resume content and page structure
style.css           Responsive design and print styles
script.js           Mobile navigation behavior
assets/             Resume PDF, profile image, or other static assets
.github/workflows/  GitHub Pages deployment workflow
```

## Customize

Update these areas in `index.html`:

- Name, title, and summary in the hero section
- Email, phone, location, LinkedIn, GitHub, and portfolio links
- Work experience
- Skills
- Projects
- Education and certifications

The current button opens the browser print dialog so visitors can save the page as a PDF.

To use a downloadable PDF instead, add your PDF resume as:

```text
assets/resume.pdf
```

Then replace the `Save as PDF` button in `index.html` with:

```html
<a class="button button-secondary" href="./assets/resume.pdf" download>Download resume</a>
```

## Preview Locally

You can open `index.html` directly in a browser.

If you prefer a local server:

```bash
npx serve .
```

## Deploy To GitHub Pages

1. Push this folder to a GitHub repository.
2. Go to repository **Settings** -> **Pages**.
3. Set **Source** to **GitHub Actions**.
4. Push to `main` or `master`.
5. The workflow in `.github/workflows/deploy.yml` will publish the site.

Your URL will look like:

```text
https://your-github-username.github.io/your-repository-name/
```

## Notes

The old React/Vite files are still present in `src/` for reference, but the deployed GitHub Pages site now uses the static root files.
