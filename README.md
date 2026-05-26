# Patrick Williams | Chartered Financial Planner & Financial Adviser

[![Website Status](https://img.shields.io/badge/status-live-success)](https://patrickwilliams.uk)
[![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-purple)](https://getbootstrap.com/)
[![Pages](https://img.shields.io/badge/pages-8-blue)](#file-structure)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)

A professional, recruiter-focused portfolio website for Patrick Williams – a Chartered Financial Planner with over 20 years of experience in accounting and financial systems, now providing FCA-regulated investment and mortgage advice at Aitana Financial Services.

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
- [Qualification Detail Pages](#qualification-detail-pages)
- [FE Analytics Skills Page](#fe-analytics-skills-page)
- [Deployment to GitHub Pages](#deployment-to-github-pages)
- [Contact Form Setup](#contact-form-setup)
- [Changelog](#changelog)
- [Credits](#credits)
- [License](#license)

---

## Overview

This multi-page portfolio website is designed to:

- Convert recruiters and employers visiting from LinkedIn or job applications
- Showcase Patrick's qualifications, honours, and technical skills with official digital badge imagery
- Provide a professional, trust-signalling digital presence with a dedicated page per qualification
- Enable direct client enquiries via a bot-protected contact form
- Demonstrate FE Analytics proficiency through a dedicated linked skills page

---

## Features

| Feature | Description |
|---------|-------------|
| **Responsive Design** | Fully mobile-friendly using Bootstrap 5 |
| **Interactive Navigation** | Hover + active colour states with smooth scroll |
| **Official Digital Badges** | Real PNG/JPG badge images for all LIBF, Money First Aid & FE Analytics certifications |
| **7 Qualification Detail Pages** | Each badge links to a dedicated page with skills, competencies and qualification info |
| **Bot-Protected Contact Form** | Honeypot field + FormSubmit.co with `_next` redirect and phone field |
| **First-Person Copy** | Professional yet personal tone for client trust |
| **Lightweight** | No base64 bloat — all badge images served from `images/` folder (~29KB main HTML) |
| **Live Links** | Aitana Financial Services + BIS Smart Digital Solutions |

---

## Tech Stack

- **HTML5** – Semantic markup across 8 pages
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
├── index.html                    # Main single-page CV / portfolio
├── fe-analytics.html             # FE Analytics certified skills detail page
├── level6-dip.html               # Level 6 DipAFA skills page
├── level4-dip.html               # Level 4 Diploma (R01-R06) skills page
├── cemap.html                    # CeMAP mortgage skills page
├── equity-release.html           # Certificate in Regulated Equity Release page
├── cpsp.html                     # CPSP specialist property finance page
├── money-first-aid.html          # Certified Money First Aider skills page
├── README.md
└── images/
    ├── CeMAP_Professional.png                              # Used on CeMAP, Equity Release & Level 4 cards
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

Because badge images use relative paths, all HTML files must be opened from the same folder. Use a local dev server:

```bash
# Python (built-in)
python3 -m http.server 8000

# Or Node
npx serve .
```

Then open `http://localhost:8000` in your browser.

**3. Deploy**

Upload all 8 HTML files and the `images/` folder to your web host. See [Deployment](#deployment-to-github-pages) below.

---

## Customisation Guide

### Personal details

All contact information is in `index.html`. Search for the following and update:

| Placeholder | Location |
|-------------|----------|
| `07432604830` | Hero section + Contact section |
| `patrickwilliams5@yahoo.co.uk` | Contact section + FormSubmit action URL |
| `London, United Kingdom` | Hero section + Contact section |
| `https://patrickwilliams.uk` | `_next` hidden field in form + README shields |

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

| Value | Usage |
|-------|-------|
| `#0a2540` | Navy — primary brand colour |
| `#d4af37` | Gold — accent colour |
| `#f8fafc` | Off-white — page background |

---

## Qualifications & Digital Badges

Badge images live in the `images/` folder. Each badge is a clickable link on `index.html` navigating to that qualification's detail page.

| Badge Image | Qualification | Links To |
|-------------|--------------|----------|
| `Chartered_Financial_Adviser_LIBF.png` | Level 6 Diploma in Advanced Financial Advice · LIBF · May 2024 | `level6-dip.html` |
| `CeMAP_Professional.png` | Level 4 Diploma for Professional Financial Advisers · CBI · Mar 2024 | `level4-dip.html` |
| `CeMAP_Professional.png` + `Certified_Mortgage_Adviser.png` | Certificate in Mortgage Advice & Practice (CeMAP) · LIBF · Sept 2024 | `cemap.html` |
| `CeMAP_Professional.png` | Certificate in Regulated Equity Release · LIBF · Nov 2024 | `equity-release.html` |
| `Certified_Practitioner_In_Specialist_Property_Finance.png` | Certified Practitioner in Specialist Property Finance (CPSP) · LIBF · April 2026 | `cpsp.html` |
| `Certified_Money_First_Aider_logo.png` | Money First Aid Certificate · Jan 2026 | `money-first-aid.html` |
| `FE_Analytics_Certified_2026.jpg` | Certified FE Analytics User · FE Analytics Academy · May 2026 | `fe-analytics.html` |

---

## Qualification Detail Pages

Each qualification has a standalone detail page built to the same navy/gold design as the main site. Every page includes a hero banner with cert-pill and badge image, a stats strip, categorised skill cards, an about section with sidebar, and back-navigation to `index.html`.

| Page | Qualification | Categories | Skills |
|------|--------------|-----------|--------|
| `level6-dip.html` | Level 6 DipAFA — LIBF | Advanced Planning, Estate Planning, Regulatory & Ethics | 9 |
| `level4-dip.html` | Level 4 Diploma — Chartered Banker Institute | Regulation, Investment & Risk, Pensions, Practice | 6 (R01–R06) |
| `cemap.html` | CeMAP — LIBF | UK Financial Services, Mortgages, Assessment | 8 |
| `equity-release.html` | Certificate in Regulated Equity Release — LIBF | Products, Client Suitability, Regulation | 9 |
| `cpsp.html` | CPSP — LIBF | Bridging Finance, Development Finance, Commercial | 9 |
| `money-first-aid.html` | Certified Money First Aider® | Wellbeing Awareness, Support & Signposting, Integration | 9 |
| `fe-analytics.html` | Certified FE Analytics User — FE Analytics Academy | Portfolio Analysis, Risk & Return, Reporting, Modelling | 14 |

---

## FE Analytics Skills Page

`fe-analytics.html` documents 14 certified competencies across four categories:

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

> **Note:** While ConcertHub is the platform applied daily for the full 6-step advice process at Aitana Financial Services, FE Analytics has been mastered to a high level through exams and extensive practical case studies.

---

## Deployment to GitHub Pages

**1. Push your repository to GitHub**

```bash
git init
git add .
git commit -m "Initial commit - Patrick Williams CV site"
git remote add origin https://github.com/your-username/patrick-williams-cv.git
git push -u origin main
```

**To update an existing repo** (add new files and changes):

```bash
git add .
git commit -m "Add qualification detail pages and badge updates"
git push origin main
```

**2. Enable GitHub Pages**

- Go to your repository → **Settings → Pages**
- Under **Source**, select `main` branch and `/ (root)` folder
- Click **Save**

Your site will be live at: `https://your-username.github.io/patrick-williams-cv/`

**3. Custom domain (optional)**

Add a `CNAME` file to the repo root containing just your domain:

```
patrickwilliams.uk
```

Then point your domain DNS to GitHub Pages per [GitHub's documentation](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

---

## Contact Form Setup

The contact form uses [FormSubmit.co](https://formsubmit.co) — no backend required.

**Current configuration** (in `index.html`):

```html
<form action="https://formsubmit.co/patrickwilliams5@yahoo.co.uk" method="POST">
  <input type="text"   name="_honey"    style="display:none">
  <input type="hidden" name="_captcha"  value="false">
  <input type="hidden" name="_subject"  value="New enquiry from Patrick Williams Portfolio">
  <input type="hidden" name="_next"     value="https://patrickwilliams.uk/index.html">
  <input type="hidden" name="_template" value="table">
  <!-- Fields: Full name, Phone (optional), Email, Message -->
</form>
```

**Fields collected:** Full name, phone number (optional), email, message.

**First use:** FormSubmit.co sends a one-time confirmation email to the recipient address. Click the link to activate submissions before going live.

**To change the recipient**, update both the `action` URL and the `_next` value.

---

## Changelog

### May 2026 — Session 3 (Claude)
- Updated Professional Profile text to new version
- `fe-analytics.html` "Applied in Practice" updated to reference ConcertHub as daily platform
- Certificate in Regulated Equity Release card: added `CeMAP_Professional.png` badge, `Equity release expert` label and link to `equity-release.html`
- Level 4 Diploma: `CeMAP_Professional.png` badge added (linking to `level4-dip.html`) on both `index.html` and `level4-dip.html` hero
- All credential badges on `index.html` now link to their respective qualification detail pages
- Contact form: added `_next` redirect, `_template=table` and optional phone number field
- Built 6 new qualification detail pages: `level6-dip.html`, `level4-dip.html`, `cemap.html`, `equity-release.html`, `cpsp.html`, `money-first-aid.html`

### May 2026 — Session 2 (Claude)
- Added three new qualifications: Money First Aid Certificate (Jan 2026), CPSP (April 2026), Certified FE Analytics User (May 2026)
- Replaced all inline base64 badge images with `images/` file references (HTML reduced from ~291KB to ~28KB)
- Swapped all SVG placeholder badges for official PNG/JPG digital badge images
- Added `Chartered_Financial_Adviser_LIBF.png` badge to Level 6 DipAFA card
- Added `CeMAP_Professional.png` + `Certified_Mortgage_Adviser.png` badges to CeMAP card
- Replaced FE Analytics Bootstrap modal with dedicated `fe-analytics.html` skills page
- Built `fe-analytics.html`: 14 skill cards across 4 categories, stats strip, hero and Applied in Practice section

### Initial build — DeepSeek
- Single-page responsive portfolio (`index.html`)
- Navy/gold brand palette with Playfair Display + Inter typography
- Sections: Hero, About, Education & Designations, Career Experience, Technical Skills, Contact
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
