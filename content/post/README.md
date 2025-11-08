# Adding New Blog Posts

This directory contains all your blog posts. Each post should be in its own folder.

## Quick Start: Adding a New Post

### Method 1: Using Hugo Command (Recommended)
```bash
hugo new content/post/your-post-name/index.md
```

### Method 2: Manual Creation
1. Create a new folder: `content/post/your-post-name/`
2. Create `index.md` inside that folder
3. Add your content with front matter

## Post Structure

Each post should follow this structure:
```
content/post/
└── your-post-name/
    ├── index.md          # Your post content
    └── cover.jpg         # (Optional) Cover image
```

## Front Matter Template

Every post needs front matter at the top. Copy this template:

```yaml
---
title: "Your Post Title"
description: "A brief description of your post"
slug: "your-post-slug"
date: 2025-01-15T00:00:00+00:00
draft: false
categories:
  - "Category Name"
tags:
  - "Tag 1"
  - "Tag 2"
image: "cover.jpg"  # Optional: if you have a cover image
---
```

## Important Notes

- **Folder name**: Use lowercase with hyphens (e.g., `my-awesome-post`)
- **File name**: Always name it `index.md`
- **Date format**: Use ISO 8601 format (YYYY-MM-DDTHH:MM:SS+00:00)
- **Draft**: Set `draft: true` to hide the post until ready
- **Categories**: Must match category names in `content/categories/`
- **Cover images**: Place in the same folder as `index.md` and reference in front matter

## Example

See `example-post/` folder for a complete example.

## Need Help?

- Check `STRUCTURE.md` in the root directory
- Review `GETTING_STARTED.md` for detailed instructions
- Visit Hugo docs: https://gohugo.io/content-management/

