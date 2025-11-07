# Blog Structure Overview

## Directory Tree

```
genli-xyz/
│
├── 📋 Documentation
│   ├── README.md              # Project overview
│   ├── QUICK_START.md         # 5-minute quick start
│   ├── GETTING_STARTED.md     # Comprehensive guide
│   ├── PROJECT_SUMMARY.md     # Technical summary
│   ├── STRUCTURE.md           # This file
│   └── LICENSE                # MIT License
│
├── ⚙️ Configuration
│   └── config/_default/
│       ├── config.toml        # Main site config
│       ├── params.toml        # Theme parameters
│       ├── menu.toml          # Navigation & social
│       ├── languages.toml     # Language settings
│       └── module.toml        # Hugo modules
│
├── 📝 Content
│   ├── post/                  # Blog posts
│   │   ├── hello-world/
│   │   ├── machine-learning-basics/
│   │   ├── deep-learning-overview/
│   │   ├── ai-ethics/
│   │   └── nlp-introduction/
│   │
│   ├── page/                  # Static pages
│   │   ├── about/
│   │   ├── archives/
│   │   └── search/
│   │
│   └── categories/            # Category definitions
│       ├── machine-learning/
│       ├── deep-learning/
│       ├── nlp/
│       └── ethics/
│
├── 🖼️ Static Assets
│   └── static/
│       ├── favicon.png        # (to be added)
│       └── img/
│           └── avatar.png     # (to be added)
│
├── 🎨 Theme Assets
│   └── assets/
│       └── icons/
│           └── brand-github.svg
│
├── 🤖 Automation
│   └── .github/workflows/
│       ├── deploy.yml         # Auto-deploy to GitHub Pages
│       └── update-theme.yml   # Daily theme updates
│
├── 🔧 Development
│   ├── .devcontainer/         # Codespace config
│   ├── .vscode/               # (ignored)
│   └── .gitignore
│
└── 📦 Hugo Modules
    ├── go.mod
    └── go.sum
```

## Key Files Explained

### Configuration Files

| File | Purpose |
|------|---------|
| `config.toml` | Site URL, title, copyright, pagination |
| `params.toml` | Sidebar, widgets, footer, comments, images |
| `menu.toml` | Navigation menu and social media links |
| `languages.toml` | Site language and description |
| `module.toml` | Hugo theme module import |

### Content Structure

#### Blog Posts (`content/post/`)
Each post is in its own directory:
```
post-name/
├── index.md           # Post content with front matter
└── cover.jpg          # (optional) Cover image
```

#### Static Pages (`content/page/`)
- `about/` - About page
- `archives/` - Auto-generated archive
- `search/` - Search functionality

#### Categories (`content/categories/`)
Each category can have its own:
- Title
- Description
- Image (optional)

### Static Assets (`static/`)

Everything in `static/` is copied to the site root:
- `favicon.png` → `/favicon.png`
- `img/avatar.png` → `/img/avatar.png`
- `img/photo.jpg` → `/img/photo.jpg`

### Generated Files (Ignored by Git)

| Directory | Contents |
|-----------|----------|
| `public/` | Built website (after running `hugo`) |
| `resources/` | Processed assets and cache |
| `.hugo_build.lock` | Build lock file |

## Content Front Matter

### Blog Post Example

```yaml
---
title: "Your Post Title"
description: Brief description
slug: url-slug
date: 2025-11-07 00:00:00+0000
image: cover.jpg              # Optional
categories:
    - Category Name
tags:
    - Tag 1
    - Tag 2
---
```

### Category Page Example

```yaml
---
title: Category Name
description: Category description
image: cover.jpg              # Optional
---
```

## Workflow

### Development
```
Write/Edit → hugo server → Preview → Commit → Push
```

### Production
```
Push to GitHub → GitHub Actions → Build → Deploy to Pages
```

## Where to Put Things

| What | Where |
|------|-------|
| Blog posts | `content/post/post-name/index.md` |
| Images for posts | `content/post/post-name/image.jpg` |
| Static images | `static/img/` |
| Favicon | `static/favicon.png` |
| Profile picture | `static/img/avatar.png` |
| About page | `content/page/about/index.md` |
| Site config | `config/_default/config.toml` |
| Navigation | `config/_default/menu.toml` |

## Common Tasks

### Add a New Post
1. Create directory: `content/post/post-name/`
2. Create file: `index.md`
3. Add front matter and content
4. (Optional) Add `cover.jpg` to the directory

### Add a New Category
1. Create directory: `content/categories/category-name/`
2. Create file: `_index.md`
3. Add front matter with title and description
4. Use category name in post front matter

### Customize Appearance
1. Sidebar: Edit `config/_default/params.toml` → `[sidebar]`
2. Colors: Advanced (requires theme customization)
3. Menu: Edit `config/_default/menu.toml`
4. Footer: Edit `config/_default/params.toml` → `[footer]`

## File Naming Conventions

- **Posts**: Use lowercase with hyphens (e.g., `my-post-name`)
- **Categories**: Use lowercase with hyphens (e.g., `machine-learning`)
- **Images**: Use descriptive names (e.g., `neural-network-diagram.png`)
- **Avoid**: Spaces, special characters, uppercase in URLs

## Best Practices

1. **One Post = One Directory**: Keep post and its assets together
2. **Descriptive Slugs**: Use clear, SEO-friendly URL slugs
3. **Consistent Categories**: Don't create too many categories
4. **Tags Liberally**: Use tags for specific topics
5. **Image Optimization**: Compress images before adding them
6. **Front Matter**: Always include title, description, date

## Git Workflow

```bash
# Check status
git status

# Stage changes
git add .

# Commit
git commit -m "Add new post about AI"

# Push (triggers auto-deployment)
git push
```

## Hugo Commands Reference

```bash
# Development
hugo server              # Start server
hugo server -D           # Include drafts
hugo server --port 8080  # Custom port

# Building
hugo                     # Build site
hugo --minify            # Build and minify
hugo --gc                # Clean cache and build

# Content
hugo new content/post/name/index.md    # New post
hugo new content/page/name/index.md    # New page

# Modules
hugo mod get -u          # Update all modules
hugo mod tidy            # Clean up modules
hugo mod graph           # Show module dependencies
```

## Need More Help?

- **Quick Start**: See `QUICK_START.md`
- **Full Guide**: See `GETTING_STARTED.md`
- **Technical Details**: See `PROJECT_SUMMARY.md`
- **Hugo Docs**: https://gohugo.io/documentation/
- **Theme Docs**: https://stack.jimmycai.com/

---

**Tip**: Keep this file as a reference while working on your blog!

