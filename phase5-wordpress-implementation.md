# PHASE 5 — WORDPRESS IMPLEMENTATION PLAN
# Sri Shivasankalpa Vṛnda — Hostinger Managed WordPress

---

## TABLE OF CONTENTS

1. Theme Selection
2. Page Builder Strategy
3. Plugin Stack
4. Site Structure & Page Types
5. Menu Setup
6. Homepage Setup
7. Events Structure
8. Blog Structure
9. Gallery Structure
10. Contact Form Setup
11. Email / SMTP Setup
12. SEO Plugin Setup
13. Media Organization
14. Performance & Caching
15. Image Optimization
16. Backup Strategy
17. Security Basics
18. Build Sequence (Step-by-Step)

---

## 1. THEME SELECTION

### Recommended: Astra (Free)

You already have Astra installed — this is the right choice. Do not change it.

**Why Astra works perfectly here:**
- Fastest free WordPress theme (lightweight, < 50KB)
- Works seamlessly on Hostinger managed WordPress
- Deep integration with block editor (no page builder dependency)
- Google Fonts support (Cormorant Garamond + Source Sans 3 for Sacred Earth direction)
- Header/footer builder in free version
- Color and typography customizer
- Mobile-responsive out of the box
- Active development and community
- Starter templates available if needed

**What to avoid:**
- Do NOT buy Astra Pro — not needed for this project
- Do NOT install a second theme "just to try" — it adds bloat
- Do NOT use the Starter Templates plugin to import a premade design — build custom from your wireframes for a clean, unique site

### Theme Configuration Checklist

| Setting | Value |
|---------|-------|
| Global Colors — Primary | #C4841D (Turmeric Gold) |
| Global Colors — Secondary | #3D2B1F (Earth Brown) |
| Global Colors — Accent | #6B7F5E (Sage Green) |
| Global Colors — Background | #FAF6F0 (Warm Ivory) |
| Global Colors — Text | #2C2C2C (Dark Charcoal) |
| Global Colors — Link | #B8621B (Deep Saffron) |
| Heading Font | Cormorant Garamond (Google Fonts) |
| Body Font | Source Sans 3 (Google Fonts) |
| Base Font Size | 17px (body), 16px mobile |
| Container Width | 1200px |
| Header Layout | Logo left, menu center or right, Donate button right |
| Footer Layout | 4-column layout |
| Blog Layout | Grid (3 columns) |
| Sidebar | Right sidebar for blog only; all other pages full-width |

---

## 2. PAGE BUILDER STRATEGY

### Recommended: WordPress Block Editor (Gutenberg) + Spectra Plugin

**Do NOT install Elementor, Divi, WPBakery, or any heavy page builder.**

Why:
- Hostinger managed WordPress has limited server resources — heavy page builders slow sites significantly
- Block editor is native, fast, and increasingly powerful
- Spectra (by Brainstorm Force, the makers of Astra) adds advanced blocks designed specifically for Astra
- Non-technical admins find the block editor easier than complex page builders
- No vendor lock-in — content stays clean if you ever change themes

### Install: Spectra (Free)

**What Spectra adds beyond standard blocks:**
- Advanced columns and containers
- Icon blocks
- Countdown timer (useful for event pages)
- Team member blocks (for trustees)
- Testimonial blocks
- Call-to-action blocks
- Image gallery with lightbox
- FAQ / Accordion blocks (for donate page)
- Tabs blocks (for payment methods)
- Google Maps block

This gives you everything needed for every wireframe section without a heavy page builder.

---

## 3. PLUGIN STACK

### Essential Plugins (Install These)

| Plugin | Purpose | Free? | Priority |
|--------|---------|-------|----------|
| **Spectra** | Advanced blocks for Astra | ✅ Free | Tier 1 |
| **Yoast SEO** | SEO meta titles, descriptions, sitemaps, schema | ✅ Free | Tier 1 |
| **WPForms Lite** | Contact form | ✅ Free | Tier 1 |
| **WP Mail SMTP** | Reliable email delivery via SMTP | ✅ Free | Tier 1 |
| **Envira Gallery Lite** or **NextGEN Gallery** | Gallery with albums, lightbox, categories | ✅ Free | Tier 1 |
| **ShortPixel** or **Smush** | Automatic image compression | ✅ Free tier | Tier 1 |
| **UpdraftPlus** | Automated backups | ✅ Free | Tier 1 |
| **Wordfence** or rely on **Hostinger built-in security** | Security | ✅ Free | Tier 1 |
| **Simple Social Icons** | Social media icons in footer/header | ✅ Free | Tier 2 |
| **Insert Headers and Footers** (WPCode) | Google Analytics, any tracking code | ✅ Free | Tier 2 |

