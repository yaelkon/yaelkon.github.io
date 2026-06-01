# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A personal academic website for Yael Konforti (PhD candidate, Computer Science, University of Cambridge) built with Jekyll using the [Chirpy theme](https://github.com/cotes2020/jekyll-theme-chirpy). Deployed automatically to GitHub Pages via the `pages-deploy.yml` workflow on every push to `main`.

## Commands

**Serve locally with live reload:**
```bash
bash tools/run.sh
# or with production mode:
bash tools/run.sh --production
```

**Build and test (HTML proofer):**
```bash
bash tools/test.sh
```

**Direct Jekyll commands:**
```bash
bundle exec jekyll s -l          # serve with livereload
bundle exec jekyll b             # build only
bundle exec htmlproofer _site --disable-external  # link check
```

## Architecture

The site is a thin configuration layer on top of the Chirpy gem (`jekyll-theme-chirpy ~> 7.2`). Most layouts, includes, Sass, and JS live inside the gem — not in this repo. To inspect theme internals: `bundle info --path jekyll-theme-chirpy`.

**What lives in this repo (customizable surface):**

| Path | Purpose |
|------|---------|
| `_config.yml` | All site-level settings: title, URL, social links, theme mode, comments, analytics, PWA |
| `_posts/` | Blog posts (Markdown). Currently empty (`.placeholder` only). |
| `_tabs/` | Top-level nav pages: about, archives, categories, tags |
| `_data/contact.yml` | Sidebar contact icons and links |
| `_data/share.yml` | Post share button configuration |
| `_plugins/posts-lastmod-hook.rb` | Sets post last-modified date from git history at build time |
| `assets/lib` | Git submodule pointing to `cotes2020/chirpy-static-assets` (optional CDN alternative) |

**Post format:** Files in `_posts/` must be named `YYYY-MM-DD-title.md` with Jekyll front matter. All posts default to `layout: post`, comments enabled, TOC enabled, and permalink `/posts/:title/` (set in `_config.yml` defaults).

**Deployment:** GitHub Actions (`.github/workflows/pages-deploy.yml`) builds with `JEKYLL_ENV=production`, runs htmlproofer, then deploys to GitHub Pages. Triggers on push to `main`/`master`.
