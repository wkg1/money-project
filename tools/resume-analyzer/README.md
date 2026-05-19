# ResumeLab — AI Resume Analyzer & Optimizer

A premium single-page micro-SaaS tool that analyzes resumes/CVs, scores them for ATS compatibility, and provides specific improvement suggestions. Built with HTML, Tailwind CSS, and vanilla JavaScript — zero backend required.

## Quick Start

1. Open `index.html` in any browser. That's it.
2. Upload a PDF or DOCX resume.
3. Get your score and improvement suggestions instantly.

All analysis runs entirely in the browser — no data is sent anywhere.

## How It Works

### Text Extraction
- **PDF files**: Parsed client-side using PDF.js (v3.11)
- **DOCX files**: Parsed client-side using Mammoth.js (v1.8)

### Analysis Engine (Scored out of 100)

| Category | Max Points | What It Checks |
|----------|-----------|----------------|
| ATS Compatibility | 30 | Email/phone presence, standard headings, no tables/columns, consistent date formatting, bullet point usage |
| Keywords & Skills | 30 | Industry keyword density (12+ categories), soft skills, action verb usage, weak phrase detection |
| Content Quality | 25 | Quantifiable achievements, first-person pronoun avoidance, bullet point quality |
| Structure & Format | 15 | Core sections present, appropriate length (250-1200 words), section ordering |

### Keyword Database

The analyzer checks against 100+ industry keywords across 8 categories:
- Technology, Business, Marketing, Finance, Healthcare, Sales, Project Management, Engineering

It also validates against 25+ common action verbs and flags 15+ weak/cliche phrases.

## Monetization

### Stripe Setup

1. Create a [Stripe account](https://stripe.com)
2. Go to **Products** > **Create Product**
3. Set up a one-time payment product for $29 (or your price)
4. Under the product, create a **Payment Link**
5. Copy the link and replace `https://buy.stripe.com/placeholder` in `index.html` (appears in 3 places)

### Revenue Model

- **Free tier**: Overall score, category breakdowns, top 8 issues
- **Premium ($29 one-time)**: Full optimization report including:
  - Rewritten professional summary
  - Keyword optimization map
  - ATS compatibility fixes
  - Industry-specific improvement suggestions
  - 7-day personalized action plan

### Pricing Strategy Tips

- **$29 one-time** is the sweet spot for resume tools — low enough for impulse purchase, high enough to show value
- Consider a **$49 "Resume + Cover Letter" bundle** later
- Add **volume discounts** for universities/career centers
- Offer an **affiliate program** (30% commission) for career coaches and LinkedIn influencers

## Deployment Options

### Option 1: Netlify / Vercel (Free, Easiest)

1. Push the folder to a GitHub repo
2. Connect to Netlify or Vercel
3. Deploy — takes 60 seconds
4. Add a custom domain

### Option 2: Cloudflare Pages (Free, Fastest CDN)

1. Push to GitHub
2. Connect Cloudflare Pages to the repo
3. Deploy with default settings (no build command needed)

### Option 3: Any Static Host

Upload `index.html` to any static file host — S3 + CloudFront, GitHub Pages, Firebase Hosting, etc.

### Option 4: Sell as a Downloadable

Package `index.html` as a ZIP and sell on Gumroad, Lemon Squeezy, or Payhip as a "White Label Resume Analyzer" that agencies can embed on their own sites.

## Customization

### Change Pricing / Text

Search for `$29` in `index.html` — all pricing copy is centralized for easy changes.

### Change Color Scheme

Edit the Tailwind config block near the top of `index.html` — the `navy` and `gold` color scales are defined there.

### Add More Keywords

Edit the `INDUSTRY_KEYWORDS` object in the script section. Add new categories or expand existing ones.

### Connect a Backend (Optional)

The analysis engine (`analyzeResume()` function) is self-contained. You can:
1. Send results to a backend to store in a database
2. Add user accounts and save analysis history
3. Integrate with OpenAI API for AI-powered rewrite suggestions
4. Add email capture for lead generation

## Files

```
resume-analyzer/
  index.html    Complete single-page application
  README.md     This file
```

That's it. No build step, no dependencies to install, no backend to maintain.

## Browser Support

All modern browsers — Chrome, Firefox, Safari, Edge. Requires JavaScript enabled.
