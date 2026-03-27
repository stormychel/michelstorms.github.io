# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal portfolio and app showcase site for Michel Storms (michelstorms.com). This is a **project site** hosted via GitHub Pages — it is NOT the main site at stormychel.github.io.

## Tech Stack

- **Jekyll** static site generator via the `github-pages` gem
- **No JavaScript** — pure HTML + inline CSS
- **No build tools** beyond Jekyll (no bundlers, task runners, etc.)
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

**All pages are standalone HTML files with inline `<style>` blocks** — there are no shared CSS files or external stylesheets (beyond Google Fonts). Each page is self-contained.

### Design System (CSS Variables)

Pages share a consistent set of CSS custom properties defined in each file's `:root`:
- Colors: `--navy`, `--navy-light`, `--navy-dark`, `--white`, `--off-white`, `--gray-100` through `--gray-500`, `--accent`
- App landing pages override `--accent` with their brand color (e.g., HoverCalc uses orange `#e07830`)
- Fonts: `Cormorant Garamond` (headings), `Inter` (body)

### Page Types

- **Top-level pages**: `index.html`, `apps.html`, `blog.html`, `accessibility-statement.html`
- **App landing pages**: `{app}/index.html` — each app directory also contains `privacy/`, `terms/`, and optionally `license/` subdirectories
- **Blog**: Posts in `_posts/` using `_layouts/post.html`

### SEO Pattern

Every page includes: meta tags, Open Graph, Twitter Card, Schema.org JSON-LD, canonical URL, and favicon references. Follow this pattern when adding new pages.

### Apps Currently Listed

HoverCalc, Unfold, PawMode, PickDatePlace — each with its own landing page directory under root.

## Assets

App screenshots and logos live in `assets/apps/{app-name}/`. Brand assets (logo variants) are in `assets/`.
