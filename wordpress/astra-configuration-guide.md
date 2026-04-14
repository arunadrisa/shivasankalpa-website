# ASTRA CONFIGURATION GUIDE
# Step-by-step setup for Sri Shivasankalpa Vṛnda

> Complete this BEFORE building any pages.
> Time required: ~45 minutes

---

## STEP 1 — Install Required Plugins

Go to **Plugins → Add New** and install + activate each:

1. Search "Spectra" → Install → Activate
2. Search "Yoast SEO" → Install → Activate
3. Search "WPForms Lite" → Install → Activate
4. Search "WP Mail SMTP" → Install → Activate
5. Search "Envira Gallery Lite" → Install → Activate
6. Search "ShortPixel Image Optimizer" → Install → Activate
7. Search "UpdraftPlus" → Install → Activate
8. Search "WPCode" (by WPCode) → Install → Activate

Verify "LiteSpeed Cache" is already installed by Hostinger. If not, install it.

**Delete** these if present: Hello Dolly, Akismet (unless you want comment spam protection).

---

## STEP 2 — Astra Customizer Settings

Go to **Appearance → Customize**

### 2a. Global → Colors

| Setting | Value |
|---------|-------|
| Theme Color (Primary/Accent) | `#C4841D` |
| Link Color | `#B8621B` |
| Link Hover Color | `#C4841D` |
| Heading Color | `#3D2B1F` |
| Text Color | `#2C2C2C` |
| Background Color | `#FAF6F0` |

### 2b. Global → Typography

**Base Typography (Body):**
| Setting | Value |
|---------|-------|
| Font Family | Source Sans 3 |
| Font Weight | 400 (Regular) |
| Font Size | 17px |
| Line Height | 1.7 |

**Heading Typography (applies to all headings):**
| Setting | Value |
|---------|-------|
| Font Family | Cormorant Garamond |
| Font Weight | 600 (Semi-Bold) |
| Line Height | 1.25 |

> Note: Astra loads Google Fonts automatically when you select them.

### 2c. Global → Container

| Setting | Value |
|---------|-------|
| Container Width | 1200px |
| Container Layout | Normal |
| Content Layout (default for pages) | Full Width / Contained |

### 2d. Global → Buttons

| Setting | Value |
|---------|-------|
| Button Text Color | `#FFFFFF` |
| Button Background Color | `#C4841D` |
| Button Hover Text Color | `#FFFFFF` |
| Button Hover Background | `#A86E15` |
| Border Radius | 4px |
| Padding | 14px top/bottom, 32px left/right |
| Font Family | Source Sans 3 |
| Font Weight | 600 |

### 2e. Header Builder

Go to **Appearance → Customize → Header Builder**

**Layout:**
- Row 1 (Primary Header): Logo on LEFT, Primary Menu on RIGHT
- Sticky Header: Enable (if available in free version, otherwise skip)

