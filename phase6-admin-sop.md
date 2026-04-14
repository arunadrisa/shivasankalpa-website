# PHASE 6 — ADMIN-FRIENDLY OPERATIONS
# Sri Shivasankalpa Vṛnda — Simple Admin Guide & SOP

---

## WHO THIS IS FOR

Non-technical administrators who are comfortable with Google Docs/Sheets but may not have WordPress experience. This guide assumes you can:
- Log into a website admin panel
- Upload photos from your phone/computer
- Copy and paste text
- Follow step-by-step instructions

---

## TABLE OF CONTENTS

1. Logging In
2. Dashboard Overview — What Matters, What to Ignore
3. How to Add a New Event
4. How to Upload Photos/Videos to the Gallery
5. How to Update Donation Information
6. How to Edit Homepage Sections Safely
7. How to Publish a New Blog Article
8. Naming Conventions
9. What Should NEVER Be Edited Directly
10. What Is Template-Driven (Synced Patterns)
11. Weekly Maintenance Checklist
12. Quick Reference Card

---

## 1. LOGGING IN

**URL:** `shivasankalpa.org/wp-admin`

**Username:** [Your admin username — NOT "admin"]
**Password:** [Your secure password — store in a password manager]

After logging in, you'll see the WordPress Dashboard.

**Tip:** Bookmark `shivasankalpa.org/wp-admin` in your browser for quick access.

---

## 2. DASHBOARD OVERVIEW

### What You'll Use Regularly

| Menu Item | What It Does | How Often |
|-----------|-------------|-----------|
| **Pages** | Edit existing pages (Home, About, Events, Donate, etc.) | As needed |
| **Posts** | Write and publish blog articles | Weekly/monthly |
| **Media** | Upload and manage photos/videos | As needed |
| **Envira Gallery** | Manage photo galleries | After events |
| **WPForms** | View contact form submissions | Weekly |
| **Yoast SEO** | Shows SEO status on pages/posts | When editing |

### What You Can Safely Ignore

| Menu Item | Why Ignore |
|-----------|-----------|
| Appearance → Theme Editor | NEVER touch this — it's raw code |
| Plugins → Plugin Editor | NEVER touch this |
| Tools | Not needed for day-to-day |
| Settings (most sub-menus) | Already configured — don't change |
| Comments | Disable or ignore unless you enable blog comments |

---

## 3. HOW TO ADD A NEW EVENT

### Step-by-Step

**Time required:** 30–45 minutes

1. **Go to Pages → Add New**

2. **Set the title:** Use the event name
   - Example: "Ganesha Homa — August 2026"

3. **Set the parent page:**
   - In the right sidebar, find "Page Attributes"
   - Set **Parent Page** to "Events"
   - This creates the URL: `shivasankalpa.org/events/ganesha-homa-august-2026`

4. **Set the URL slug:**
   - Click on the URL/Permalink area
   - Set slug to something clean: `ganesha-homa-august-2026`

5. **Build the page content:**
   - Use the Maharudra Purascharana page as your reference
   - Copy the section structure (you can literally duplicate that page and edit the content)
   - Sections to include:
     - Event hero (title, date, venue)
     - About the event (2–3 paragraphs)
     - Programme schedule (use a table block)
     - Seva options (if applicable)
     - How to participate
     - Venue & directions
     - Closing

6. **Add a featured image:**
   - In the right sidebar → Featured Image → Set Featured Image
   - Upload a relevant photo (see naming conventions below)

7. **Set SEO (Yoast):**
   - Scroll to the bottom of the editor
   - Fill in "SEO Title" and "Meta Description"
   - Example title: "Ganesha Homa August 2026 — Sri Shivasankalpa Vṛnda"
   - Example description: "Join the Ganesha Homa organized by Sri Shivasankalpa Vṛnda in August 2026. View schedule, seva options, and how to participate."

8. **Publish:**
   - Click "Publish" in the top right
   - Review the live page

9. **Add the event to the Events listing page:**
   - Go to Pages → Events (the listing page)
   - Edit the page
   - In the "Upcoming Events" section, add a new card with:
     - Event name
     - Date
     - 1-line summary
     - "View Details" button linking to the new event page
   - Update the page

### After the Event Is Over

1. Edit the Events listing page
2. Move the event card from "Upcoming Events" to "Past Events" section
3. Optionally add a recap paragraph and link to gallery photos
4. The event detail page stays live (don't delete it — it's good for SEO)

---

## 4. HOW TO UPLOAD PHOTOS/VIDEOS TO THE GALLERY

### Adding Photos to an Existing Gallery

**Time required:** 10–20 minutes

