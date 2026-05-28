# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## remember

Read existing files before writing. Don't re-read unless changed.

Thorough in reasoning, concise in output.

Skip files over 100KB unless required.

No sycophantic openers or closing fluff.

No emojis or em-dashes.

Do not guess APIs, versions, flags, commit SHAs, or package names. Verify by reading code or docs before asserting.

## Project Overview

This is an MkDocs Material site for an AI & CS learning guide, hosted on GitHub Pages. The content is written in Chinese (zh) with English (en) translations available. The site covers AI fundamentals, prompt engineering, AI-assisted programming, and CS learning resources.

## Development Commands

```bash
# Install dependencies
pip install -r requirements.txt

# Local development server
mkdocs serve

# Build the site
mkdocs build --clean

# Build with specific locale (if needed)
mkdocs build --clean -f mkdocs.yml
```

## Architecture

- **docs/**: Markdown content organized by topic (AI基础与大模型, 提示工程, 工具和方法, Python)
  - Each topic has `.md` (Chinese) and `.en.md` (English) versions
  - `template.en.md` provides the course template structure
- **site/**: Generated output (committed to gh-pages branch)
- **overrides/**: Custom MkDocs Material theme overrides (Giscus comments integration)
- **mkdocs.yml**: Main configuration with i18n plugin, search, git-revision-date, minify, and open-in-new-tab plugins

## Key Configuration

- **i18n**: Dual-language support (zh default, en) configured in `mkdocs.yml` under `plugins.i18n`
- **Comments**: Giscus integration via `overrides/partials/comments.html`
- **Deployment**: GitHub Actions workflow in `.github/workflows/deploy.yml` builds and deploys to gh-pages on push to main
- **Custom JS**: `site/js/open_in_new_tab.js` handles external links and document links opening in new tabs

## Content Structure

When adding new course content:
1. Create `.md` file in the appropriate `docs/` subdirectory
2. Create corresponding `.en.md` for English translation
3. Follow the template structure from `template.en.md` (Descriptions, Course Resources, Personal Resources)
4. Add navigation entry in `mkdocs.yml` under `nav`
5. If adding a new section, add translation mapping in `mkdocs.yml` under `plugins.i18n.languages[1].nav_translations`