### Plugins to Avoid

| Plugin | Why Avoid |
|--------|-----------|
| Elementor / Divi / WPBakery | Too heavy for Hostinger, creates vendor lock-in |
| Jetpack (full suite) | Bloated, overlaps with other plugins, slows site |
| All-in-One SEO (if using Yoast) | Don't run two SEO plugins |
| Revolution Slider | Heavy, not needed |
| Any "coming soon" plugin | Use Astra's built-in maintenance mode or Hostinger's |
| WooCommerce | Not needed — you're not running an e-commerce store |
| Any popup/notification plugin | Not aligned with calm, spiritual UX |

### Total Plugin Count Target: 8–10 maximum

More plugins = slower site, more security risk, more update hassle. Every plugin must earn its place.

---

## 4. SITE STRUCTURE & PAGE TYPES

### Static Pages (built with Block Editor + Spectra)

| Page | Slug | Template |
|------|------|----------|
| Home | `/` (set as static front page) | Full-width, no sidebar |
| About Us | `/about` | Full-width, no sidebar |
| Events | `/events` | Full-width, no sidebar |
| Maharudra Purascharana | `/events/maharudra-purascharana-2026` | Full-width, no sidebar |
| Donate | `/donate` | Full-width, no sidebar |
| Gallery | `/gallery` | Full-width, no sidebar |
| Contact | `/contact` | Full-width, no sidebar |
| Gurukulas We Support | `/gurukulas` | Full-width, no sidebar (Tier 2) |
| Privacy Policy | `/privacy-policy` | Default, no sidebar |
| Terms | `/terms` | Default, no sidebar |

### Dynamic Content (WordPress Posts)

| Content Type | How to Build | Why |
|-------------|--------------|-----|
| Blog posts | Standard WordPress Posts | Native, SEO-friendly, easy for admins |
| Events | Individual static pages (for now) | At current scale (1-2 events), custom post types are overkill |
| Gallery | Envira/NextGEN gallery plugin | Better UX than manually adding images to a page |

### Custom Post Types — NOT Needed Now

At the current stage (1 event, 0 blog posts, no Gurukula profiles), adding custom post types adds complexity without benefit. Revisit when:
- You have 5+ events and need archive/filter functionality
- You have 3+ Gurukula profiles and want a repeatable template
- You add a team/people section with individual profile pages

### Reusable Patterns (Block Editor Feature)

Create these as **Synced Patterns** (formerly Reusable Blocks) so they can be used across multiple pages without re-creating:

| Pattern Name | Used On | Content |
|-------------|---------|---------|
| `donate-cta-strip` | Home, About, Events, Gallery, Blog | The warm CTA strip inviting donations |
| `trust-credibility-strip` | Home, About, Donate | Sringeri blessings, registration, trustee names |
| `seva-options-table` | Events detail, Donate | The seva types and amounts table |
| `payment-methods` | Donate (primary), Events detail (linked) | UPI, QR code, bank transfer details |
| `footer-tagline` | Footer (auto via theme) | Devanagari tagline + copyright |

**Why Synced Patterns matter:** When you update donation amounts or bank details in one place, it updates everywhere automatically. This is critical for non-technical admins.

---

## 5. MENU SETUP

### Primary Menu (Header)

```
About Us    Events    Gallery    Blog    Contact    [Donate] (styled as button)
```

**Setup in WordPress:**
1. Go to Appearance → Menus
2. Create menu named "Primary Menu"
3. Add pages in the order above
4. For the "Donate" item, add a CSS class `donate-menu-btn` via the Screen Options → CSS Classes checkbox
5. Assign to "Primary Menu" location
6. In Astra Customizer → Header Builder, style the last menu item as a button using the Donate class

