# LuxeEstate — Premium Real Estate Website

A single-page luxury real estate website with a dark gold theme, 3D visuals,
smooth scroll animations, and an in-page property detail view.

## Live Pages

- **`luxeestate.html`** — the main site. This is the file to open.
- **`property-details.html`** — the original standalone detail page (now merged
  into the main site; kept as a fallback / reference).

## Features

- Fully responsive, single-file build (HTML + CSS + JS in one file)
- Animated hero with a Three.js 3D scene
- Interactive, draggable 3D building model
- GSAP scroll reveals and animated stat counters
- Property filtering (For Sale / For Rent / Luxury / Commercial)
- Auto-playing testimonial carousel
- **In-page property detail view** — clicking "View Details" opens a full
  property page instantly without a reload, with:
  - Deep linking (`luxeestate.html?property=manhattan`)
  - Browser **Back** button support
  - **Esc** key to close
  - Image gallery, video tours, 3D model, and Google Maps location
- Booking + newsletter forms (front-end demo, no backend)
- Floating WhatsApp contact button

## Tech / Dependencies (loaded via CDN)

- [Three.js](https://threejs.org/) r128 — 3D scenes
- [GSAP](https://greensock.com/gsap/) 3.12 + ScrollTrigger — animations
- [Font Awesome](https://fontawesome.com/) 6.4 — icons
- Google Fonts — Playfair Display + Inter

## How to Run

No build step or server required. Just open the file in a browser:

```
luxeestate.html
```

Or, to serve locally (recommended so the videos/maps load reliably):

```bash
# Python 3
python -m http.server 8000
# then visit http://localhost:8000/luxeestate.html
```

## Project Structure

```
luxeestate.html        # main site (open this)
property-details.html  # original detail page (reference/fallback)
assets/                # css/ and js/ folders for future split-out
README.md
```

## Notes

- All property data lives in the `properties` object inside `luxeestate.html`.
  To add or edit a listing, update that object and add a matching
  `<article class="property-card">` with a `data-property` link.
- The site uses the native OS cursor for smooth, normal pointer behavior.

---

© 2026 LuxeEstate. Premium real estate services across the United States.
