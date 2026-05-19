# AI Tools Review — Affiliate Content Site

A niche SEO affiliate website targeting "best AI tools for [use case]" keywords. Built as a static HTML site for maximum speed, zero hosting costs, and easy deployment.

## Site Structure

```
ai-tools-review/
  index.html                          # Homepage (hero, featured comparisons, review grid)
  about.html                          # About page with full affiliate disclosure
  blog/
    best-ai-writing-tools.html        # Jasper vs Copy.ai vs Writesonic vs ChatGPT
    best-ai-image-generators.html     # Midjourney vs DALL-E vs Stable Diffusion vs Leonardo
    best-ai-video-tools.html          # Runway vs Pika vs Synthesia vs HeyGen
  css/
    style.css                         # All styles (mobile-first, light theme, ~500 lines)
  README.md                           # This file
```

## Target Keywords

| Article | Primary Keyword | Monthly Search Volume (est.) |
|---------|----------------|------------------------------|
| Homepage | best AI tools 2026 | ~15,000 |
| Writing tools | best AI writing tools 2026 | ~8,000 |
| Writing tools | Jasper vs Copy.ai vs Writesonic | ~2,500 |
| Image generators | best AI image generator 2026 | ~9,000 |
| Image generators | Midjourney vs DALL-E comparison | ~3,500 |
| Video tools | best AI video tools 2026 | ~5,500 |
| Video tools | Runway vs Pika comparison | ~1,800 |

## Monetization

### Active Affiliate Programs

| Tool | Affiliate Program | Approximate Commission | Signup Link |
|------|------------------|----------------------|-------------|
| Jasper | Jasper Partners | 30% recurring (lifetime) | https://www.jasper.ai/partners |
| Copy.ai | Copy.ai Partners (PartnerStack) | 20-30% recurring | https://www.copy.ai/partners |
| Writesonic | Writesonic Affiliate Program | 30% recurring | https://writesonic.com/affiliate-program |
| Leonardo AI | Leonardo AI Affiliate | 25% recurring | https://leonardo.ai/affiliates |
| Runway | Runway Affiliate Program | ~10-20% | https://runwayml.com/affiliates |
| Synthesia | Synthesia Partner Program | 20% recurring | https://www.synthesia.io/partners |
| HeyGen | HeyGen Affiliate Program | 20% recurring | https://www.heygen.com/affiliates |

### Non-Affiliate Recommendations (also included because they're genuinely best for some users)
- ChatGPT (OpenAI) — No affiliate program
- Midjourney — No public affiliate program
- Stable Diffusion — Open source, no affiliate program
- Pika — No public affiliate program (as of May 2026)

### Revenue Potential Estimate
At 10,000 monthly visitors with a 3% click-through rate and 5% conversion rate on a $30/mo subscription plan (at 25% avg commission), monthly revenue would be approximately $1,100. Historically realistic affiliate site metrics assume 1-2% conversion, placing a more conservative estimate around $400-$800/month at this traffic level.

## Deployment Options

### Option 1: Netlify (Recommended — Free)
1. Push the `ai-tools-review/` folder to a GitHub repository
2. Connect the repo to Netlify (netlify.com)
3. Set the publish directory to `/` (root of the repo)
4. Deploy. Netlify provides free SSL, CDN, and 100GB/month bandwidth
5. Add your custom domain in Netlify's domain settings

### Option 2: Cloudflare Pages (Free, faster CDN)
1. Push the repo to GitHub
2. Connect to Cloudflare Pages (pages.cloudflare.dev)
3. Set build output directory to `/`
4. Deploy. Unlimited bandwidth on the free plan
5. Add custom domain through Cloudflare (also free DNS)

### Option 3: GitHub Pages (Free)
1. Push to a GitHub repo
2. Go to Settings > Pages
3. Set source to "Deploy from a branch" and select `main` / `(root)`
4. Site will be live at `yourusername.github.io/repo-name`
5. Add a custom domain in the Pages settings

### Option 4: Vercel (Free)
1. Push to GitHub
2. Import to Vercel (vercel.com)
3. Deploy. Free SSL, CDN, and 100GB/month bandwidth
4. Add custom domain in Vercel's domain settings

### Option 5: Any Static Host (S3, BunnyCDN, etc.)
Since this is pure HTML/CSS, serve the directory from any static host or object storage bucket.

## Post-Deployment Checklist

1. **Replace placeholder email.** Change `hello@aitoolsreview.com` in about.html to your actual contact email.

2. **Set up Google Search Console.** Add your domain and submit your sitemap (you will need to create one — see below).

3. **Set up Google Analytics.** Add your GA4 measurement ID to each page's `<head>`.

4. **Create a sitemap.xml.** Use a tool like xml-sitemaps.com or generate one manually. Submit it to Google Search Console and Bing Webmaster Tools.

5. **Add a robots.txt file:**
```
User-agent: *
Allow: /
Sitemap: https://yourdomain.com/sitemap.xml
```

6. **Set up your affiliate accounts.** Sign up for each affiliate program listed above. Replace the generic affiliate links on each page with your personal affiliate IDs/tracking codes.

7. **Add images.** The current card placeholders are CSS gradients. Add real screenshots or tool logos for better UX and SEO:
   - Create an `images/` folder
   - Add a 1200x630 Open Graph image for each article
   - Add tool logos/screenshots for the review cards on the homepage

8. **Interlink review articles.** Add contextual links between related articles (e.g., from the writing tools article, link to the image tools article where relevant).

9. **Build backlinks.** Reach out to AI newsletters, blogs, and forums. Guest post on related sites. List your site on affiliate directories.

10. **Content calendar.** Plan additional articles to expand topical authority:
    - Best AI audio tools (ElevenLabs, Murf, Speechify)
    - Best AI coding assistants (Cursor, Copilot, Windsurf)
    - Best AI SEO tools (Surfer, Clearscope, NeuronWriter)
    - Individual deep-dive reviews of each tool
    - "How to use [Tool] for [Specific Task]" tutorials
    - Monthly roundups of new AI tool releases

## SEO Best Practices Implemented

- Proper meta titles and descriptions with target keywords
- Open Graph and Twitter Card meta tags
- JSON-LD structured data (Article schema on blog posts, WebSite schema on homepage)
- Canonical URLs to prevent duplicate content
- Semantic HTML5 (article, nav, main, aside, header, footer)
- Mobile-first responsive design
- Fast loading (no JS frameworks, no external dependencies, system fonts)
- Breadcrumb navigation for internal linking
- Proper heading hierarchy (single h1, h2 for sections, h3 for subsections)
- rel="nofollow sponsored" on affiliate links (FTC/Google compliant)

## Design Decisions

- **System fonts only** — No web font downloads. Renders instantly on every device.
- **Zero JavaScript** — No frameworks, no tracking bloat. Pure HTML + CSS.
- **Light color scheme** — White background, blue (#2563eb) accent. High contrast for readability.
- **Mobile-first CSS** — Starts with single-column layout, adds grid layouts at breakpoints.
- **Sticky header** — Backdrop-filter blur for a modern feel without JS.
- **No external dependencies** — The entire site loads in a single HTTP request (HTML + inline CSS reference).

## License

This site content is for your use. Modify, deploy, and monetize as you see fit. All tool names and trademarks belong to their respective owners.
