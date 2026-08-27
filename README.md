# Deploying this to kennithcrasta.com via GitHub

This folder is the entire site — everything needed is already inside it, nothing else to add before it can go live.

## Files
- `index.html`, `style.css` — the site
- `CVPIC01.jpg` — your photo, already resized/compressed for web (1.1MB → ~180KB, no visible quality loss). **When you get your professional photo taken, save it with this exact filename and it replaces the current one automatically — no code changes needed.**
- `Kennith-Crasta-CV.pdf` — your current CV, already linked from all three "Download CV" buttons
- `robots.txt`, `sitemap.xml` — basic SEO plumbing

## Steps
1. Create a new GitHub repository (or use your existing one for kennithcrasta.com).
2. Upload all the files in this folder to the repo root — drag-and-drop through GitHub's web UI works fine, no git command line required.
3. In the repo: **Settings → Pages → Deploy from a branch → main → / (root) → Save.**
4. In your domain registrar's DNS settings, point kennithcrasta.com at GitHub Pages (an A record to GitHub's IPs, or a CNAME if using a `www` subdomain — GitHub's Pages docs list the exact records). Add a `CNAME` file containing just `kennithcrasta.com` to the repo root if you want the apex domain to work.
5. Give DNS a little time to propagate, then check the live URL.

## When you get the new photo
Just replace `CVPIC01.jpg` in the repo with the new file, same filename. Commit, and it updates everywhere it's used (hero photo + social share preview) with no other changes.

## Design notes
Colors and type are all CSS variables at the top of `style.css` (`--paper`, `--ruled-line`, `--ink`, `--verified`, etc.) if you ever want to tweak the palette yourself. Fonts are IBM Plex Serif/Sans/Mono, loaded from Google Fonts in `index.html`.
