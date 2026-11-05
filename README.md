# Universal Media Studio — Website

A static, single-file marketing and download page for **Universal Media Studio**, a Python desktop media utility built with PySide6 and QML.

The app itself lives at **https://github.com/mhhanzala12/UMS**. The page's download buttons link to that repository, and the "Download ZIP" link points to its `main` branch archive.

The whole site lives in `index.html` (HTML + CSS + vanilla JavaScript). There is no framework and no build step required.

## Host it on GitHub Pages

1. Create a new repository on GitHub (for example `media-studio-site`).
2. Upload `index.html` (and this `README.md`) to the root of the repository, or push them with git:

   ```bash
   git init
   git add index.html README.md
   git commit -m "Add Universal Media Studio website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo>.git
   git push -u origin main
   ```

3. On GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to *Deploy from a branch*.
5. Choose branch **`main`** and folder **`/ (root)`**, then click **Save**.
6. After a minute or two the site is live at:

   `https://<your-username>.github.io/<your-repo>/`

To update the site, edit `index.html`, commit, and push. GitHub Pages redeploys automatically.

## Local preview

Just open `index.html` in a browser, or run a tiny local server:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Notes

- All links are relative (`#anchors`), so the site works from a project page URL without changes.
- Fonts fall back to the system UI font, so no external requests are made.
- Respects `prefers-reduced-motion`.

## Responsible use

Download only media you own or are authorized to save. Spotify links are used for public metadata resolution only; the application does not use Spotify's authenticated Web API.
