# handytuner-site — notes for AI agents

- The HandyTuner website: one self-contained `index.html` (CSS and images inlined) served by GitHub Pages from `main`. A push to `main` is live within a minute; there is no staging.
- Run `git fetch` before editing; the site is sometimes edited from elsewhere.
- `index.html` is several MB of base64 images. Never print or read it whole; search it, or strip `data:image/...` when reading.
- When swapping a screenshot, keep the original `width`/`height` and wrapper elements (like `<span class="dash">`); the layout depends on them.
- Before pushing, render the page at desktop and phone width and look at it, e.g. `chromium --headless=new --window-size=1440,1000 --screenshot=out.png file://$PWD/index.html`.
- The download count comes live from the GitHub API; never hardcode it.
- When HandyTuner ships a release, update the version, size and date line (`.release-meta`).
- American spelling in all on-screen text.
- Never force-push `main`.
