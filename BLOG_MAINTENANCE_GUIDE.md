# Blog Maintenance Guide

## Table of Contents
1. [Quick Start](#quick-start)
2. [Writing Posts](#writing-posts)
3. [Local Development](#local-development)
4. [Publishing](#publishing)
5. [Customization](#customization)
6. [Troubleshooting](#troubleshooting)

## Quick Start

### Essential Commands
```bash
# Write a new post
# Create file in _posts/ with format: YYYY-MM-DD-title.md

# Preview locally
bundle exec jekyll serve

# Publish
git add .
git commit -m "Add new post: [title]"
git push origin main
```

## Writing Posts

### 1. Create a New Post
Posts must be in the `_posts/` directory with the naming format: `YYYY-MM-DD-title-of-post.md`

Example: `2024-01-15-my-first-post.md`

### 2. Post Structure
Every post needs front matter at the top:

```markdown
---
layout: post
title: "Your Post Title"
date: 2024-01-15 10:00:00 +0000
categories: [tech, tutorial]  # Optional
tags: [jekyll, blog]          # Optional
excerpt: "Brief description"   # Optional
---

Your content starts here...
```

### 3. Writing Tips

#### Formatting
- **Headers**: Use `##` for main sections, `###` for subsections
- **Code blocks**: Use triple backticks with language specification
- **Images**: Store in `/assets/images/` and reference as `![alt text](/assets/images/filename.jpg)`
- **Links**: Use `[text](url)` for external links

#### Code Highlighting
```markdown
```python
def hello_world():
    print("Hello, World!")
```
```

#### Including Images
1. Add images to `/assets/images/`
2. Reference in posts:
```markdown
![Description](/assets/images/your-image.jpg)
```

## Local Development

### Initial Setup (One Time)
```bash
# Install Ruby (if not installed)
# macOS: brew install ruby
# Ubuntu: sudo apt-get install ruby-full

# Install bundler
gem install bundler

# Install dependencies
bundle install
```

### Running Locally
```bash
# Start local server
bundle exec jekyll serve

# With drafts
bundle exec jekyll serve --drafts

# Access at: http://localhost:4000
```

### Live Reload
The local server automatically rebuilds when you save changes. Just refresh your browser.

## Publishing

### Standard Publishing Flow
```bash
# 1. Check status
git status

# 2. Add your changes
git add .
# OR add specific files
git add _posts/2024-01-15-new-post.md

# 3. Commit with descriptive message
git commit -m "Add post: Understanding Jekyll basics"

# 4. Push to GitHub
git push origin main
```

### Best Practices
- **Always preview locally** before publishing
- **Use descriptive commit messages**
- **Check GitHub Actions** for build status after pushing

### Checking Build Status
1. Go to: https://github.com/forbidden-game/forbidden-game.github.io/actions
2. Look for green checkmark (success) or red X (failure)
3. Click on the workflow to see details if failed

## Customization

### 1. Site Configuration
Edit `_config.yml` for:
- Site title and description
- Author information
- Social media links
- URL settings

**Important**: After changing `_config.yml`, restart the local server.

### 2. Styling
Edit `/assets/css/style.css` for:
- Colors and fonts
- Layout adjustments
- Responsive design tweaks

### 3. Layouts
Modify files in `_layouts/`:
- `default.html` - Base template
- `post.html` - Post template
- `page.html` - Page template

### 4. Creating New Pages
1. Create a new `.md` file in the root directory
2. Add front matter:
```markdown
---
layout: page
title: "Page Title"
permalink: /custom-url/
---
```

### 5. Navigation
To add pages to navigation, create them in the root with proper front matter. Common pages:
- `about.md`
- `projects.md`
- `contact.md`

## Troubleshooting

### Site Not Updating
1. **Check GitHub Actions**: Ensure build succeeded
2. **Clear browser cache**: Hard refresh (Ctrl+Shift+R or Cmd+Shift+R)
3. **Wait 5-10 minutes**: GitHub Pages can have delays

### Build Failures
1. **Check GitHub Actions logs** for specific errors
2. **Common issues**:
   - Invalid YAML in front matter (check for tabs vs spaces)
   - Missing closing tags in HTML
   - Incorrect date format in filename

### Local Server Issues
```bash
# If bundle install fails
gem install bundler:2.3.26

# If server won't start
bundle update
bundle exec jekyll clean
bundle exec jekyll serve
```

### 404 Errors
- Ensure repository name matches username: `forbidden-game.github.io`
- Check `_config.yml` has correct URL
- Verify file is pushed to GitHub

## Advanced Tips

### Drafts
```bash
# Create draft in _drafts/ folder
_drafts/my-draft-post.md

# Preview drafts locally
bundle exec jekyll serve --drafts
```

### Scheduling Posts
Use future dates in front matter. Posts won't appear until that date:
```yaml
date: 2024-12-25 00:00:00 +0000
```

### SEO Optimization
1. Use descriptive titles
2. Add meta descriptions in front matter:
```yaml
excerpt: "This post explains..."
```
3. Use proper heading hierarchy
4. Add alt text to images

### Performance
1. Optimize images (use WebP or compressed JPEG)
2. Minimize custom CSS
3. Use Jekyll's built-in pagination for post lists

## Quick Reference

### Directory Structure
```
forbidden-game.github.io/
├── _config.yml          # Site configuration
├── _posts/              # Blog posts
├── _layouts/            # Page templates
├── _includes/           # Reusable components
├── _drafts/             # Unpublished posts
├── assets/              
│   ├── css/            # Stylesheets
│   └── images/         # Images
├── index.md            # Homepage
├── about.md            # About page
└── Gemfile             # Ruby dependencies
```

### Useful Resources
- [Jekyll Documentation](https://jekyllrb.com/docs/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Markdown Guide](https://www.markdownguide.org/)
- [Your Blog](https://forbidden-game.github.io)

## Emergency Contacts
- GitHub Pages Status: https://www.githubstatus.com/
- Jekyll Forums: https://talk.jekyllrb.com/
- Your Repository: https://github.com/forbidden-game/forbidden-game.github.io