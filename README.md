# Google Play Screenshot Validator

A free, client-side tool that checks Google Play Store screenshots against
Google's size, aspect-ratio and format requirements, and can auto-fix
failed screenshots (pad or crop to a safe size) — all in the browser.
No upload, no login, no database.

## Files

- `index.html` — the full site: header, hero, validator, content sections
  (Requirements, How to Use, Common Errors, FAQ), and footer.
- `about.html`, `contact.html`, `privacy.html`, `terms.html` — static
  companion pages linked from the footer.
- `_page.css` — shared stylesheet for the four static pages above.
- `robots.txt`, `sitemap.xml` — basic SEO crawling files.

## Before you deploy

1. **Replace `https://example.com/`** with your real domain in:
   - `index.html` (`<link rel="canonical">`, `og:url`)
   - `about.html`, `contact.html`, `privacy.html`, `terms.html` (`<link rel="canonical">`)
   - `robots.txt` (Sitemap line)
   - `sitemap.xml` (every `<loc>`)
2. **Replace the placeholder email** in `contact.html`
   (`hello@example.com`) with your real support address.
3. Optional: add a real Open Graph image (`og:image` meta tag) sized
   1200×630px for nicer link previews on social media.
4. Optional: add a favicon file and a `<link rel="icon">` tag.

## Deploying

This is a fully static site — no build step, no server, no database.
Any static host works, for example:

- **Netlify / Vercel**: drag-and-drop this folder, or connect a Git repo.
- **GitHub Pages**: push this folder to a repo and enable Pages.
- **Any web server**: upload the files over FTP/SFTP to your web root.

## Notes on the "Download Fixed Image" feature

Inside Claude Artifacts, browser download prompts can be restricted, so
the app also offers "Open Fixed Image" (an in-page preview with a
"View Full Size" option) as a fallback. Once deployed to a real domain,
"Download Fixed Image" will trigger a normal file download in all
modern browsers — no changes needed.
