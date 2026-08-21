# Deploying this update

These files are a complete replacement for your current homepage — not a patch. Since your site is plain HTML/CSS/JS, this is a drag-and-drop swap:

1. **Back up your current `index.html`** somewhere, in case you want to compare or revert.
2. Upload `index.html`, `style.css`, `robots.txt`, and `sitemap.xml` to your site's root, replacing what's there now.
3. Export your rebuilt CV (the `.docx` from this chat) to PDF, name it **`Kennith-Crasta-CV.pdf`**, and upload it to the same root — this matches the download links already wired up in `index.html`. (Your current live CV is at a different filename with a space in it; once you upload the new one under the clean name, you can delete the old `Resume _KC.pdf`.)
4. Replace the hero photo: keep the same filename (`IMG-20241102-WA0028.jpg`) and it'll work immediately with no code changes, or swap in a new photo and update the two `src="..."` references in `index.html` (hero section + the Open Graph meta tag near the top of `<head>`) to match.
5. No build step, no dependencies — it's just static files. Google Fonts (IBM Plex family) load from a CDN link already in the `<head>`.

## What changed from your current site
- Added: Finance Systems & ERP section, a Featured Project case study (Oracle AGIS), a Certifications section — all previously missing.
- Fixed: the unverified "15%" and "cash management" claims are removed/softened; the ERP bullet now matches the stronger version on your CV; location and target roles are explicit above the fold.
- New visual design — a distinct, ledger/statement-inspired look (see the audit report for the reasoning). Your previous CSS wasn't accessible to me, so this is a fresh build rather than an edit of your existing styles.

## Still worth doing
- The `og:image` and hero photo currently point at the existing WhatsApp-export photo. Consider a proper compressed headshot when you have one.
- Add a real meta description / OG setup check on your other pages, if you add any beyond the homepage.