1. **Go to Envira Gallery** in the left sidebar menu
2. **Click on the gallery** you want to add photos to (e.g., "Events" or "Gurukula Life")
3. **Click "Add Photos"** or drag and drop images into the upload area
4. **For each photo, fill in:**
   - **Title:** Short description (e.g., "Morning Vedic chanting")
   - **Alt Text:** Descriptive text for SEO (e.g., "Students performing morning Vedic chanting at a Gurukula")
   - **Caption:** Optional, shown below the photo in the gallery
5. **Click "Update"** to save

### Creating a New Gallery Category

1. **Go to Envira Gallery → Add New**
2. **Name the gallery** (e.g., "Maharudra Purascharana 2026")
3. **Upload all photos** for that category
4. **Fill in titles and alt text** for each
5. **Publish** the gallery
6. **Go to Pages → Gallery**
7. **Add the new gallery** to the page using the Envira block:
   - Click the "+" button to add a block
   - Search for "Envira"
   - Select your new gallery
8. **Update** the Gallery page

### Uploading Videos

- **Do NOT upload video files directly to WordPress** — they are too large and slow down the site
- Instead:
  1. Upload the video to **YouTube** (unlisted or public)
  2. Copy the YouTube URL
  3. On the Gallery page or any page, add a "YouTube" embed block
  4. Paste the URL
  5. The video will embed automatically

---

## 5. HOW TO UPDATE DONATION INFORMATION

### Updating Bank Details, UPI ID, or QR Code

**Important:** Donation information uses **Synced Patterns** (formerly Reusable Blocks). This means you update it in ONE place and it changes everywhere on the site.

1. **Go to the Block Editor** on the Donate page (Pages → Donate → Edit)
2. **Find the payment section** — it will have a purple border indicating it's a Synced Pattern
3. **Click on it** — you'll see a notice that it's a synced pattern
4. **Click "Edit original"** to edit the pattern itself
5. **Make your changes:**
   - Update bank account number, IFSC, etc.
   - Replace QR code image (click on existing image → Replace)
   - Update UPI ID
6. **Click "Update"** to save
7. **The change is now live on every page that uses this pattern** (Donate page, Events page if embedded)

### Adding 80G Information (When Ready)

1. Go to Pages → Donate → Edit
2. Find the "Transparency & Trust" section
3. Replace the placeholder text `[PLACEHOLDER: 80G registration is currently in progress...]` with:
   - "Donations to Sri Shivasankalpa Vṛnda are eligible for tax exemption under Section 80G of the Income Tax Act. Registration No: [your 80G number]."
4. Update the page
5. Also update the Trust Credibility strip synced pattern with "80G Approved"

### Updating Seva Amounts

1. The seva table is also a Synced Pattern
2. Follow the same process: find it → Edit original → change amounts → Update
3. Both the Events page and Donate page will reflect the change

---

## 6. HOW TO EDIT HOMEPAGE SECTIONS SAFELY

### General Rules

- **NEVER delete a section** — if you want to hide something, select the block and change its visibility
- **Always "Preview" before "Update"** — use the Preview button to see changes before publishing
- **Work on one section at a time** — don't try to rebuild the whole page at once

### Editing Text on the Homepage

1. Go to Pages → Home → Edit
2. Click directly on the text you want to change
3. Edit the text (just like editing a Google Doc)
4. Click "Preview" to check
5. Click "Update" to publish

### Changing a Homepage Image

1. Go to Pages → Home → Edit
2. Click on the image you want to change
3. In the toolbar that appears, click "Replace"
4. Choose "Media Library" to pick an existing image, or "Upload" for a new one
5. Click "Preview" → then "Update"

### Changing the Hero Background Image

1. Go to Pages → Home → Edit
2. Click on the hero section (the large top container)
3. In the right sidebar, look for "Background" settings under the Spectra container options
4. Click on the background image → Replace
5. Upload the new image
6. Preview → Update

### Editing the Featured Event on Homepage

When the Maharudra event is over and you want to feature a new event:
1. Go to Pages → Home → Edit
2. Find the "Featured Event" section
3. Change the headline, date, venue, description text
4. Change the CTA button link to point to the new event page
5. Replace the event image if applicable
6. Preview → Update

---

## 7. HOW TO PUBLISH A NEW BLOG ARTICLE

### Step-by-Step

**Time required:** 20–40 minutes (excluding writing time)

1. **Go to Posts → Add New**

2. **Write the title:** Clear, descriptive, keyword-rich
   - Good: "Why Vedic Gurukulas Are Essential for Preserving Our Heritage"
   - Avoid: "Update #3" or "New Post"

3. **Set the category:**
   - In the right sidebar → Categories
   - Check ONE primary category: Trust Updates / Vedic Education / Dharmic Thought / Events
   - Do NOT check multiple categories for one post

