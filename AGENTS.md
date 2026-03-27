# AGENTS.md

This file provides guidance to coding agents when working with code in this repository.

## Project Overview

Personal portfolio and app showcase site for Michel Storms (michelstorms.com). This is a **project site** hosted via GitHub Pages.

## Tech Stack

- **Jekyll** static site generator via the `github-pages` gem
- **No JavaScript build tooling** beyond Jekyll
- **Standalone pages** built mostly from HTML files with inline `<style>` blocks
- Deployed automatically by GitHub Pages on push to `main`

## Local Development

```bash
bundle install              # Install dependencies (first time)
bundle exec jekyll serve    # Serve locally at http://localhost:4000
```

## Workflow Expectations

- For visual or content changes, make the change locally first and preview it before considering the task done.
- After editing, open the changed page from a local server in the browser so the result can be reviewed locally before deployment.
- Prefer using the local preview URL in the handoff when the task affects page layout, styling, or copy.

## Architecture

**Top-level pages and app landing pages are self-contained**. They generally keep their own inline styles instead of relying on a shared stylesheet.

### Page Types

- **Top-level pages**: `index.html`, `apps.html`, `blog.html`, `accessibility-statement.html`
- **App landing pages**: `{app}/index.html` with supporting `privacy/`, `terms/`, and optional `license/` subdirectories
- **Blog**: Posts in `_posts/` using `_layouts/post.html`

### SEO Pattern

Pages include meta tags, Open Graph, Twitter card metadata, Schema.org JSON-LD, canonical URLs, and favicon references. Follow that pattern when adding or changing public pages.

## Assets

App screenshots and logos live in `assets/apps/{app-name}/`. Shared brand assets live in `assets/`.
