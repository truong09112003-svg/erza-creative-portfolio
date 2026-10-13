# ERZA Creative Portfolio

A responsive, static portfolio for Trường Nguyễn (Erza), built with HTML, CSS, and vanilla JavaScript. Project content lives separately in `js/projects.js` so it can be updated without changing the layout code.

## Current portfolio content

- Five selected graphic design projects and a portrait image are sourced from Erza's public Behance portfolio.
- The project details link to the original Behance page; descriptive text summarizes what is visible there.
- Video thumbnails and playback links still need to be added when Erza shares video assets.
- Contact email and other social links are left blank until Erza confirms what to publish.

Image assets are stored locally in `assets/images/`, so the site does not depend on remote image hosting.

## Update projects

Open `js/projects.js` and edit `window.ERZA_CONTENT`.

### Add a graphic design project

Add an object in `projects` with `title`, `category`, `year`, `image`, `context`, `objective`, `role`, `idea`, and `source`. Put the image in `assets/images/` and use its relative path. Use one of the existing category names or add a category to `designCategories`.

### Add video

Add an object to `videos` with `title`, `category`, `role`, `ratio`, and (when ready) a thumbnail and video URL. Current video cards open a details dialog but do not play media. To enable playback, add a real media URL and extend the dialog renderer in `js/main.js` to create a `<video controls preload="none">` or a consent-driven embed. Do not autoplay.

### Contact and social links

Set `email` to a verified address to activate both mailto links, each with a distinct subject. Add confirmed social URLs to `socials` if desired, then render those links in the footer. Empty values are intentionally not displayed as fake contact details.

## Run locally

Open `index.html` in a browser. For a local web server, run `python -m http.server 8000` from this folder, then visit `http://localhost:8000`.

## Publish with GitHub Pages

1. Add this folder to a GitHub repository and push the `index.html`, `css/`, `js/`, and `favicon.svg` files.
2. In repository **Settings → Pages**, choose **Deploy from a branch**.
3. Select the branch and `/ (root)` folder, then save.
4. Wait for the published URL and open it on mobile and desktop to check links and assets.

The site uses Google Fonts when online and falls back to local system sans-serif fonts. No build step, backend, database, or external image hosting is required.