4. **Add tags** (optional):
   - In the right sidebar → Tags
   - Add 2–4 relevant tags: e.g., "Gurukula", "Vedas", "Maharudra"

5. **Add a featured image:**
   - Right sidebar → Featured Image → Set Featured Image
   - Every blog post MUST have a featured image
   - Use a warm, relevant photo (1200 × 630px ideal)

6. **Write the content:**
   - Use short paragraphs (3–4 sentences max)
   - Use Heading 2 (H2) for main sections
   - Use Heading 3 (H3) for sub-sections
   - Add images within the post where helpful
   - Add the `donate-cta-strip` synced pattern at the bottom

7. **Write a custom excerpt:**
   - Right sidebar → Excerpt
   - Write 1–2 sentences summarizing the post (this appears on the blog listing page)

8. **Fill in Yoast SEO:**
   - Scroll to the bottom
   - SEO Title: Include the primary keyword
   - Meta Description: 140–160 characters, compelling summary
   - Focus Keyphrase: Set one phrase this post targets

9. **Preview** the post on desktop and mobile

10. **Publish:**
    - Click "Publish"
    - Set visibility to "Public"
    - Publish immediately or schedule for a future date

### Blog Post Checklist (Copy This)

- [ ] Title is clear and descriptive
- [ ] One category selected
- [ ] 2–4 tags added
- [ ] Featured image uploaded (warm tones, 1200×630px)
- [ ] Content uses H2 and H3 headings
- [ ] Paragraphs are short and readable
- [ ] Custom excerpt written
- [ ] Yoast SEO title and description filled
- [ ] Donate CTA strip added at bottom
- [ ] Previewed on mobile
- [ ] Published

---

## 8. NAMING CONVENTIONS

Consistent naming makes the site easy to manage as it grows.

### Page Slugs (URLs)

| Page | Slug | Full URL |
|------|------|----------|
| Home | `/` | shivasankalpa.org |
| About | `/about` | shivasankalpa.org/about |
| Events | `/events` | shivasankalpa.org/events |
| Event detail | `/events/[event-name-year]` | shivasankalpa.org/events/maharudra-purascharana-2026 |
| Donate | `/donate` | shivasankalpa.org/donate |
| Gallery | `/gallery` | shivasankalpa.org/gallery |
| Blog | `/blog` | shivasankalpa.org/blog |
| Blog post | `/blog/[post-title-slug]` | shivasankalpa.org/blog/why-gurukulas-matter |
| Contact | `/contact` | shivasankalpa.org/contact |
| Gurukulas | `/gurukulas` | shivasankalpa.org/gurukulas |

### Media File Names

**Before uploading any image, rename it on your computer first.**

| Format | Example |
|--------|---------|
| `page-section-description.jpg` | `home-hero-students-chanting.jpg` |
| `event-name-description.jpg` | `maharudra-2026-homa-fire.jpg` |
| `gallery-category-description.jpg` | `gallery-gurukula-morning-prayers.jpg` |
| `trustee-firstname-lastname.jpg` | `trustee-harisha-harithasa.jpg` |
| `blog-slug-description.jpg` | `blog-gurukulas-matter-hero.jpg` |

**Never upload images with names like:**
- `IMG_3847.jpg`
- `WhatsApp Image 2026-04-10.jpg`
- `Screenshot 2026-04-10.png`
- `photo (1).jpg`

Rename them first. It takes 10 seconds and helps SEO and organization.

### Blog Post Slugs

| Good | Bad |
|------|-----|
| `why-vedic-gurukulas-matter` | `post-1` |
| `understanding-maharudra-purascharana` | `new-article` |
| `trust-update-may-2026` | `update` |

### Gallery Names

| Good | Bad |
|------|-----|
| `Maharudra Purascharana 2026` | `Gallery 1` |
| `Gurukula Daily Life` | `Photos` |
| `Trust Foundation Day` | `New Album` |

---

## 9. WHAT SHOULD NEVER BE EDITED DIRECTLY

These areas can break the site if modified incorrectly:

| Area | Why Not | What to Do Instead |
|------|---------|-------------------|
| **Appearance → Theme Editor** | Raw PHP/CSS code — one wrong character breaks the site | Use Customizer for visual changes |
| **Plugins → Plugin Editor** | Same — raw code | Never needed |
| **Settings → Permalinks** | Changing this breaks all existing URLs and SEO | Already set correctly — don't touch |
| **Settings → Reading** | Changing homepage/blog page settings disrupts the site | Already configured |
| **Astra → Global colors/fonts** | These affect the entire site — changing them changes everything | Only change if intentionally rebranding |
| **Synced Patterns content** | Changes propagate everywhere — edit intentionally | Always preview after editing a synced pattern |
| **Page slugs of existing pages** | Changing a slug (URL) breaks links and SEO | If you must change, set up a redirect |
| **wp-config.php** | Core configuration file | Only IT person should touch this |

