# 🟢 NYX'S BLOG v2.0 - Setup & Deployment Guide

Your improved retro blog with better design, filtering, and features is ready!

---

## 📋 What's New in v2.0

✨ **Visual Improvements:**
- Modern retro aesthetic with smooth animations
- Better typography and spacing
- Responsive design (mobile-friendly)
- Animated scanline effect
- Color-coded category system

🎯 **New Features:**
- Category filtering (All, CEH, Pentest, Tools, Lab Setup)
- Post metadata with read time estimates
- Better navigation and typography
- Loading animations
- Improved post templates

🔧 **Technical:**
- Smooth gradient backgrounds
- CSS hover effects and transitions
- Better code block styling
- Mobile-responsive grid layout

---

## ⚡ QUICK DEPLOYMENT (Copy/Paste)

You're in your `itzNyx900.github.io` repo. Run these commands:

### Step 1: Replace Old Files

```bash
# Copy new index.html (replaces old one)
cp /home/claude/index-new.html ./index.html

# Copy new posts.json
cp /home/claude/posts-new.json ./posts.json

# Copy improved post template
cp /home/claude/posts/template.html ./posts/template.html

# Copy new welcome post
cp /home/claude/posts/welcome-new.html ./posts/welcome.html

# Copy pentest lab post
# (It already exists, just verify it's there)
```

### Step 2: Verify Files

```bash
ls -la
# Should see: index.html, posts.json, posts/

ls posts/
# Should see: welcome.html, pentest-lab.html, template.html, kali-setup.html
```

### Step 3: Push to GitHub (DEPLOY LIVE)

```bash
git add .
git commit -m "Update: Nyx's Blog v2.0 with improved design and features"
git push
```

✅ **Your site is now live!** Visit: `https://itzNyx900.github.io`

---

## 📝 How to Add New Posts in v2.0

### New Post Template Structure

Each post should have this structure in `posts/post-name.html`:

```html
<div class="post-category-tag">CATEGORY</div>
<h1>Your Post Title</h1>
<div class="post-meta">
    <div class="post-meta-item">📅 Date</div>
    <div class="post-meta-item">✍️ Author</div>
    <div class="post-meta-item">⏱️ X min read</div>
</div>
```

### Step-by-Step: Add a New Post

**1. Create the HTML file**

Copy the template from `posts/template.html` and save as `posts/your-post-name.html`

Edit the content (title, date, category, body text)

**2. Update posts.json**

Add an entry to `posts.json`:

```json
{
    "title": "Your Post Title",
    "author": "Sina",
    "date": "2026-06-20",
    "category": "pentest",
    "filename": "your-post-name.html",
    "excerpt": "Short description that shows on home page..."
}
```

**3. Available Categories**

Use one of these in your posts:
- `ceh` — CEH certification content
- `pentest` — Penetration testing techniques
- `tools` — Security tool guides
- `lab` — Lab setup and configuration
- `meta` — About the blog itself

**4. Deploy**

```bash
git add .
git commit -m "Add post: Your Post Title"
git push
```

Done! Your new post appears on the home page with filtering.

---

## 🎨 Styling Features

### In Your Posts, Use:

**Highlight important text:**
```html
<span class="highlight">Important text</span>
```
Result: Yellow highlighted text

**Code blocks:**
```html
<div class="code-block">
command or code here
</div>
```
Result: Monospace code with accent border

**Sections:**
```html
<h2>Main Section</h2>
<h3>Subsection</h3>
```

**Links:**
```html
<a href="https://example.com">Link text</a>
```

**Lists:**
```html
<ul>
    <li>Point one</li>
    <li>Point two</li>
</ul>
```

---

## 🔍 Post Metadata Explained

Each post in `posts.json` needs:

```json
{
    "title": "Exact title of post",
    "author": "Your name",
    "date": "YYYY-MM-DD format",
    "category": "one of: ceh, pentest, tools, lab, meta",
    "filename": "filename.html (in posts/ folder)",
    "excerpt": "50-100 word description for home page"
}
```

⚠️ **Important:**
- `date` format must be `YYYY-MM-DD`
- `filename` must match actual file in `posts/` folder
- `category` must be exact (lowercase, no spaces)
- Posts sort by newest first automatically

---

## 📱 Mobile Friendly

The blog is fully responsive. On mobile devices:
- Single column layout for posts
- Readable font sizes
- Touch-friendly buttons
- Same great retro aesthetic

---

## 🎛️ Customization

### Change Colors

In `index.html`, find the `:root` section:

```css
:root {
    --primary: #00ff41;      /* Main green */
    --secondary: #ffff00;    /* Yellow accents */
    --accent: #ff006e;       /* Pink for code */
    --text: #e0e0e0;         /* Light text */
    --muted: #888888;        /* Gray text */
}
```

Change these hex codes to your preferred colors.

### Change Header Text

In `index.html`, find:
```html
<div class="logo">[ SECURITY & HACKING ]</div>
<h1>NYX'S BLOG</h1>
<p class="tagline">CEH | Penetration Testing | Security Research</p>
```

Edit these lines to customize.

---

## 📚 File Structure

```
itzNyx900.github.io/
├── index.html          ← Home page with filtering
├── posts.json          ← Metadata for all posts
├── README.md           ← This file
└── posts/
    ├── welcome.html           ← Welcome post
    ├── pentest-lab.html       ← Lab setup guide
    ├── template.html          ← Copy this for new posts
    └── [your posts here]
```

---

## ✅ Checklist for New Posts

- [ ] Created HTML file in `posts/` folder
- [ ] Updated `posts.json` with metadata
- [ ] Set `date` in `YYYY-MM-DD` format
- [ ] Picked correct `category`
- [ ] `filename` matches actual file
- [ ] Tested links work (back button, etc.)
- [ ] `git add .`
- [ ] `git commit -m "Add post: [title]"`
- [ ] `git push`

---

## 🚀 You Now Have

✅ **Free hosting** — GitHub Pages (forever free)  
✅ **Custom domain** — itzNyx900.github.io  
✅ **Modern retro design** — Professional yet nostalgic  
✅ **Category filtering** — Easy navigation  
✅ **Mobile responsive** — Works everywhere  
✅ **Zero maintenance** — Just write posts  
✅ **Version controlled** — All changes tracked with git  

---

## 📖 Quick Reference: Common Tasks

**Add a new post:**
1. Copy `posts/template.html` → `posts/your-post.html`
2. Edit the content
3. Add to `posts.json`
4. `git add . && git commit -m "..." && git push`

**Edit an existing post:**
1. Open `posts/post-name.html`
2. Make changes
3. `git add . && git commit -m "Update: ..." && git push`

**Change blog title:**
Edit `index.html` header section

**Change colors:**
Edit `:root` variables in `index.html` style tag

---

**Happy blogging! 🎛️**

Questions? Check the files themselves — they're well-commented.
