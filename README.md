# AI Insights & Innovations Blog

A personal blog built with Hugo and the Stack theme.

## Quick Start

### Prerequisites
- [Hugo Extended](https://gohugo.io/getting-started/installing/) (v0.100.0+)
- [Go](https://golang.org/dl/) (v1.19+)

### Development

```bash
# Initialize modules
hugo mod get -u
hugo mod tidy

# Run development server
hugo server -D
```

Visit `http://localhost:1313` to preview.

## Content

- `content/post/` - Blog posts
- `content/page/` - Static pages
- `content/categories/` - Category definitions
- `config/_default/` - Configuration files
- `static/` - Static assets

## Create New Post

```bash
hugo new content/post/your-post-name/index.md
```

## Deployment

Configured for automatic deployment to GitHub Pages via GitHub Actions.

1. Go to repository Settings → Pages
2. Set source to "GitHub Actions"
3. Push to `main` branch to deploy

## Theme

Uses [Hugo Theme Stack](https://github.com/CaiJimmy/hugo-theme-stack). Update with:

```bash
hugo mod get -u github.com/CaiJimmy/hugo-theme-stack/v3
hugo mod tidy
```

## License

MIT License - see [LICENSE](LICENSE) file.
