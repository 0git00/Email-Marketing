# GitHub Pages Deployment

Repository: `Emil-Marketing` under account `0git00`. Live URL: https://0git00.github.io/Emil-Marketing/

1. Unzip `updated-site.zip`; open the `site` folder.
2. Back up the current repo first (download ZIP from GitHub or keep `original-backup.zip`).
3. In GitHub, open the `Emil-Marketing` repo > **Add file > Upload files**.
4. Drag in **everything inside** `site`: `index.html`, `sitemap.xml`, `robots.txt`, `site.webmanifest`, `404.html`, `favicon.ico`, `.nojekyll` and the `assets` folder. (Hidden file `.nojekyll`: if your computer hides it, skip it; the site still works.)
5. Commit to the main branch.
6. **Settings > Pages**: source = "Deploy from a branch", branch `main`, folder `/ (root)`.
7. Wait 1–3 minutes, then check:
   - https://0git00.github.io/Emil-Marketing/
   - https://0git00.github.io/Emil-Marketing/sitemap.xml
   - https://0git00.github.io/Emil-Marketing/robots.txt
   - https://0git00.github.io/Emil-Marketing/assets/og-image.jpg
8. Test the contact form once (FormSubmit sends an activation email the first time).
9. Share the link in a chat to see the preview image. Platforms cache previews, so retry later if the old one shows.

Note: `robots.txt` only works at the domain root of a host. On a project page like `/Emil-Marketing/robots.txt`, crawlers do not read it as the site's robots file (they look at `0git00.github.io/robots.txt`). It is harmless, and the sitemap is still discoverable by other means (profile links, Bing Webmaster Tools).
