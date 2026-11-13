# Wister Lim — V4 Editorial Portfolio

Full static site for Netlify, GitHub and Pages CMS. English and Simplified Chinese.

## Updates in V4
- New `IMG_1509.jpg` is first in the interactive hero. Existing hero photos follow.
- **Soft-edge CSS image masks** on portrait images with a bottom fade. This does not constitute a pixel-accurate subject-only cutout. For a fully transparent cutout, replace the photos with transparent PNG/WebP assets using Pages CMS.
- Hero name kept in its own text lane to prevent portrait obscuring critical letters.
- Equal-width, 16:10 portfolio frames; in-place hover video previews and mobile tap previews.
- Portfolio category tabs: Website, Automation, SEO, Carousels, Video Editing. Empty categories display an intentional Coming Soon state.
- Eight bilingual services with industry examples.
- Rolling tools bar with platforms used by Wister.
- Two designed video testimonial poster images, aligned testimonials and compact contact CTA.
- Existing `.pages.yml`, `data/`, and `assets/` remain editable through Pages CMS after GitHub integration.

## Deploy
Update the existing GitHub repo with changed files, preserving folders. Netlify uses `publish = .` with no build command. To test locally: `python -m http.server 8000` in the project folder and open http://localhost:8000.

## Updated files
`index.html`, `css/style.css`, `js/site.js`, `data/site.json`, `data/testimonials.json`, `.pages.yml`, `README.md`; plus `assets/images/img_1509.webp` and two `assets/images/testimonial-video-*-poster.webp` files.

## Notes
- Tally remains unconnected until its real form URL is saved in `data/site.json` / Pages CMS.
- No paid services or false project claims are included.
- Test mobile and desktop after Netlify deployment before making the site public.


## V4.1 corrections
- Hero, including default photo, is unchanged.
- Work preview image and video use matching 16:10 containers.
- Service rows have no decorative clickable-looking arrows.
- Written client feedback is shown full-size using contain on off-white/white backgrounds.
- Video feedback 02 has a newly composed cover with the complete face visible.
- Social links reorder Instagram/TikTok/Threads and LinkedIn/X/Facebook in a tidy grid.
