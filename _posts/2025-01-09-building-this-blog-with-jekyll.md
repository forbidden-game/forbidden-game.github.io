---
layout: post
title: "Building This Blog with Jekyll and GitHub Pages"
date: 2025-01-09 17:00:00 +0800
tags: [jekyll, github-pages, blogging, tutorial]
excerpt: "A detailed walkthrough of how I built this blog using Jekyll and GitHub Pages, including the design decisions and technical implementation details."
---

# Building This Blog with Jekyll and GitHub Pages

In this post, I'll walk you through how I built this blog using Jekyll and GitHub Pages. This serves as both documentation of my process and a tutorial for anyone looking to create their own technical blog.

## Why Jekyll and GitHub Pages?

I chose this combination for several reasons:

### Jekyll Benefits
- **Markdown Support**: Write posts in Markdown, which is perfect for technical content
- **Static Site Generation**: Fast loading times and excellent performance
- **Flexible Templating**: Full control over the design and layout
- **Built-in Features**: Syntax highlighting, RSS feeds, and SEO optimization

### GitHub Pages Benefits
- **Free Hosting**: No hosting costs for personal blogs
- **Automatic Deployment**: Push to GitHub and the site updates automatically
- **Version Control**: All content is version-controlled with Git
- **Custom Domains**: Easy to set up custom domain names

## Project Structure

Here's the structure I implemented:

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

## Key Configuration Decisions

### Site Configuration (`_config.yml`)

```yaml
# Essential settings
title: Lucain Pan's Technical Blog
description: A personal blog focused on technical reports and insights
url: "https://lucainpan.github.io"

# Markdown processing
markdown: kramdown
highlighter: rouge
kramdown:
  input: GFM
  syntax_highlighter: rouge
  syntax_highlighter_opts:
    block:
      line_numbers: true
```

This configuration enables:
- GitHub Flavored Markdown (GFM) for familiar syntax
- Rouge syntax highlighter for code blocks
- Line numbers in code blocks for better readability

### Gemfile Dependencies

```ruby
gem "jekyll", "~> 4.3.2"
gem "minima", "~> 2.5"

group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
end
```

Essential plugins:
- `jekyll-feed`: Generates RSS feed automatically
- `jekyll-sitemap`: Creates sitemap.xml for SEO
- `jekyll-seo-tag`: Adds SEO-friendly meta tags

## Design Philosophy

### Clean and Readable
I prioritized readability for technical content:
- Clean typography with system fonts
- Proper line spacing and margins
- Code syntax highlighting
- Mobile-responsive design

### Technical Content Focus
The design accommodates technical writing:
- Syntax-highlighted code blocks
- Proper styling for blockquotes and lists
- Tag system for categorizing posts
- Navigation between related posts

## Custom Styling Highlights

### Code Block Styling
```css
pre {
  background-color: #f8f9fa;
  padding: 1rem;
  border-radius: 5px;
  overflow-x: auto;
  margin-bottom: 1rem;
  border-left: 4px solid #3498db;
}
```

### Responsive Navigation
```css
@media (max-width: 768px) {
  .site-header .container {
    flex-direction: column;
    gap: 1rem;
  }
}
```

## Content Strategy

### Post Structure
Each post follows a consistent structure:
- Clear title and metadata
- Excerpt for homepage display
- Tags for categorization
- Proper heading hierarchy
- Code examples with syntax highlighting

### Writing Workflow
1. Create new file: `_posts/YYYY-MM-DD-title.md`
2. Add front matter with metadata
3. Write content in Markdown
4. Commit and push to GitHub
5. Site updates automatically

## GitHub Pages Setup

### Repository Configuration
1. Repository name: `username.github.io`
2. Enable GitHub Pages in settings
3. Source: Deploy from branch (main)
4. Custom domain (optional)

### Deployment Process
```bash
# Local development
bundle install
bundle exec jekyll serve

# Production deployment
git add .
git commit -m "Add new post"
git push origin main
```

## Performance Considerations

### Static Site Benefits
- Fast loading times (no server-side processing)
- Excellent caching capabilities
- CDN distribution through GitHub Pages
- Minimal resource requirements

### Optimization Techniques
- Minified CSS
- Optimized images
- Efficient HTML structure
- Semantic markup for SEO

## Future Enhancements

### Planned Features
- [ ] Comment system integration
- [ ] Search functionality
- [ ] Archive by tags/categories
- [ ] Reading time estimates
- [ ] Social sharing buttons

### Technical Improvements
- [ ] Advanced syntax highlighting themes
- [ ] Dark mode toggle
- [ ] Progressive Web App features
- [ ] Analytics integration

## Lessons Learned

### What Worked Well
- Jekyll's simplicity and flexibility
- GitHub Pages seamless integration
- Markdown workflow efficiency
- Clean, minimal design approach

### Challenges Faced
- Initial setup complexity
- CSS specificity issues
- Responsive design considerations
- SEO optimization details

## Conclusion

Building this blog with Jekyll and GitHub Pages has been a rewarding experience. The combination provides an excellent platform for technical blogging with minimal maintenance overhead.

The focus on content over complexity aligns perfectly with my goal of sharing technical insights without getting bogged down in blog management tasks.

## Resources

- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Jekyll Themes](https://jekyllthemes.io/)
- [Markdown Guide](https://www.markdownguide.org/)

---

*Want to build your own Jekyll blog? Feel free to fork this blog's [source code](https://github.com/lucainpan/lucainpan.github.io) as a starting point.*