### If Something Goes Wrong

1. **Don't panic.** WordPress has revision history.
2. Go to the page/post editor
3. In the right sidebar, click "Revisions" (under Post/Page settings)
4. Select a previous version and click "Restore this revision"
5. The page returns to its previous state

---

## 10. WHAT IS TEMPLATE-DRIVEN (SYNCED PATTERNS)

These content blocks are shared across multiple pages. **When you edit them, the change appears everywhere they are used.**

| Synced Pattern Name | Used On | Contains |
|--------------------|---------|----------|
| `donate-cta-strip` | Home, About, Events, Gallery, Blog posts | "Every contribution nurtures..." headline + Donate button |
| `trust-credibility-strip` | Home, About, Donate | Sringeri blessings, registration info, trustee names |
| `seva-options-table` | Events detail, Donate | Table of all seva types and amounts |
| `payment-methods` | Donate page (primary) | UPI ID, QR code, bank details |

### How to Edit a Synced Pattern

1. Open any page that contains the pattern
2. Click on the pattern block (you'll see a purple outline)
3. Click "Edit original" in the toolbar
4. Make changes
5. Click "Update"
6. All pages using this pattern are now updated

### How to Find All Synced Patterns

Go to **Appearance → Patterns** (or the block editor → Browse Patterns) to see and manage all synced patterns.

---

## 11. WEEKLY MAINTENANCE CHECKLIST

Print this or keep it bookmarked. Run through it every Monday (or any fixed day).

### Every Week — 15 minutes

- [ ] **Check for WordPress updates:** Dashboard → Updates. Update core, themes, plugins if available.
- [ ] **Review contact form entries:** WPForms → Entries. Respond to any pending messages.
- [ ] **Check the site visually:** Open shivasankalpa.org in an incognito/private browser. Does it load? Does it look right? Check on mobile too.
- [ ] **Check email delivery:** Send a test message via the contact form. Confirm it arrives at info@shivasankalpa.org.

### Every Month — 30 minutes

- [ ] **Review and update event information:** Is the featured event still current? Any new events to add?
- [ ] **Upload new gallery photos** if any are available.
- [ ] **Check Yoast SEO:** Any red/orange indicators on pages? Fix if easy.
- [ ] **Verify backups:** Go to UpdraftPlus → check that recent backups exist and are stored in Google Drive.
- [ ] **Review and clear spam** if any (in Comments, if enabled).

### Every Quarter — 1 hour

- [ ] **Review all page content:** Read through each page. Is anything outdated?
- [ ] **Update trustee bios** if needed.
- [ ] **Check Google Search Console** (if set up) for any crawl errors.
- [ ] **Delete unused media** from Media Library to keep it organized.
- [ ] **Test the donate page:** Are bank details correct? Does the QR code work?

---

## 12. QUICK REFERENCE CARD

Print this and keep it near your computer.

```
╔══════════════════════════════════════════════════════╗
║   SRI SHIVASANKALPA VṚNDA — ADMIN QUICK REFERENCE   ║
╠══════════════════════════════════════════════════════╣
║                                                      ║
║  LOGIN:  shivasankalpa.org/wp-admin                  ║
║  EMAIL:  info@shivasankalpa.org                      ║
║                                                      ║
║  COMMON TASKS:                                       ║
║  ─────────────────────────────────────────────────   ║
║  Edit a page       → Pages → [page name] → Edit     ║
║  New blog post      → Posts → Add New                ║
║  Upload photos      → Media → Add New                ║
║  Gallery photos     → Envira Gallery → [gallery]     ║
║  View messages      → WPForms → Entries              ║
║  Check backups      → Settings → UpdraftPlus         ║
║  Check updates      → Dashboard → Updates            ║
║                                                      ║
║  BEFORE PUBLISHING: Always click "Preview" first!    ║
║                                                      ║
║  SOMETHING BROKE?   Use Revisions to restore.        ║
║  (Page editor → right sidebar → Revisions)           ║
║                                                      ║
║  NEVER TOUCH:                                        ║
║  • Appearance → Theme Editor                         ║
║  • Plugins → Plugin Editor                           ║
║  • Settings → Permalinks                             ║
║  • Settings → Reading                                ║
║                                                      ║
║  NEED HELP?   Contact your IT support person.        ║
║                                                      ║
╚══════════════════════════════════════════════════════╝
```

---

## END OF PHASE 6
