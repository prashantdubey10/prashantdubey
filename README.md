# 🔱 Pt. Prashant Dubey — Vedic Astrology Website

[![Live Site](https://img.shields.io/badge/Live%20Site-prashantdubey.co.in-8B1A1A?style=flat-square&logo=googlechrome&logoColor=white)](https://www.prashantdubey.co.in/)
[![License](https://img.shields.io/badge/License-Proprietary-F0A04A?style=flat-square)](#license)
[![GitHub Pages](https://img.shields.io/badge/Hosted%20on-GitHub%20Pages-181717?style=flat-square&logo=github&logoColor=white)](https://pages.github.com/)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)

> **Pt. Prashant Kumar Dubey** — India's most trusted Vedic astrologer, based in Varanasi (Kashi), with 26+ years of experience in Jyotish, Numerology, Vastu Shastra, Palmistry, and Kundli reading. Serving 50,000+ clients across 15 countries.

---

## 📑 Table of Contents

- [About](#about)
- [Features](#features)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Deployment](#deployment)
- [SEO & Performance](#seo--performance)
- [File Reference](#file-reference)
- [Contact](#contact)
- [License](#license)

---

## About

This is the official website for **Pandit Prashant Dubey**, a Varanasi-based Vedic astrologer and recipient of the *Yuva Pratibha Award* by the Akhil Bharatiya Vidvat Parishad, Kashi. The site is a fully static, single-page application built with pure HTML5, CSS3, and vanilla JavaScript — no frameworks, no dependencies, no build step required.

### Services Offered

| Service | Starting Price |
|---|---|
| Quick Guidance (First Question) | ₹ 550 |
| Numerology Reading | ₹ 2,000 |
| Natal Chart / Kundli Reading | ₹ 2,500 |
| Palmistry & Face Reading | ₹ 2,500 |
| Predictive Astrology | ₹ 3,200 |
| Vastu Shastra Consultation | ₹ 3,500 |
| Synastry & Matchmaking | ₹ 3,800 |
| Vedic Jyotish Consultation | ₹ 4,000 |

---

## Features

- ⚡ **Zero dependencies** — Pure HTML/CSS/JS, loads in under 1 second
- 🌐 **Bilingual** — Full English ↔ Hindi toggle (i18n via JS object map)
- 📱 **Fully responsive** — Mobile-first design, tested on iOS/Android/tablet/desktop
- 🎠 **Puja Gallery Carousel** — Touch/swipe/keyboard/mouse-drag, auto-plays, pauses on hover
- 🔱 **Dakshina section** — UPI QR, real app logos (Google Pay, PhonePe, Paytm, BHIM), bank details, international devotee support
- 🎥 **YouTube integration** — Lazy-loaded video embeds
- 📅 **Booking form** — Typeform integration
- 🗺️ **Google Maps embed** — Varanasi location
- 🔍 **Advanced SEO** — Schema.org structured data (Person, LocalBusiness, FAQPage, BreadcrumbList, WebSite), Open Graph, Twitter Card, Geo meta tags
- 🤖 **AEO-ready** — AI Overview optimised with FAQPage schema and LLM crawler access in `robots.txt`
- 🌑 **Dark announcement bar** — Dismissable, bilingual
- 🏆 **Trust bar** — Social proof strip with key stats
- ♿ **Accessible** — Semantic HTML5, ARIA labels, keyboard navigation

---

## Project Structure

```
prashantdubey.co.in/
│
├── index.html              # Main site (single-page application)
├── robots.txt              # Crawler directives + sitemap reference
├── sitemap.xml             # XML sitemap (generate separately)
├── manifest.json           # PWA web app manifest
├── 404.html                # Custom 404 error page
├── .nojekyll               # Prevents GitHub Pages Jekyll processing
├── .gitignore              # Git exclusions
├── .travis.yml             # CI/CD pipeline (Travis CI)
├── LICENSE.MD              # Proprietary licence
├── README.md               # This file
├── pom.xml                 # Maven project descriptor (for Java tooling)
├── nbactions.xml           # NetBeans IDE Maven action bindings
│
└── images/
    ├── hero.jpg            # Hero / OG cover image (1200×630)
    ├── og-cover.jpg        # Open Graph cover
    ├── favicon-32.png      # Favicon 32×32
    ├── favicon-16.png      # Favicon 16×16
    ├── apple-touch-icon.png
    ├── puja-temple.webp    # Gallery slide 1 (temple puja)
    ├── puja-havan.webp     # Gallery slide 2 (home havan)
    └── puja-vivah.webp     # Gallery slide 3 (wedding ceremony)
```

---

## Getting Started

No build tools, no npm, no compilation required.

### Local Development

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/prashantdubey-astrology.git
cd prashantdubey-astrology

# Serve locally (any static server works)
npx serve .
# or
python3 -m http.server 8080
# or simply open index.html in your browser
```

### Before Going Live

1. **Replace UPI ID** — Search for `prashantdubey@upi` in `index.html` and update to the real UPI ID
2. **Replace QR code** — Swap the SVG placeholder in the Dakshina section with an actual UPI QR image
3. **Bank details** — Fill in `XXXX XXXX XXXX` account number and `XXXXXXXX` IFSC code
4. **Telephone number** — Add phone number to the `LocalBusiness` schema and contact section
5. **Gallery images** — Place puja photos as `images/puja-temple.webp`, `images/puja-havan.webp`, `images/puja-vivah.webp`
6. **OG image** — Add `images/og-cover.jpg` (1200×630px) for social sharing previews
7. **Hero image** — Add `images/hero.jpg` for the homepage and schema
8. **Sitemap** — Generate and upload `sitemap.xml` referencing `https://www.prashantdubey.co.in/`

---

## Deployment

### GitHub Pages (Recommended)

```bash
# Push to main branch — GitHub Pages serves from root
git add .
git commit -m "deploy: update site"
git push origin main
```

Enable Pages in **Settings → Pages → Source: Deploy from branch → main / root**.

The `.nojekyll` file in the root prevents GitHub from running Jekyll, which ensures files starting with `_` and paths with special characters are served correctly.

### Custom Domain

Set your custom domain in **Settings → Pages → Custom domain**: `www.prashantdubey.co.in`

Add a `CNAME` file at the repository root:

```
www.prashantdubey.co.in
```

Then add these DNS records at your registrar:

| Type | Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | YOUR_USERNAME.github.io |

### Travis CI (Automated Deploy)

See `.travis.yml` — pushes to `main` auto-deploy to GitHub Pages via the `pages` provider.

---

## SEO & Performance

### Structured Data Implemented

| Schema Type | Purpose |
|---|---|
| `Person` | AEO — AI Overviews, Knowledge Panel |
| `LocalBusiness` | Google Maps, local search |
| `FAQPage` | Featured Snippets, People Also Ask |
| `WebSite` | Sitelinks search box |
| `BreadcrumbList` | Rich breadcrumbs in SERPs |

### Performance Tips

- Images should be compressed WebP (use [Squoosh](https://squoosh.app/))
- Hero image: max 150 KB, 1200×800px
- Add `loading="lazy"` to below-fold images (already done)
- Enable Gzip/Brotli compression at the server/CDN level
- Consider Cloudflare for CDN + HTTPS + DDoS protection

### Core Web Vitals Targets

| Metric | Target |
|---|---|
| LCP (Largest Contentful Paint) | < 2.5 s |
| FID / INP | < 100 ms |
| CLS (Cumulative Layout Shift) | < 0.1 |

---

## File Reference

| File | Purpose |
|---|---|
| `robots.txt` | Controls crawler access; references sitemap; blocks scrapers |
| `.nojekyll` | Disables Jekyll on GitHub Pages |
| `404.html` | Branded custom error page with navigation back to home |
| `.gitignore` | Excludes OS files, editor configs, build artefacts |
| `.travis.yml` | CI pipeline: lint → test → deploy to GitHub Pages |
| `LICENSE.MD` | All rights reserved — proprietary content |
| `pom.xml` | Maven descriptor for Java-based tooling / build automation |
| `nbactions.xml` | NetBeans IDE Maven action bindings |

---

## Contact

**Pandit Prashant Kumar Dubey**
📍 Varanasi (Kashi), Uttar Pradesh, India — 221001
📧 [prashant.dubey10@outlook.com](mailto:prashant.dubey10@outlook.com)
🌐 [www.prashantdubey.co.in](https://www.prashantdubey.co.in/)
▶️ [YouTube — Shastri Ji Kashivale](https://www.youtube.com/@ShastriJiKashivale235)

---

## License

© 2026 Pt. Prashant Dubey Astrology. All rights reserved.

All content, code, images, and intellectual property on this website are the exclusive property of Pandit Prashant Kumar Dubey. Reproduction, redistribution, or use of any part of this website without prior written permission is strictly prohibited. See [LICENSE.MD](LICENSE.MD) for full terms.
