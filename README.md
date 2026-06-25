# Personal Website

**Live site:** https://sw1jari.github.io/Personal-Website/

Built with Hugo. Content in markdown, hosted on GitHub Pages. Edit the `.md`
files (e.g. in Obsidian), push to git, and the site rebuilds automatically.

## Local Development

```bash
hugo server --buildDrafts
```

Visit http://localhost:1313

## Content Structure

- `content/_index.md` - Home page (bio + experience + education)
- `content/photos/_index.md` - Photos
- `content/recipes/` - Recipe collection

## Adding a Recipe

Copy this template into a new file like `content/recipes/my-dish.md`. The format
is the same for every recipe so they all look and behave identically.

```markdown
---
title: "My Dish"
servings: 4                       # the number this recipe is written for
credit: "Original Author"         # optional
credit_url: "https://..."         # optional, links the credit
video_url: "https://..."          # optional, adds a "video" link
---

## Ingredients

- [2 cups (250 g)] flour
- [1] onion, diced
- A pinch of salt

## Instructions

1. Mix the [2 cups (250 g)] flour with the [1] diced onion.
2. Bake for 20 minutes.
```

**The one rule:** wrap any amount you want to scale in `[square brackets]`. Everything else is normal markdown.

- **Servings box**: visitors type any number (1 and up) and every bracketed
  amount rescales. Numbers, fractions (`1 1/2`, `2/3`) and metric in parentheses
  all scale together.
- **Hide amounts in steps**: a button hides the bracketed amounts inside the
  Instructions section so you can cook from clean steps. Ingredient amounts stay.

## Deployment

Pushing to `claude/personal-website-markdown-PGAC1` triggers the GitHub Actions
workflow, which builds the site and deploys it to GitHub Pages.

> **One-time setup:** in the repo, go to Settings > Pages > Source and select
> GitHub Actions (not "Deploy from a branch").