### Footer Menu

```
Quick Links: Home | About Us | Events | Gallery | Blog | Contact
Get Involved: Donate | Volunteer | Spread the Word
```

**Setup:** Create two separate menus — "Footer Quick Links" and "Footer Get Involved" — assign each to a footer widget column.

### Mobile Menu

Astra handles mobile menu automatically — hamburger icon with slide-out. Ensure "Donate" button remains visible and prominent on mobile.

---

## 6. HOMEPAGE SETUP

### Step-by-Step

1. **Create a new Page** titled "Home"
2. **Go to Settings → Reading** → set "Your homepage displays" to "A static page" → select "Home"
3. **In Astra Customizer**, set the page to full-width with no title displayed (title is handled within the content)
4. **Build sections using Block Editor + Spectra:**

| Section | Blocks to Use |
|---------|--------------|
| Hero | Spectra Container (full-width, background image, overlay) + Heading + Paragraph + Buttons |
| Mission Positioning | Spectra Container + Heading + Paragraph + Button |
| How We Serve (4 pillars) | Spectra Advanced Columns (4-col) + Icon + Heading + Paragraph per column |
| Featured Event | Spectra Container (dark background #3D2B1F) + Image + Heading + Paragraph + Buttons |
| Why Gurukulas Matter | Spectra Container + Heading (Devanagari shloka) + Paragraph (translation) + Paragraph (body) |
| Trust Credibility Strip | Spectra Advanced Columns (3-4 col) + small text/icons |
| Donate Invitation | Spectra Container (gold background #C4841D) + Heading + Paragraph + Button |

### Important Settings for Homepage
- Remove page title from display (Astra page settings → disable title)
- Set each section's padding: desktop 80px top/bottom, mobile 40px
- Use full-width layout for all sections
- Test on mobile after each section is built

---

## 7. EVENTS STRUCTURE

### Events Listing Page (`/events`)

Built as a static page with:
- Hero section (heading + subheadline + intro text)
- Featured event section (manually built — large card with image, text, CTA)
- "Upcoming Events" section (manually add cards as events are planned)
- "Past Events" section (hidden initially, add after May 2026)

### Event Detail Page (`/events/maharudra-purascharana-2026`)

Built as a **child page** under Events:
1. Create a new Page
2. In Page Attributes → set Parent Page to "Events"
3. Set slug to `maharudra-purascharana-2026`
4. Build all sections from the wireframe using Block Editor + Spectra

This gives you the URL: `shivasankalpa.org/events/maharudra-purascharana-2026`

### Adding Future Events

For each new event:
1. Create a new Page as a child of "Events"
2. Copy the structure from the Maharudra page (use it as a template)
3. Add a card for it on the Events listing page
4. When event is over, move the card to "Past Events" section and add recap/photos

**When to switch to a plugin:** If you reach 5+ events per year, consider "The Events Calendar" plugin (free) for automated listings, calendars, and archives. Not needed now.

---

## 8. BLOG STRUCTURE

### Setup

1. **Create a new Page** titled "Blog" (leave it blank — WordPress auto-populates it)
2. **Go to Settings → Reading** → set "Posts page" to "Blog"
3. **In Astra Customizer → Blog**, configure:
   - Layout: Grid (3 columns)
   - Show featured image: Yes
   - Show excerpt: Yes (limit to 25 words)
   - Show date, author, category: Yes
   - Sidebar: Right (optional — can be disabled)

### Post Categories

Create these categories in Posts → Categories:
- Trust Updates
- Vedic Education
- Dharmic Thought
- Events

### Post Tags

Use sparingly and consistently. Good tags:
- Maharudra, Gurukula, Vedas, Vedangas, Sringeri, Rudra

### Blog Post Template (How to Write a New Post)

Each post should have:
1. **Title** — clear, keyword-rich
2. **Featured Image** — every post needs one (warm tones, relevant)
3. **Category** — exactly one primary category
4. **Tags** — 2–4 relevant tags
5. **Excerpt** — 1-2 sentence custom excerpt (don't rely on auto-excerpt)
6. **Body** — well-structured with headings (H2, H3), short paragraphs, images where helpful
7. **Yoast SEO** — fill in meta title and description for every post
8. **CTA at bottom** — use the `donate-cta-strip` synced pattern

---

## 9. GALLERY STRUCTURE

### Recommended Plugin: Envira Gallery Lite

**Why Envira over other options:**
- Lightweight
- Clean grid + lightbox
- Album/category support
- Easy for non-technical admins
- Works well with Astra
- Drag-and-drop image management

### Setup

1. Install and activate Envira Gallery Lite
2. Create galleries by category:
   - "Gurukula Life"
   - "Events"
   - "Trust Activities"
3. Upload images into each gallery with titles and alt text
4. On the Gallery page (`/gallery`), add:
   - Hero section with headline and intro text
   - Embed each gallery using the Envira shortcode or block
   - CTA strip at the bottom

### Alternative: NextGEN Gallery

If Envira feels limited, NextGEN Gallery (free) offers more features — albums, slideshows, thumbnails. Slightly heavier but still manageable. Choose one, not both.

---

## 10. CONTACT FORM SETUP

### Plugin: WPForms Lite

### Form Fields

| Field | Type | Required |
|-------|------|----------|
| Your Name | Text (single line) | Yes |
| Email Address | Email | Yes |
| Subject | Dropdown: General Inquiry / Donation Query / Volunteer / Event Inquiry / Other | Yes |
| Your Message | Textarea (multiline) | Yes |

### Setup Steps

1. Install WPForms Lite
2. Create a new form: "Contact Form"
3. Add the fields above
4. Set notification email to: info@shivasankalpa.org
5. Set confirmation message: "Thank you for reaching out. We typically respond within 2 business days."
6. Embed the form on the Contact page using the WPForms block

### Anti-Spam

WPForms Lite includes basic anti-spam (honeypot). For extra protection:
- Enable the built-in WPForms anti-spam token
- Optionally add hCaptcha (free) — Google reCAPTCHA also works but hCaptcha is more privacy-friendly

---

## 11. EMAIL / SMTP SETUP

### Problem

WordPress default mail function (`wp_mail`) is unreliable — emails from contact forms and notifications often go to spam or don't deliver at all.

### Solution: WP Mail SMTP Plugin

### Recommended SMTP Configuration for Hostinger

Hostinger provides built-in email with your business email (info@shivasankalpa.org). Use Hostinger's SMTP:

| Setting | Value |
|---------|-------|
| From Email | info@shivasankalpa.org |
| From Name | Sri Shivasankalpa Vṛnda |
| SMTP Host | smtp.hostinger.com |
| Encryption | SSL |
| SMTP Port | 465 |
| SMTP Username | info@shivasankalpa.org |
| SMTP Password | (your email password) |

### Setup Steps

1. Install WP Mail SMTP
2. Go to WP Mail SMTP → Settings
3. Enter the values above
4. Send a test email to verify delivery
5. Confirm contact form notifications arrive at info@shivasankalpa.org

---

## 12. SEO PLUGIN SETUP

### Plugin: Yoast SEO (Free)

### Initial Configuration

1. **Run the Yoast Configuration Wizard:**
   - Site type: Organization (not person)
   - Organization name: Sri Shivasankalpa Vṛnda
   - Set social profiles (when available)

2. **General Settings:**
   - Enable XML Sitemaps: Yes
   - Set homepage meta title and description (from Phase 4)
   - Breadcrumbs: Enable (Astra supports Yoast breadcrumbs natively)

3. **For Every Page/Post, Fill In:**
   - SEO Title (use the meta titles from Phase 4)
   - Meta Description (use the meta descriptions from Phase 4)
   - Focus Keyphrase (set one per page)

### Focus Keyphrases by Page

| Page | Focus Keyphrase |
|------|----------------|
| Home | Shivasankalpa Vedic Gurukula support |
| About | Shivasankalpa trust about |
| Events | Vedic events Shivasankalpa |
| Maharudra Detail | Maharudra Purascharana 2026 Bangalore |
| Donate | Donate Vedic Gurukula |
| Gallery | Vedic Gurukula gallery |
| Blog | Vedic Dharma blog |
| Contact | Shivasankalpa contact |

4. **Schema / Structured Data:**
   - Yoast automatically adds Organization schema
   - For the Events page: consider adding Event schema manually via the WPCode plugin (Insert Headers and Footers) — provide JSON-LD for the Maharudra event
   - For blog posts: Yoast handles Article schema automatically

---

## 13. MEDIA ORGANIZATION

### Folder Structure (Mental Model)

WordPress doesn't natively support folders, but use consistent naming:

| Naming Convention | Example |
|------------------|---------|
| `page-section-description` | `home-hero-gurukula-students.jpg` |
| `event-name-description` | `maharudra-2026-homa-setup.jpg` |
| `gallery-category-description` | `gallery-gurukula-morning-chanting.jpg` |
| `trustee-name` | `trustee-harisha-harithasa.jpg` |
| `blog-post-slug-image` | `blog-why-gurukulas-matter-hero.jpg` |

### Image Specifications

| Usage | Recommended Size | Format |
|-------|-----------------|--------|
| Hero backgrounds | 1920 × 800px | JPEG (compressed) |
| Featured event images | 1200 × 630px | JPEG |
| Blog featured images | 1200 × 630px | JPEG |
| Gallery images | 1200 × 900px (landscape) or 900 × 1200px (portrait) | JPEG |
| Trustee headshots | 400 × 400px (square) | JPEG or PNG |
| Logo | SVG preferred, or PNG with transparency | SVG/PNG |
| QR Code | 400 × 400px minimum | PNG |
| Favicon | 512 × 512px | PNG |

### Alt Text Guidelines

Every image must have descriptive alt text for SEO and accessibility:
- Good: "Vedic students chanting during morning prayers at a Gurukula"
- Bad: "IMG_3847" or "image1" or left empty
- For decorative images: leave alt text empty (screen readers skip them)

---

## 14. PERFORMANCE & CACHING

### Hostinger Built-in Caching

Hostinger managed WordPress includes LiteSpeed caching. This is already active. Confirm:
1. Go to Hostinger dashboard → WordPress → Performance
2. Ensure "Object Cache" is enabled
3. Ensure "LiteSpeed Cache" plugin is installed and active (Hostinger often pre-installs this)

### If LiteSpeed Cache Plugin is Active

| Setting | Value |
|---------|-------|
| Page Cache | ON |
| Object Cache | ON (if available on your Hostinger plan) |
| Browser Cache | ON |
| CSS/JS Minification | ON |
| CSS/JS Combination | ON (test for conflicts first) |
| Lazy Load Images | ON |

### Additional Performance Tips

- Do NOT install a second caching plugin (no W3 Total Cache, no WP Super Cache alongside LiteSpeed)
- Keep total plugins under 10
- Use the ShortPixel/Smush plugin for image optimization (see below)
- Avoid auto-playing videos — use click-to-play embeds
- Use YouTube embeds for video (don't self-host video files)

---

## 15. IMAGE OPTIMIZATION

### Plugin: ShortPixel Image Optimizer (Free Tier)

**Why ShortPixel:**
- Compresses images on upload automatically
- Free tier: 100 images/month (sufficient for your usage)
- Supports lossy + lossless compression
- WebP conversion (modern format, faster loading)
- Works silently in the background

### Configuration

| Setting | Value |
|---------|-------|
| Compression Type | Lossy (best file size reduction, minimal quality loss) |
| Create WebP | Yes |
| Resize large images | Yes — max width 2048px |
| Remove EXIF data | Yes |
| Backup originals | Yes |

### Alternative: Smush (Free)

If ShortPixel's 100/month limit is reached, Smush offers unlimited free compression (slightly less aggressive but reliable).

---

## 16. BACKUP STRATEGY

### Plugin: UpdraftPlus (Free)

### Configuration

| Setting | Value |
|---------|-------|
| Backup schedule — Files | Weekly |
| Backup schedule — Database | Daily |
| Retain | 4 file backups, 14 database backups |
| Remote storage | Google Drive (free, easy to set up) |
| What to back up | Plugins, themes, uploads, database |

### Setup Steps

1. Install UpdraftPlus
2. Go to Settings → UpdraftPlus
3. Set schedule as above
4. Connect Google Drive (follow the authentication flow)
5. Run a manual backup immediately to verify
6. Test a restore once to confirm backups work

### Hostinger Also Provides

Hostinger managed WordPress includes weekly automatic backups accessible from the Hostinger dashboard. UpdraftPlus gives you more frequent + portable backups as a second layer.

---

## 17. SECURITY BASICS

### Hostinger Built-in Security

Hostinger managed WordPress provides:
- SSL certificate (ensure HTTPS is active on shivasankalpa.org)
- Automatic WordPress core updates
- Built-in firewall
- Malware scanning

### Additional Steps

| Action | How |
|--------|-----|
| **Strong admin password** | Use a 16+ character password. Never use "admin" as username. |
| **Limit login attempts** | Hostinger may include this. If not, Wordfence free or "Limit Login Attempts Reloaded" plugin. |
| **Keep everything updated** | Update WordPress core, themes, and plugins promptly. Check weekly. |
| **Remove unused themes/plugins** | Delete (not just deactivate) any theme or plugin not in use. |
| **SSL verification** | Visit shivasankalpa.org — confirm the padlock icon appears. If not, in Hostinger dashboard → SSL → force HTTPS. |
| **Disable file editing** | Add `define('DISALLOW_FILE_EDIT', true);` to wp-config.php (prevents editing theme/plugin files from WP admin — safety net). |

### Do NOT install multiple security plugins

If using Hostinger's built-in security, you likely don't need Wordfence. If you add Wordfence, don't add Sucuri or iThemes too. One security layer is sufficient.

---

## 18. BUILD SEQUENCE (Step-by-Step)

### The 1-Week Build Plan

This is the practical sequence for taking the site live within your timeline.

#### Day 1 — Foundation

| # | Task | Time |
|---|------|------|
| 1 | Log into Hostinger WordPress admin | 5 min |
| 2 | Update WordPress core, Astra theme to latest versions | 10 min |
| 3 | Delete unused default themes (Twenty Twenty-Three, etc.) | 5 min |
| 4 | Delete unused default plugins (Hello Dolly, Akismet if not using) | 5 min |
| 5 | Install plugins: Spectra, Yoast SEO, WPForms Lite, WP Mail SMTP, ShortPixel, UpdraftPlus | 15 min |
| 6 | Install gallery plugin: Envira Gallery Lite or NextGEN | 5 min |
| 7 | Configure Astra: set global colors, fonts, container width, header, footer | 45 min |
| 8 | Set up UpdraftPlus backup to Google Drive, run first backup | 15 min |
| 9 | Configure WP Mail SMTP with Hostinger email | 15 min |
| 10 | Send test email to verify delivery | 5 min |

**Day 1 total: ~2 hours**

#### Day 2 — Homepage

| # | Task | Time |
|---|------|------|
| 1 | Create "Home" page, set as static front page | 5 min |
| 2 | Build Hero section (container + background image + text + CTAs) | 45 min |
| 3 | Build Mission Positioning section | 20 min |
| 4 | Build How We Serve (4 pillars) section | 30 min |
| 5 | Build Featured Event section (dark background) | 30 min |
| 6 | Build Why Gurukulas Matter section (shloka + body) | 20 min |
| 7 | Build Trust Credibility strip | 15 min |
| 8 | Build Donate Invitation strip | 15 min |
| 9 | Test on mobile | 15 min |

**Day 2 total: ~3.5 hours**

#### Day 3 — About Us + Contact

| # | Task | Time |
|---|------|------|
| 1 | Create "About Us" page, build all sections | 2 hours |
| 2 | Create "Contact" page | 15 min |
| 3 | Create contact form in WPForms, embed on Contact page | 20 min |
| 4 | Test contact form submission | 10 min |
| 5 | Create Synced Patterns: donate-cta-strip, trust-credibility-strip | 20 min |

**Day 3 total: ~3 hours**

#### Day 4 — Events + Maharudra Detail

| # | Task | Time |
|---|------|------|
| 1 | Create "Events" listing page with hero + intro + featured card | 1 hour |
| 2 | Create "Maharudra Purascharana 2026" as child page | 10 min |
| 3 | Build event hero, about, spiritual significance sections | 1 hour |
| 4 | Build programme schedule tables | 30 min |
| 5 | Build seva options section | 30 min |
| 6 | Build how to participate + venue sections | 30 min |
| 7 | Test on mobile | 15 min |

**Day 4 total: ~4 hours**

#### Day 5 — Donate + Gallery

| # | Task | Time |
|---|------|------|
| 1 | Create "Donate" page | 10 min |
| 2 | Build hero, why donate, seva options sections | 1 hour |
| 3 | Build payment methods section (tabs: UPI / QR / Bank) | 45 min |
| 4 | Build transparency section + FAQ accordion | 45 min |
| 5 | Create "Gallery" page with hero + intro | 20 min |
| 6 | Set up Envira galleries, upload available media | 45 min |
| 7 | Embed galleries on Gallery page | 15 min |

**Day 5 total: ~4 hours**

#### Day 6 — Blog + SEO + Navigation

| # | Task | Time |
|---|------|------|
| 1 | Create "Blog" page, set as posts page | 10 min |
| 2 | Create blog categories (Trust Updates, Vedic Education, Dharmic Thought, Events) | 10 min |
| 3 | Write and publish 1 seed blog post (optional but recommended) | 1 hour |
| 4 | Set up menus: Primary (header) + Footer menus | 20 min |
| 5 | Style the Donate menu button | 15 min |
| 6 | Configure Yoast SEO: run wizard, set homepage meta, enable sitemaps | 30 min |
| 7 | Set meta titles and descriptions for ALL pages (from Phase 4) | 30 min |
| 8 | Set up ShortPixel image optimization | 10 min |
| 9 | Build the footer: 4-column layout with all content | 30 min |

**Day 6 total: ~3.5 hours**

#### Day 7 — QA, Launch, Post-Launch

| # | Task | Time |
|---|------|------|
| 1 | Full review: check every page on desktop | 45 min |
| 2 | Full review: check every page on mobile | 45 min |
| 3 | Check all links (CTAs, menu items, footer links) | 20 min |
| 4 | Check contact form delivers email | 10 min |
| 5 | Check donate page — all payment info correct | 10 min |
| 6 | Verify SSL (HTTPS padlock) | 5 min |
| 7 | Verify Yoast sitemap: shivasankalpa.org/sitemap_index.xml | 5 min |
| 8 | Submit sitemap to Google Search Console | 15 min |
| 9 | Remove "Coming Soon" page / maintenance mode | 5 min |
| 10 | Take final backup before going live | 10 min |
| 11 | **GO LIVE** | — |
| 12 | Test site as a visitor (incognito browser) | 15 min |
| 13 | Share site URL with trust team for review | 5 min |

**Day 7 total: ~3 hours**

---

## PAGE CLASSIFICATION: Static vs. Dynamic vs. Template

| Page | Type | Notes |
|------|------|-------|
| Home | **Static page** | Built section by section, rarely changes structure |
| About | **Static page** | Update trustee bios/photos occasionally |
| Events listing | **Static page** | Manually add/move event cards |
| Event detail | **Static page** (child) | One page per event, copy structure for future events |
| Donate | **Static page** | Update payment details, seva options as needed |
| Gallery | **Semi-dynamic** | Gallery plugin manages photos, page wraps them |
| Blog listing | **Dynamic** | WordPress auto-populates from posts |
| Blog post | **Dynamic** | Standard WordPress post template |
| Contact | **Static page** | Embed WPForms shortcode, rarely changes |
| Gurukulas | **Static page** | Tier 2 — build when ready |

---

## SUMMARY: Complete Plugin List at Launch

| # | Plugin | Purpose |
|---|--------|---------|
| 1 | Spectra | Advanced blocks |
| 2 | Yoast SEO | SEO management |
| 3 | WPForms Lite | Contact form |
| 4 | WP Mail SMTP | Reliable email delivery |
| 5 | Envira Gallery Lite | Photo galleries |
| 6 | ShortPixel | Image compression |
| 7 | UpdraftPlus | Backups |
| 8 | WPCode (Insert Headers & Footers) | Analytics, schema |
| 9 | LiteSpeed Cache | Performance (likely pre-installed by Hostinger) |

**Total: 9 plugins. Clean, lightweight, maintainable.**
