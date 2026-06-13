# SparkleClean — Premium Cleaning Service Website

A stunning, conversion-focused single-page website for a professional home &
office cleaning company. Fresh cyan + clean-green theme, smooth animations, and
a booking flow designed to turn visitors into customers.

## Live Page

- **`index.html`** — the entire site. This is the only file you need to open.

## Features

- Fully responsive, single-file build (HTML + CSS + JS in one file — no build step)
- Sticky frosted-glass navigation with mobile hamburger menu
- Animated hero with floating soap-bubble effect and live trust badges
- Animated stat counters (cleans completed, rating, rebook rate)
- 6 service cards with hover lift + pricing
- "Why Us" trust section, 4-step "How It Works" process timeline
- 3-tier pricing table with a highlighted "Most Popular" plan
- Customer testimonials with star ratings
- Accordion FAQ
- Free-quote booking form with an instant success state (front-end demo, no backend)
- Scroll-reveal animations throughout

## Design System (from the UI/UX Pro Max skill)

- **Palette** — Cleaning Service: primary `#0891B2` (fresh cyan), CTA `#22C55E`
  (clean green), background `#ECFEFF`, text `#164E63`
- **Typography** — Poppins (headings) + Open Sans (body), the "Modern
  Professional" pairing
- **Conversion structure** — Hero → Social proof → Services → Why → Process →
  Pricing → Testimonials → FAQ → CTA/booking

## Tech / Dependencies

- Google Fonts — Poppins + Open Sans (loaded via CDN)
- Pure vanilla CSS + JavaScript — no frameworks, no libraries

## How to Run

No build step or server required. Just open the file in a browser:

```
index.html
```

Or serve locally:

```bash
# Python 3
python -m http.server 8000
# then visit http://localhost:8000/index.html
```

## Customizing

- **Company name / phone / email** — search `index.html` for `SparkleClean`,
  `(800) 555-0199`, and `hello@sparkleclean.com` and replace.
- **Services & prices** — edit the cards in the `#services` section and the
  `#pricing` table.
- **Testimonials / FAQ** — edit the `#reviews` and `#faq` sections directly.
- **Booking form** — currently a front-end demo; connect the `#bookForm`
  submit handler to your email service or CRM to receive real leads.

---

© 2026 SparkleClean. Premium home & office cleaning services.
