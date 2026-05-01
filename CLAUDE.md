# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Local Development

```bash
bundle install              # install Ruby dependencies (delete Gemfile.lock first if errors occur)
bundle exec jekyll liveserve  # serve at localhost:4000 with live reload
bundle exec jekyll serve      # serve without live reload
```

The `_config.yml` is not reloaded automatically — restart the server after changing it. Use `_config.dev.yml` to override settings for local development.

## Architecture

This is a Jekyll academic website based on the [academicpages](https://github.com/academicpages/academicpages.github.io) template (forked from Minimal Mistakes). Content is organized as Jekyll collections:

- `_publications/` — individual paper pages (YAML frontmatter + markdown)
- `_talks/` — talk/presentation pages
- `_teaching/` — teaching pages
- `_portfolio/` — portfolio items
- `_posts/` — blog posts
- `_pages/` — standalone pages (about, cv, publications list, etc.)

**Content generation:** `markdown_generator/` contains Jupyter notebooks and Python scripts to batch-generate markdown files from TSV data. Run `publications.ipynb` (or `publications.py`) and `talks.ipynb` (or `talks.py`) from within that folder to regenerate `_publications/` and `_talks/` entries from their respective `.tsv` files.

**Site configuration:** `_config.yml` controls author profile, social links, analytics, collections, and permalink structure. Navigation menus are in `_data/navigation.yml`.

**Theming:** Layouts live in `_layouts/`, partials in `_includes/`, and SCSS in `_sass/`. The `assets/` folder holds compiled JS and CSS.

**Talk map:** `talkmap.ipynb` / `talkmap.py` generate a Leaflet.js map from talk locations; output goes in `talkmap/`.

## Adding Content

Each collection entry is a markdown file with YAML frontmatter. Required fields vary by collection — see existing entries for the expected schema. Publication files follow the naming convention `YYYY-MM-DD-url-slug.md`.
