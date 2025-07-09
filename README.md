# Lucain Pan's Technical Blog

A personal blog focused on technical reports, thoughts, and insights about software development and technology.

## 🚀 Live Site

Visit the blog at: [https://lucainpan.github.io](https://lucainpan.github.io)

## 📝 About

This blog serves as a platform to share:
- Technical reports and analyses
- Software development insights
- Programming tips and best practices
- Technology trends and thoughts
- Personal projects and experiments

## 🛠 Technical Stack

- **Static Site Generator**: [Jekyll](https://jekyllrb.com/)
- **Hosting**: [GitHub Pages](https://pages.github.com/)
- **Styling**: Custom CSS with responsive design
- **Content**: Written in Markdown

## 🏗 Project Structure

```
lucainpan.github.io/
├── _config.yml          # Site configuration
├── Gemfile             # Ruby dependencies
├── index.md            # Homepage
├── about.md            # About page
├── posts.md            # All posts page
├── _layouts/           # HTML templates
│   ├── default.html    # Base layout
│   ├── post.html       # Blog post layout
│   └── page.html       # Static page layout
├── _posts/             # Blog posts
│   └── *.md           # Individual posts
└── assets/
    └── css/
        └── style.css   # Custom styles
```

## 🚀 Local Development

### Prerequisites

- Ruby (version 2.7 or higher)
- Bundler gem

### Setup

1. Clone the repository:
```bash
git clone https://github.com/lucainpan/lucainpan.github.io.git
cd lucainpan.github.io
```

2. Install dependencies:
```bash
bundle install
```

3. Run the development server:
```bash
bundle exec jekyll serve
```

4. Open your browser and visit `http://localhost:4000`

### Creating a New Post

1. Create a new file in the `_posts` directory following the naming convention:
   ```
   YYYY-MM-DD-title-of-post.md
   ```

2. Add front matter at the top of the file:
   ```yaml
   ---
   layout: post
   title: "Your Post Title"
   date: 2025-01-09 12:00:00 +0800
   tags: [tag1, tag2, tag3]
   excerpt: "A brief description of your post"
   ---
   ```

3. Write your content in Markdown below the front matter.

4. Commit and push to GitHub for automatic deployment.

## 📚 Features

- **Responsive Design**: Works on desktop and mobile devices
- **Syntax Highlighting**: Code blocks with Rouge syntax highlighter
- **SEO Optimized**: Meta tags and sitemap generation
- **RSS Feed**: Automatic feed generation for subscribers
- **Tag System**: Categorize posts with tags
- **Navigation**: Easy navigation between posts
- **Social Sharing**: Share posts on social media

## 🎨 Customization

### Updating Site Information

Edit `_config.yml` to update:
- Site title and description
- Author information
- Social media links
- Build settings

### Styling

Modify `assets/css/style.css` to customize:
- Colors and typography
- Layout and spacing
- Responsive breakpoints
- Component styling

### Adding Pages

Create new `.md` files in the root directory with appropriate front matter:
```yaml
---
layout: page
title: "Page Title"
permalink: /page-url/
---
```

## 🤝 Contributing

If you find any issues or have suggestions for improvements:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 📬 Contact

- GitHub: [@lucainpan](https://github.com/lucainpan)
- Email: [your.email@example.com](mailto:your.email@example.com)

---

Built with ❤️ using Jekyll and GitHub Pages.
