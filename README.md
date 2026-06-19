# 🟢 RETRO BLOG - Setup & Usage Guide

Your green-screen blog is ready! Follow these steps.

---

## STEP 1: Copy Files to Your Repo

You should be in your `username.github.io` directory. Copy the files I created:

```bash
# From wherever you downloaded these files:
cp index.html ~/username.github.io/
cp posts.json ~/username.github.io/
cp -r posts/ ~/username.github.io/
```

(Replace `username` with your actual GitHub username)

Check it worked:
```bash
ls -la
# You should see: index.html, posts.json, posts/
```

---

## STEP 2: Push to GitHub

```bash
cd ~/username.github.io
git add .
git commit -m "Add retro blog"
git push
```

Your site is now LIVE at: `https://username.github.io`

Visit it in your browser! You should see the retro green screen theme.

---

## STEP 3: Add Your First Post

The blog already has 2 sample posts. To add your own:

### A) Create the post file

In the `posts/` folder, create a new HTML file. Copy this template:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your Post Title</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { background: #1a1a1a; color: #00ff00; font-family: 'Courier New', monospace; line-height: 1.8; padding: 20px; border: 3px solid #00ff00; }
        .post-container { max-width: 800px; margin: 0 auto; }
        h1 { font-size: 2.5em; margin-bottom: 10px; text-shadow: 0 0 10px #00ff00; }
        .post-meta { color: #888; margin-bottom: 30px; border-bottom: 2px dashed #00ff00; padding-bottom: 15px; }
        .post-content { line-height: 1.8; margin-bottom: 30px; }
        .post-content p { margin-bottom: 15px; }
        .post-content h2 { color: #ffff00; margin-top: 25px; margin-bottom: 10px; }
        .code-block { background: #000; border: 1px solid #00ff00; padding: 15px; margin: 15px 0; overflow-x: auto; }
        .back-link { display: inline-block; margin-bottom: 20px; }
        .back-link a { color: #00ff00; font-size: 1.1em; }
        a { color: #ffff00; text-decoration: underline; }
        footer { border-top: 2px dashed #00ff00; padding-top: 15px; color: #888; }
    </style>
</head>
<body>
    <div class="post-container">
        <div class="back-link">
            <a href="../index.html">← Back to Blog</a>
        </div>
        <h1>Your Post Title Here</h1>
        <div class="post-meta">
            By Sina | Published on June 20, 2026 | Tags: #tag1 #tag2
        </div>
        <div class="post-content">
            <p>Write your content here. Use paragraphs, lists, code blocks.</p>
            <h2>Section Title</h2>
            <p>More content...</p>
            <div class="code-block">
code example here
            </div>
        </div>
        <footer>
            <p>[ END OF POST ]</p>
        </footer>
    </div>
</body>
</html>
```

### B) Update posts.json

Open `posts.json` and add your new post:

```json
[
    {
        "title": "Your New Post Title",
        "author": "Sina",
        "date": "2026-06-20",
        "filename": "your-post-name.html",
        "excerpt": "A short description of your post that appears on the home page."
    },
    ...rest of posts...
]
```

### C) Push it live

```bash
git add .
git commit -m "Add new post: Your Post Title"
git push
```

Done! Your post appears on the home page automatically.

---

## QUICK REFERENCE: Add a Post

Every time you write a new post:

1. **Create file**: `posts/post-name.html` (use the template above)
2. **Edit**: Write your content
3. **Add to posts.json**: Add the metadata
4. **Push**:
   ```bash
   git add .
   git commit -m "Add: Post Title"
   git push
   ```

That's it!

---

## Tips

- **File names**: Use lowercase, hyphens (no spaces): `my-post.html`
- **Dates**: Use `YYYY-MM-DD` format in posts.json
- **Tags**: Add tags after `#` in the meta section
- **Links**: Use `<a href="../index.html">link</a>` to go back
- **Code blocks**: Use `<div class="code-block">code here</div>`

---

## You Now Have:

✅ Free hosting (GitHub Pages)  
✅ Custom domain (username.github.io)  
✅ Retro theme (green screen aesthetic)  
✅ No payment required  
✅ Full control  
✅ Version control (git)  

**Start writing!** 🎛️
