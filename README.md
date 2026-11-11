# Wister Lim — personal portfolio website (Version 1)

Built with **HTML, CSS, vanilla JavaScript**, and data JSON files. No build step or paid package needed.

## Preview on your computer

Do not double-click `index.html`: browsers block local `fetch` of JSON content.

1. Unzip this folder.
2. Open a terminal in the `wister-website` folder.
3. Run `python -m http.server 8000` (Windows: `py -m http.server 8000`).
4. Open `http://localhost:8000` in Chrome.

For VS Code you can also use a local-server extension.

## What's included

- Homepage (EN / Simplified Chinese), responsive dark design
- Hover-to-advance personal photo slideshow (1 image/second; pauses on exit)
- Portfolio covers that play muted MP4 preview in place on hover, with reset when pointer leaves
- Portfolio project detail pages: `project.html?id=...`
- Service descriptions, About photos (static), testimonial images/videos
- Contact section (WhatsApp fallback until Tally is connected)
- `.pages.yml` for hosted Pages CMS, editing three JSON files, photos and videos

## Production deployment

1. Create a **GitHub repository**. It can be private, but enable Pages CMS GitHub App access to it.
2. Upload all **contents of this folder**, including hidden `.pages.yml` and `netlify.toml`.
3. Create Netlify site from the GitHub repository. Build command: **leave empty**. Publish directory: **`.`**.
4. Connect the same GitHub repository in https://app.pagescms.org/ (GitHub login and permission required).
5. Edit text, images and project entries in Pages CMS. Changes commit to GitHub; Netlify deploys automatically.
6. Create your Tally form and integrate it with Google Sheets and email notifications **inside Tally**.
7. Open Pages CMS → Website text, photos & links → set `tally_url` to your URL like `https://tally.so/r/xxxxxx`.
8. Test a real form submission, source/UTM tracking, notification and new Google Sheets row.

## Notes

- This ZIP is a complete **website code prototype**, not a deployed public website. No GitHub, Netlify, Pages CMS or Tally account has been configured or connected yet.
- The contact form is **not yet live** until you supply a Tally form URL. Until then the site visibly offers WhatsApp.
- User-submitted images/videos are optimized for web. Review and obtain publication permission before publicly posting testimonials or client work.
- English is default, Simplified Chinese available via top right toggle. Language preference is kept in this browser.
- Portfolio recordings are shortened web previews, not original master files. Keep originals on Google Drive.
- Text about roles/descriptions is **draft copy**. Check it carefully for factual accuracy before publishing.
- Changes to `data/*.json` are fetched when the page loads. A successful Pages CMS commit and Netlify redeploy are needed to publish updates.
- Pages CMS edits *content*, not the page layout code. Layout changes still require editing HTML/CSS/JS.
- Project IDs must be unique and use URL-friendly lowercase letters and hyphens.
- Home photo slideshow is triggered by hovering or click/tap. Project preview plays on hover, with a tap to preview on touch devices.

## Paths

`index.html` = homepage; `project.html` = project detail; `css/style.css` = theme; `js/site.js` = functionality; `data/site.json` = editable main content; `data/projects.json` = portfolio content; `data/testimonials.json` = feedback; `assets/` = optimized media.


## V2 Mobile Interaction Updates

- On desktop, hover a Portfolio screenshot to play its video in the same card. Leaving the card stops and resets the video. The project card and title still open its project detail page.
- On mobile and touchscreens, tap the **Tap to preview / 点击预览视频** button to play or stop the inline preview. Tap the screenshot or **View Project** link to navigate to the case study. Video stops when it scrolls off-screen or the tab becomes inactive.
- Portfolio cards and Services use gentle scroll-triggered fade/slide-up. Home text and photo area reveal once on touch devices.
- Home photo sequence: tap to start or pause on touchscreens; desktop hover to cycle.
- About Me photos never animate. Only the About text may reveal on scroll.
- Motion effects respect the visitor's `prefers-reduced-motion` setting.
- Desktop and mobile interactions should be tested on real devices before production launch.
