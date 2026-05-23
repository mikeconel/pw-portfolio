# Patrick Williams | Chartered Financial Planner & Financial Adviser

[![Website Status](https://img.shields.io/badge/status-live-success)](https://patrickwilliams.uk)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-purple)](https://getbootstrap.com/)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

A professional, recruiter-focused portfolio website for Patrick Williams – a Chartered Financial Planner with over 20 years of accountancy experience, now providing FCA-regulated investment and mortgage advice.

**Live site:** [https://patrickwilliams.uk](https://patrickwilliams.uk) *(replace with your actual domain)*

---

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [File Structure](#file-structure)
- [Installation & Setup](#installation--setup)
- [Customisation Guide](#customisation-guide)
- [Qualifications & Digital Badges](#qualifications--digital-badges)
- [FE Analytics Skills Page](#fe-analytics-skills-page)
- [Deployment to GitHub Pages](#deployment-to-github-pages)
- [Contact Form Setup](#contact-form-setup)
- [Changelog](#changelog)
- [Credits](#credits)
- [License](#license)

---

## Overview

This two-page portfolio website is designed to:

- Convert recruiters and employers visiting from LinkedIn or job applications
- Showcase Patrick's qualifications, honours, and technical skills with official digital badge imagery
- Provide a professional, trust-signalling digital presence
- Enable direct client enquiries via a bot-protected contact form
- Demonstrate FE Analytics proficiency through a dedicated, linked skills page

---

## Features

| Feature | Description |
|---------|-------------|
| **Responsive Design** | Fully mobile-friendly using Bootstrap 5 |
| **Interactive Navigation** | Hover + active colour states with smooth scroll |
| **Official Digital Badges** | Real PNG/JPG badge images for all LIBF, Money First Aid & FE Analytics certifications |
| **FE Analytics Skills Page** | Dedicated `fe-analytics.html` page listing 14 certified competencies across 4 categories |
| **Bot-Protected Contact Form** | Honeypot field + FormSubmit.co integration |
| **First-Person Copy** | Professional yet personal tone for client trust |
| **Lightweight** | No base64 bloat — all badge images served from `images/` folder (~28KB HTML) |
| **Live Links** | Aitana Financial Services + BIS Smart Digital Solutions |

---

## Tech Stack

- **HTML5** – Semantic markup across two pages
- **CSS3** – Custom styles + Bootstrap 5 utilities
- **Bootstrap 5.3** – Grid system, components, responsive layout
- **Bootstrap Icons 1.11** – Icon library
- **Google Fonts** – Inter + Playfair Display
- **JavaScript (Vanilla)** – Navigation active states, scroll spy, form validation
- **FormSubmit.co** – Serverless email endpoint (no backend required)

---

## File Structure

```
project-root/
├── index.html               # Main single-page CV / portfolio
├── fe-analytics.html        # FE Analytics certified skills detail page
├── README.md
└── images/
    ├── CeMAP_Professional.png
    ├── Certified_Mortgage_Adviser.png
    ├── Certified_Practitioner_In_Specialist_Property_Finance.png
    ├── Certified_Money_First_Aider_logo.png
    ├── Chartered_Financial_Adviser_LIBF.png
    └── FE_Analytics_Certified_2026.jpg
```

---

## Installation & Setup

No build tools or dependencies required. This is a static site.

**1. Clone the repository**

```bash
git clone https://github.com/your-username/patrick-williams-cv.git
cd patrick-williams-cv
```

**2. Open locally**

Simply open `index.html` in any modern browser. Because badge images use relative paths, both HTML files must be opened from the same folder — not as isolated files.

```bash
# macOS / Linux
open index.html

# Or use a local dev server (recommended to avoid CORS on some browsers)
npx serve .
# or
python3 -m http.server 8000
```

**3. Deploy**

Upload all files (both HTML files + the `images/` folder) to your web host. See [Deployment](#deployment-to-github-pages) below.

---

## Customisation Guide

### Personal details

All contact information is in `index.html`. Search for the following and update:

| Placeholder | Location |
|-------------|----------|
| `07432604830` | Hero section + Contact section |
| `patrickwilliams5@yahoo.co.uk` | Contact section + FormSubmit action URL |
| `London, United Kingdom` | Hero section + Contact section |
| `https://patrickwilliams.uk` | Update README shields + any meta tags |

### Profile photo

Replace the placeholder icon in the hero section with a real photo:

```html
<!-- Find this block and replace with an <img> tag -->
<div class="profile-img-placeholder mx-auto">
  <i class="bi bi-person-bounding-box" style="font-size: 4rem;"></i>
</div>
```

Replace with:

```html
<img src="images/profile-photo.jpg" alt="Patrick Williams"
     style="width:140px;height:140px;border-radius:50%;object-fit:cover;
            box-shadow:0 15px 30px rgba(0,0,0,0.1);">
```

### Colours

The colour palette is defined via inline CSS variables at the top of each HTML file:

| Variable / Value | Usage |
|-----------------|-------|
| `#0a2540` | Navy — primary brand colour |
| `#d4af37` | Gold — accent colour |
| `#f8fafc` | Off-white — page background |

---

## Qualifications & Digital Badges

Badge images live in the `images/` folder and are referenced by relative path. Each badge is assigned to its matching qualification card in the **Education & Professional Designations** section of `index.html`.

| Badge Image | Qualification | Card |
|-------------|--------------|------|
| `Chartered_Financial_Adviser_LIBF.png` | Level 6 Diploma in Advanced Financial Advice | LIBF · May 2024 |
| `CeMAP_Professional.png` | Certificate in Mortgage Advice & Practice (CeMAP) | LIBF · Sept 2024 |
| `Certified_Mortgage_Adviser.png` | Certificate in Mortgage Advice & Practice (CeMAP) | LIBF · Sept 2024 |
| `Certified_Practitioner_In_Specialist_Property_Finance.png` | Certified Practitioner in Specialist Property Finance (CPSP) | LIBF · April 2026 |
| `Certified_Money_First_Aider_logo.png` | Money First Aid Certificate | Money First Aid · Jan 2026 |
| `FE_Analytics_Certified_2026.jpg` | Certified FE Analytics User | FE Analytics Academy · May 2026 |

The FE Analytics badge appears in three locations — the hero paragraph, the About section checklist, and the credentials card — and in all three cases links through to `fe-analytics.html`.

---

## FE Analytics Skills Page

`fe-analytics.html` is a standalone page matching the design of `index.html`. It is reached by clicking any FE Analytics badge on the main page.

It documents 14 certified competencies across four categories:

**Portfolio & Fund Analysis**
- Portfolio creation and management
- Fund, portfolio and sector filtering analysis
- Fund diversification and correlation tables

**Risk & Return Analytics**
- Risk v Return Scatter graphs
- ATR & CFL analysis
- FE risk score charts

**Client Comparison & Reporting**
- Recommended portfolio v existing portfolio analysis
- Investment v cash savings analysis
- Fund and platform charges comparator
- Discrete v Rolling performance bar charts
- Market movement analysis report

**Planning & Modelling**
- Investment forecasting
- CashCalc integration via FE Analytics
- Cashflow modelling

The page includes a stats strip (14 competencies, 4 categories, certification date), an "Applied in Practice" section, and navigation back to `index.html`.

---

## Deployment to GitHub Pages

**1. Push your repository to GitHub**

```bash
git init
git add .
git commit -m "Initial commit – Patrick Williams CV site"
git remote add origin https://github.com/your-username/patrick-williams-cv.git
git push -u origin main
```

**2. Enable GitHub Pages**

- Go to your repository → **Settings → Pages**
- Under **Source**, select `main` branch and `/ (root)` folder
- Click **Save**

GitHub Pages will serve `index.html` automatically from the root. Your site will be live at:
`https://your-username.github.io/patrick-williams-cv/`

**3. Custom domain (optional)**

Add a `CNAME` file to the repo root containing just your domain:

```
patrickwilliams.uk
```

Then point your domain's DNS to GitHub Pages as per [GitHub's documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

---

## Contact Form Setup

The contact form uses [FormSubmit.co](https://formsubmit.co) — no server-side code required.

**Current configuration** (in `index.html`):

```html
<form action="https://formsubmit.co/patrickwilliams5@yahoo.co.uk" method="POST">
  <input type="text"   name="_honey"    style="display:none">       <!-- Bot trap -->
  <input type="hidden" name="_captcha"  value="false">
  <input type="hidden" name="_subject"  value="New enquiry from Patrick Williams Portfolio">
  ...
</form>
```

**First use:** FormSubmit.co will send a one-time confirmation email to the address in the `action` URL. Click the confirmation link to activate form submissions.

**To change the recipient email**, update the `action` attribute value.

---

## Changelog

### May 2026 — Claude updates
- Added three new qualifications: Money First Aid Certificate (Jan 2026), Certified Practitioner in Specialist Property Finance / CPSP (April 2026), Certified FE Analytics User (May 2026)
- Replaced all inline base64 badge images with external file references in `images/` folder (HTML size reduced from ~291KB to ~28KB)
- Swapped SVG placeholder badges for official PNG/JPG digital badge images from LIBF, Money First Aid and FE Analytics Academy
- Added `Chartered_Financial_Adviser_LIBF.png` badge to the Level 6 DipFA card
- Added both `CeMAP_Professional.png` and `Certified_Mortgage_Adviser.png` badges to the CeMAP card
- Replaced FE Analytics Bootstrap modal with a dedicated `fe-analytics.html` skills page
- FE Analytics badge now links to `fe-analytics.html` from three locations: hero, About section, and credentials card
- Built `fe-analytics.html`: full skills page with hero banner, 14 skill cards across 4 categories, stats strip, and "Applied in Practice" section

### Initial build — DeepSeek
- Single-page responsive portfolio (`index.html`)
- Navy/gold brand palette with Playfair Display + Inter typography
- Sections: Hero, About / Professional Profile, Education & Designations, Career Experience, Technical Skills, Contact
- Bot-protected contact form via FormSubmit.co
- Honours & Awards card, Professional Memberships
- Interactive navigation with scroll-spy active states

---

## Credits

- **Design & development:** [BIS Smart Digital Solutions](http://217.154.38.190/)
- **Framework:** [Bootstrap 5](https://getbootstrap.com/)
- **Icons:** [Bootstrap Icons](https://icons.getbootstrap.com/)
- **Fonts:** [Google Fonts](https://fonts.google.com/) — Inter & Playfair Display
- **Contact form:** [FormSubmit.co](https://formsubmit.co/)
- **Digital badges:** LIBF, Money First Aid, FE Analytics Academy

---

## License

MIT License — free to use and adapt with attribution.

```
Copyright (c) 2026 Patrick Williams / BIS Smart Digital Solutions
```
