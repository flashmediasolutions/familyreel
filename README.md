# FamilyReel website

The public pages for **FamilyReel: Scan & Slideshow**, the Mac App Store app from Flash Media Solutions, Inc.

- https://flashmediasolutions.github.io/familyreel/: the product page
- https://flashmediasolutions.github.io/familyreel/support/: support and FAQ (App Store support URL)
- https://flashmediasolutions.github.io/familyreel/privacy/: privacy policy (App Store privacy URL)
- https://flashmediasolutions.github.io/familyreel/compatibility/: scanner compatibility

**How the site is built:**

- Plain HTML and one stylesheet, served by GitHub Pages from `main` at the repo root.
- No build step.
- No scripts, web fonts, analytics or third-party requests. Every page carries a Content-Security-Policy that
  allows only this site's own CSS and images.
- Light and dark mode follow the system.

**Editing:**

- **The support email** appears once on the Support page and once on the Privacy page, and nowhere else. To change
  it, run `grep -rl support@flashmediasolutions.com .` and edit those two lines.
- **Speed numbers** (278 prints in 23 minutes, about 12 a minute with three scanners) come from a measured session.
  Change them only with a new measurement. The method is in the app repo's `store/research/throughput.md`.
- **When the app is live,** replace the "Coming soon to the Mac App Store" pill on the home page with Apple's
  official badge and the App Store link. Download the badge from Apple's Marketing Resources and host it in
  `assets/`; never hotlink it.
- **Screenshots** can join the home page once they're rendered from Demo Mode. Never use real family photos.
