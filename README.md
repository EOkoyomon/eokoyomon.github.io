# My Personal Website :)

This is the source code for my personal website, built with [Hugo](https://gohugo.io/) and hosted on [GitHub Pages](https://pages.github.com/).

---

## 🛠️ Local Development

To preview the site locally:

1. Install Hugo (if not already installed)

   ```bash
   brew install hugo       # macOS
   sudo apt install hugo   # Ubuntu/Debian
   ```

2. Start the development server

   ```bash
   hugo server -D
   ```
   - -D includes drafts and unpublished content.
   - Site is live at: http://localhost:1313

## 🚀 Deployment (via GitHub Actions)

Deployment is handled automatically by GitHub Actions. You can find the deployment workflow in:
   ```bash
   .github/workflows/hugo.yml
   ```

### Make a Change and Deploy

1. Make your changes (e.g. edit content, add files)
   
2. Commit and push:
    ```bash
    git add .
    git commit -m "Update site content"
    git push origin main
    ```

3. GitHub Actions will automatically build and deploy the site within a minute or two.

## 📁 Hosting Static Files (e.g., PDFs)

1. Place downloadable files like preprints in `static/`, for example:
    ```bash
    static/files/my-paper-preprint.pdf
    ```

2. The file will be publicly accessible at:
    ```bash
    https://eokoyomon.github.io/files/my-paper-preprint.pdf
    ```

## 🤖 Controlling Indexing (robots.txt)

1. Create or edit static/robots.txt:

    ```bash
    User-agent: *
    Disallow: /publications/
    Disallow: /files/my-paper-preprint.pdf
    ```

2. To allow indexing later, just remove those lines and push again.