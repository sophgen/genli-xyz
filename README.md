# AI Insights & Innovations Blog

A personal blog exploring Artificial Intelligence, Machine Learning, and emerging technologies. Built with Hugo and the Stack theme.

## 🚀 Quick Start

### Prerequisites

- [Hugo Extended](https://gohugo.io/getting-started/installing/) (v0.100.0 or later)
- [Go](https://golang.org/dl/) (v1.19 or later)

### Local Development

1. Clone this repository:
```bash
git clone https://github.com/your-username/genli-xyz.git
cd genli-xyz
```

2. Initialize Hugo modules:
```bash
hugo mod get -u
hugo mod tidy
```

3. Run the development server:
```bash
hugo server -D
```

4. Open your browser and visit `http://localhost:1313`

## 📝 Content Structure

- `/content/post/` - Blog posts
- `/content/page/` - Static pages (About, Archives, Search)
- `/content/categories/` - Category definitions
- `/config/_default/` - Configuration files
- `/static/` - Static assets (images, favicon, etc.)

## ✨ Features

- Modern, responsive design
- Dark mode support
- Full-text search
- Category and tag organization
- Archive page
- Customizable sidebar
- Social media integration
- GitHub Actions for automatic deployment

## 🎨 Customization

### Update Site Information

Edit the following files to customize your site:

- `config/_default/config.toml` - Basic site configuration
- `config/_default/params.toml` - Theme parameters
- `config/_default/menu.toml` - Navigation menu
- `content/page/about/index.md` - About page content

### Add New Posts

Create a new post:

```bash
hugo new content/post/your-post-name/index.md
```

### Images

- Replace `static/favicon.png` with your site favicon (recommended: 32x32 or 64x64 PNG)
- Replace `static/img/avatar.png` with your profile picture (recommended: square, at least 200x200 PNG)
- Add post cover images to each post directory (e.g., `content/post/your-post/cover.jpg`)
- To add a cover image to a post, place an image file in the post directory and add `image: cover.jpg` to the front matter

**Note:** The blog is currently set up without cover images. You can add them later by placing actual image files in each post directory and updating the front matter.

## 🚢 Deployment

This blog is configured to automatically deploy to GitHub Pages using GitHub Actions.

### Setup GitHub Pages

1. Go to your repository Settings → Pages
2. Set the source to "GitHub Actions"
3. Push to the `main` branch to trigger deployment

### Manual Build

To build the site manually:

```bash
hugo --minify
```

The static site will be generated in the `public/` directory.

## 📚 Theme

This blog uses the [Hugo Theme Stack](https://github.com/CaiJimmy/hugo-theme-stack) theme. The theme is loaded as a Hugo module for easy updates.

### Update Theme

To update the theme to the latest version:

```bash
hugo mod get -u github.com/CaiJimmy/hugo-theme-stack/v3
hugo mod tidy
```

The theme also updates automatically every day via GitHub Actions.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Hugo](https://gohugo.io/) - The static site generator
- [Hugo Theme Stack](https://github.com/CaiJimmy/hugo-theme-stack) - The beautiful theme
- [GitHub Pages](https://pages.github.com/) - Hosting platform

---

Built with ❤️ and AI