**Logo Area:**
- Until you have a logo, go to **Site Identity → Site Title**
- Set Site Title: `Sri Shivasankalpa Vṛnda`
- Uncheck "Display Site Tagline" (we'll show it elsewhere)
- Upload Favicon: a 512×512 px icon (when ready)

**Primary Menu:**
- Will be configured after creating pages (see Menu Setup below)

### 2f. Footer Builder

Go to **Appearance → Customize → Footer Builder**

**Footer Widgets (Above Footer):**
- Layout: 4 columns (25% | 25% | 25% | 25%)
- Background Color: `#3D2B1F`
- Text Color: `#FAF6F0`
- Link Color: `rgba(250, 246, 240, 0.75)`
- Link Hover Color: `#C4841D`
- Top/Bottom Padding: 60px

**Copyright Bar (Below Footer):**
- Layout: 1 column centered
- Text: `© 2026 Sri Shivasankalpa Vṛnda · तन्मे मनः शिवसंकल्पमस्तु`
- Background Color: `#33231A` (slightly darker than footer)
- Text Color: `rgba(250, 246, 240, 0.6)`
- Font Size: 14px
- Padding: 16px

### 2g. Blog / Archive Settings

Go to **Appearance → Customize → Blog**

**Blog / Archive:**
| Setting | Value |
|---------|-------|
| Layout | Grid |
| Grid Columns | 3 |
| Post Content | Excerpt |
| Excerpt Length | 25 words |
| Show Featured Image | Yes |
| Show Date | Yes |
| Show Author | No (trust is the author) |
| Show Categories | Yes |

**Single Post:**
| Setting | Value |
|---------|-------|
| Content Width | Full Width |
| Sidebar | Right Sidebar (or No Sidebar — your choice) |
| Show Featured Image | Yes |
| Show Categories | Yes |
| Show Tags | Yes |
| Show Author Bio | No |

### 2h. Sidebar

Go to **Appearance → Customize → Sidebar**

| Setting | Value |
|---------|-------|
| Default Sidebar Layout (Pages) | No Sidebar |
| Default Sidebar Layout (Posts) | Right Sidebar |
| Default Sidebar Layout (Archives) | No Sidebar |

### 2i. Breadcrumbs

1. Go to Yoast SEO → Settings → Breadcrumbs → Enable
2. Go to Astra Customizer → Breadcrumbs → Enable Breadcrumbs → Position: After Header
3. This gives automatic "Home > About Us" navigation on every page

---

## STEP 3 — Paste Custom CSS

Go to **Appearance → Customize → Additional CSS**

1. Open the file `custom-styles.css` from this project
2. Select ALL the content (Ctrl+A / Cmd+A)
3. Paste it into the Additional CSS box
4. Click "Publish"

This immediately applies the Sacred Earth design system to your entire site.

---

## STEP 4 — Create Pages (Empty First)

Go to **Pages → Add New** and create these pages. Just set the title and publish — we'll add content next:

| Page Title | Slug | Parent Page |
|-----------|------|-------------|
| Home | (will be set as front page) | None |
| About Us | `about` | None |
| Events | `events` | None |
| Maharudra Purascharana 2026 | `maharudra-purascharana-2026` | Events |
| Donate | `donate` | None |
| Gallery | `gallery` | None |
| Contact | `contact` | None |
| Blog | (will be set as posts page) | None |

**For each page** (except Blog): In the page editor right sidebar:
- Page Attributes → Template: Default or Full Width
- Astra Settings (below content) → Sidebar: No Sidebar
- Astra Settings → Content Layout: Full Width / Stretched
- Astra Settings → Disable Title: YES (we'll add titles within the content)

---

## STEP 5 — Set Homepage and Blog Page

Go to **Settings → Reading:**

| Setting | Value |
|---------|-------|
| Your homepage displays | A static page |
| Homepage | Home |
| Posts page | Blog |

---

## STEP 6 — Set Permalink Structure

Go to **Settings → Permalinks:**

| Setting | Value |
|---------|-------|
| Permalink Structure | Post name |

(If already set, do NOT change it.)

For the Blog page to use `/blog/post-slug` URLs:
- This requires the Blog page slug to be `blog` (which it is by default)
- Posts will automatically use the Post name structure

---

## STEP 7 — Create Menus

Go to **Appearance → Menus**

### Primary Menu

1. Click "Create a new menu"
2. Name: `Primary Menu`
3. Add pages in this order: About Us, Events, Gallery, Blog, Contact, Donate
4. **For the Donate menu item:** click the dropdown arrow → in "CSS Classes" field, type: `donate-menu-btn`
   - If you don't see CSS Classes: click "Screen Options" at top right → check "CSS Classes"
5. Check "Primary Menu" under Menu Settings → Display Location
6. Save Menu

### Footer Quick Links

1. Create new menu: `Footer Quick Links`
2. Add: Home, About Us, Events, Gallery, Blog, Contact
3. Assign to a footer menu location (or use in a widget)

### Footer Get Involved

1. Create new menu: `Footer Get Involved`
2. Add: Donate
3. Add Custom Links:
   - URL: `/contact` | Link Text: "Volunteer"
   - URL: `#` | Link Text: "Spread the Word"
4. Assign to footer widget

---

## STEP 8 — Footer Widgets

Go to **Appearance → Widgets** (or Customize → Footer Builder → Widgets)

**Footer Column 1:**
- Add a "Text" or "Custom HTML" widget
- Title: (leave empty)
- Content:
```html
<p style="font-family: 'Cormorant Garamond', serif; font-size: 1.3rem; color: #FAF6F0; font-weight: 600;">
  Sri Shivasankalpa Vṛnda
</p>
<p class="sv-footer-tagline">तन्मे मनः शिवसंकल्पमस्तु</p>
<p style="font-size: 0.9rem; margin-top: 12px; color: rgba(250,246,240,0.7);">
  Supporting Vedic Gurukulas.<br>
  Preserving the Guru–Shishya Paramparā.
</p>
```

**Footer Column 2:**
- Add "Navigation Menu" widget
- Title: Quick Links
- Select: Footer Quick Links menu

**Footer Column 3:**
- Add "Navigation Menu" widget
- Title: Get Involved
- Select: Footer Get Involved menu

**Footer Column 4:**
- Add "Custom HTML" widget
- Title: Connect
- Content:
```html
<p style="color: rgba(250,246,240,0.75); font-size: 0.95rem;">
  <strong style="color: #FAF6F0;">Email:</strong><br>
  <a href="mailto:info@shivasankalpa.org">info@shivasankalpa.org</a>
</p>
<p style="color: rgba(250,246,240,0.75); font-size: 0.95rem; margin-top: 16px;">
  <strong style="color: #FAF6F0;">Location:</strong><br>
  Bengaluru, India
</p>
```

---

## STEP 9 — Configure Plugins

### Yoast SEO

1. Go to Yoast SEO → First-time configuration (run the wizard)
2. Site type: Organization
3. Organization name: Sri Shivasankalpa Vṛnda
4. Skip social profiles for now (add later)
5. Enable XML Sitemaps (should be on by default)
6. Go to Yoast → Settings → Breadcrumbs → Enable

### WP Mail SMTP

1. Go to WP Mail SMTP → Settings
2. From Email: `info@shivasankalpa.org`
3. From Name: `Sri Shivasankalpa Vṛnda`
4. Mailer: Other SMTP
5. SMTP Host: `smtp.hostinger.com`
6. Encryption: SSL
7. SMTP Port: 465
8. SMTP Authentication: ON
9. Username: `info@shivasankalpa.org`
10. Password: (your email password)
11. Save → Send Test Email to verify

### WPForms

1. Go to WPForms → Add New
2. Name: Contact Form
3. Choose "Simple Contact Form" template
4. Modify fields:
   - Name (required)
   - Email (required)
   - Add Dropdown field: Label "Subject", Options: General Inquiry, Donation Query, Volunteer, Event Inquiry, Other
   - Message / Comment (required)
5. Settings → Notifications → Send to: `info@shivasankalpa.org`
6. Settings → Confirmations → Message: "Thank you for reaching out to Sri Shivasankalpa Vṛnda. We typically respond within 2 business days."
7. Save

### ShortPixel

1. Go to Settings → ShortPixel
2. Get a free API key from shortpixel.com (100 images/month free)
3. Enter the API key
4. Compression Type: Lossy
5. Create WebP: Yes
6. Resize large images: Yes, max 2048px
7. Save

### UpdraftPlus

1. Go to Settings → UpdraftPlus Backups
2. Files backup schedule: Weekly, retain 4
3. Database backup schedule: Daily, retain 14
4. Remote storage: Google Drive → Authenticate
5. Click "Backup Now" to create first backup

### LiteSpeed Cache

1. Go to LiteSpeed Cache → Cache
2. Enable Page Cache: ON
3. Enable CSS/JS Minification: ON (under Page Optimization)
4. Enable Lazy Load Images: ON (under Page Optimization)
5. Save

---

## STEP 10 — Build Pages

You're now ready to build pages. Open each page file in the `wordpress/pages/` folder and follow the instructions to paste the block markup into the Code Editor.

### How to use the page HTML files:

1. Go to Pages → [Page Name] → Edit
2. In the top right, click the **three dots (⋮)** menu
3. Select **"Code editor"**
4. Delete any existing content
5. Copy the ENTIRE contents of the corresponding HTML file
6. Paste into the code editor
7. Click **"Exit code editor"** (top right) to switch back to visual mode
8. Review and adjust — replace placeholder images, tweak text if needed
9. Click **Update** to save

---

## DONE!

After completing these steps, proceed to build each page using the HTML templates provided.
