# Personal Website

Built with Hugo. Content in markdown, hosted on GitHub Pages.

## Local Development

```bash
hugo server --buildDrafts
```

Visit http://localhost:1313

## Content Structure

- `content/_index.md` - Home page
- `content/about/_index.md` - About / CV
- `content/portfolio/_index.md` - Portfolio
- `content/recipes/` - Recipe collection
- `content/blog/` - Blog posts

## Adding Content

### Recipe with Scaling

```markdown
---
title: "Recipe Name"
servings: 4
source: "https://example.com"
source_name: "Recipe Source"
---

## Ingredients

- <span class="ingredient-amount">2 cups</span> flour
```

The recipe template includes buttons to scale ingredients and toggle amounts on/off.

### Blog Post

```markdown
---
title: "Post Title"
date: 2025-05-22
draft: false
---

Your content here...
```

## Deployment

Automatically deploys to GitHub Pages on push to `claude/personal-website-markdown-PGAC1`.
