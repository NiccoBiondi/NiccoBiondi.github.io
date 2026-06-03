# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

A personal academic website built on the [al-folio](https://github.com/alshedivat/al-folio) Jekyll theme, deployed to GitHub Pages at `https://NiccoBiondi.github.io`.

## Local development

**Recommended (Docker):**
```sh
docker compose pull
docker compose up
# site available at http://localhost:8080
```

**Slim image (~100MB):**
```sh
docker compose -f docker-compose-slim.yml up
```

**Without Docker:**
```sh
bundle install
pip install jupyter
bundle exec jekyll serve
# site available at http://localhost:4000
```

**Build static site:**
```sh
bundle exec jekyll build
# output in _site/
```

**Format code (Prettier):**
```sh
npx prettier --write .
```

## Deployment

Pushing to `main` triggers the GitHub Actions deploy workflow, which builds and pushes to the `gh-pages` branch. Do not manually edit `gh-pages`. Changes to `_config.yml` require a full rebuild to take effect; all other content changes hot-reload locally.

## Key files to edit for personal customization

| What to change | Where |
|---|---|
| Name, bio, profile photo | `_pages/about.md` and `_config.yml` (top section) |
| CV | `assets/json/resume.json` (preferred) or `_data/cv.yml` (fallback) |
| Publications | `_bibliography/papers.bib` |
| Social links | `_data/socials.yml` |
| News items | `_news/` (one `.md` file per item) |
| Projects | `_projects/` (one `.md` file per project) |
| Blog posts | `_posts/YYYY-MM-DD-title.md` |
| GitHub repos/users shown | `_data/repositories.yml` |
| Co-author links | `_data/coauthors.yml` |
| Theme color | `_sass/_themes.scss` (`--global-theme-color`) |
| Site-wide settings | `_config.yml` |

## Architecture

The site uses Jekyll collections. Content flows like this:

- `_config.yml` — central config: site identity, navbar, scholar settings (author name matching for underline in publications), enabled plugins, collection definitions.
- `_pages/` — each `.md` file becomes a nav page. Front matter controls `nav`, `nav_order`, and `permalink`.
- `_layouts/` and `_includes/` — Liquid templates. `bib.liquid` controls publication card rendering; `_includes/` has reusable partials.
- `_sass/` — SCSS. `_themes.scss` for colors, `_variables.scss` for color palette options, `_base.scss` for typography/spacing.
- `_plugins/` — custom Ruby plugins: citation counts from Google Scholar/InspireHEP, cache busting, external post import.

Publications are rendered via `jekyll-scholar`. The author whose name matches `scholar: last_name`/`first_name` in `_config.yml` is underlined automatically. Extra BibTeX fields (`pdf`, `arxiv`, `code`, `poster`, `slides`, `website`, `bibtex_show`, etc.) generate buttons on publication cards.

## Code quality checks

Pre-commit hooks enforce trailing whitespace, EOF newlines, and YAML validity. CI also runs Prettier for formatting and lychee for broken links.
