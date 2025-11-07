# Getting Started with Your AI Blog

This guide will help you customize your new AI-focused blog built with Hugo and the Stack theme.

## 📋 Table of Contents

1. [Initial Setup](#initial-setup)
2. [Customizing Site Information](#customizing-site-information)
3. [Adding Content](#adding-content)
4. [Managing Images](#managing-images)
5. [Deployment](#deployment)
6. [Tips and Tricks](#tips-and-tricks)

## Initial Setup

### Prerequisites

Make sure you have the following installed:
- Hugo Extended (v0.100.0+)
- Go (v1.19+)
- Git

### First Steps

1. **Update site URL**: Edit `config/_default/config.toml` and change `baseurl` to your actual site URL (e.g., `https://yourusername.github.io`)

2. **Update copyright**: In the same file, change `copyright` to your name

3. **Test locally**: Run `hugo server` and visit `http://localhost:1313`

## Customizing Site Information

### Site Title and Description

Edit `config/_default/config.toml`:
```toml
title = "Your Blog Title"
```

Edit `config/_default/languages.toml`:
```toml
[en.params]
description = "Your blog description"
```

### Sidebar

Edit `config/_default/params.toml`:
```toml
[sidebar]
emoji = "🤖"  # Change the emoji
subtitle = "Your custom subtitle"
```

### Navigation Menu

Edit `config/_default/menu.toml` to add, remove, or modify menu items.

### Social Links

In `config/_default/menu.toml`, update the `[[social]]` sections:
```toml
[[social]]
identifier = "github"
name = "GitHub"
url = "https://github.com/yourusername"
[social.params]
icon = "brand-github"
```

### Footer

Edit `config/_default/params.toml`:
```toml
[footer]
since = 2025  # Your start year
customText = "Your custom footer text"
```

## Adding Content

### Creating a New Post

Use Hugo's command:
```bash
hugo new content/post/your-post-name/index.md
```

Or manually create a directory and `index.md` file:
```
content/post/your-post-name/
├── index.md
└── cover.jpg (optional)
```

### Post Front Matter

Every post should have front matter like this:
```yaml
---
title: "Your Post Title"
description: A brief description
slug: your-post-slug
date: 2025-11-07 00:00:00+0000
categories:
    - AI
    - Machine Learning
tags:
    - Tutorial
    - Python
---
```

### Adding Categories

Create category pages in `content/categories/`:
```markdown
---
title: Your Category
description: Category description
---
```

### Post Structure

Current posts are placeholders. To fill them in:
1. Open any post in `content/post/`
2. Replace the placeholder text with your actual content
3. Use Markdown for formatting

## Managing Images

### Profile Picture

1. Create or find a square image (at least 200x200px)
2. Save it as `static/img/avatar.png`
3. It will automatically appear in the sidebar

### Favicon

1. Create a favicon (32x32 or 64x64px)
2. Save it as `static/favicon.png`

### Post Cover Images

1. Add an image to your post directory (e.g., `content/post/my-post/cover.jpg`)
2. Reference it in the front matter:
   ```yaml
   image: cover.jpg
   ```

### Images in Content

Place images in the post directory and reference them:
```markdown
![Image description](image-name.jpg)
```

Or use images from the static directory:
```markdown
![Image description](/img/image-name.png)
```

## Deployment

### GitHub Pages Setup

1. **Create a GitHub repository** named `yourusername.github.io`

2. **Push your code**:
   ```bash
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/yourusername/yourusername.github.io.git
   git push -u origin main
   ```

3. **Enable GitHub Pages**:
   - Go to repository Settings → Pages
   - Set source to "GitHub Actions"

4. **Configure permissions**:
   - Go to Settings → Actions → General
   - Under "Workflow permissions", select "Read and write permissions"
   - Save

5. **Deploy**: Push to main branch, and GitHub Actions will automatically build and deploy

### Custom Domain (Optional)

1. Add a `CNAME` file to `static/` with your domain name
2. Configure DNS settings with your domain provider
3. Update `baseurl` in `config/_default/config.toml`

## Tips and Tricks

### Writing Tips

1. **Keep titles concise**: Use clear, descriptive titles
2. **Add descriptions**: Front matter descriptions improve SEO
3. **Use categories wisely**: Don't create too many categories
4. **Tag appropriately**: Tags help readers find related content

### Content Organization

- Use categories for broad topics (e.g., "Machine Learning", "NLP")
- Use tags for specific subjects (e.g., "TensorFlow", "GPT", "Tutorial")
- Keep related posts in the same category

### Development Workflow

1. Create new post: `hugo new content/post/post-name/index.md`
2. Write content
3. Preview: `hugo server -D` (includes drafts)
4. When ready, remove `draft: true` from front matter
5. Commit and push

### Theme Updates

The theme automatically updates daily via GitHub Actions. To update manually:
```bash
hugo mod get -u github.com/CaiJimmy/hugo-theme-stack/v3
hugo mod tidy
```

### Building for Production

```bash
hugo --minify
```

Output will be in the `public/` directory.

### Troubleshooting

**Issue**: Site doesn't build
- Check for YAML errors in front matter
- Ensure all required fields are present
- Run `hugo` to see error messages

**Issue**: Images don't show
- Verify image files exist
- Check file paths in front matter
- Ensure images are valid formats (JPG, PNG, WebP)

**Issue**: Changes don't appear
- Clear Hugo cache: `hugo --gc`
- Restart the server
- Check browser cache

## Next Steps

1. Update the About page (`content/page/about/index.md`)
2. Add your profile picture and favicon
3. Write your first real post
4. Customize colors and styles (advanced - see theme documentation)
5. Set up analytics (optional)
6. Configure comments system (optional)

## Resources

- [Hugo Documentation](https://gohugo.io/documentation/)
- [Stack Theme Documentation](https://stack.jimmycai.com/)
- [Markdown Guide](https://www.markdownguide.org/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)

## Getting Help

- Check the [Hugo Forums](https://discourse.gohugo.io/)
- Stack Theme [GitHub Issues](https://github.com/CaiJimmy/hugo-theme-stack/issues)
- Hugo [Discord Server](https://discord.gg/hugo)

---

Happy blogging! 🚀

