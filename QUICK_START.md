# Quick Start Guide

## 🚀 Get Running in 5 Minutes

### 1. Preview Your Blog Locally

```bash
hugo server
```

Then visit: http://localhost:1313

### 2. Create Your First Post

```bash
hugo new content/post/my-first-post/index.md
```

Edit the new file and add your content!

### 3. Build for Production

```bash
hugo --minify
```

## ⚙️ Essential Customizations

### Update Site URL

Edit `config/_default/config.toml`:
```toml
baseurl = "https://yourusername.github.io"
copyright = "© Your Name"
```

### Update About Page

Edit `content/page/about/index.md` with your information.

### Add Your Social Links

Edit `config/_default/menu.toml` and update the `[[social]]` sections with your URLs.

## 📸 Add Images

1. **Profile Picture**: Add `static/img/avatar.png` (200x200+ recommended)
2. **Favicon**: Add `static/favicon.png` (32x32 or 64x64)
3. **Post Covers**: Add image to post folder and add `image: filename.jpg` to front matter

## 🚢 Deploy to GitHub Pages

1. Create a repository named `yourusername.github.io`
2. Push your code:
   ```bash
   git remote add origin https://github.com/yourusername/yourusername.github.io.git
   git push -u origin main
   ```
3. Go to Settings → Pages → Set source to "GitHub Actions"
4. Go to Settings → Actions → General → Set "Read and write permissions"
5. Done! Your site will auto-deploy on every push

## 📚 More Details

- Full customization guide: `GETTING_STARTED.md`
- Project overview: `PROJECT_SUMMARY.md`
- Theme documentation: https://stack.jimmycai.com/

## ⌨️ Useful Commands

```bash
# Start development server
hugo server

# Start server with drafts
hugo server -D

# Build for production
hugo --minify

# Create new post
hugo new content/post/post-name/index.md

# Update theme
hugo mod get -u github.com/CaiJimmy/hugo-theme-stack/v3
hugo mod tidy

# Clean cache
hugo --gc
```

## 🎨 Current Placeholder Content

The blog comes with 5 placeholder posts about AI:
1. Welcome to My AI Blog
2. Understanding Machine Learning Fundamentals
3. Deep Learning: An Overview
4. AI Ethics and Responsible Development
5. Natural Language Processing Fundamentals

Feel free to edit or delete these and add your own content!

---

**Need help?** Check `GETTING_STARTED.md` for detailed instructions.

