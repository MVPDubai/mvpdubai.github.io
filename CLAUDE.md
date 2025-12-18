# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based GitHub Pages site for MVP Software Solutions, a Dubai-based software consultancy. The site uses the Minimal Mistakes theme (v4.24.0) via remote theme loading.

- **Custom domain**: mvpss.dev
- **Theme**: Minimal Mistakes with "dark" skin
- **Hosting**: GitHub Pages (auto-builds on push to main)

## Local Development

```bash
# Install dependencies
bundle install

# Run local server with live reload
bundle exec jekyll serve --livereload

# Build static site (outputs to _site/)
bundle exec jekyll build
```

Note: You'll need a `Gemfile` with `gem "github-pages"` to run locally. The site currently relies on GitHub Pages' automatic Jekyll building.

## Architecture

- **_config.yml**: Site configuration (theme, metadata, defaults)
- **index.md**: Homepage content using splash layout
- **CNAME**: Custom domain configuration

The site uses remote theme loading (`remote_theme: "mmistakes/minimal-mistakes@4.24.0"`), so theme files are not stored locally. The `jekyll-include-cache` plugin is required for the theme to work with GitHub Pages. Refer to [Minimal Mistakes documentation](https://mmistakes.github.io/minimal-mistakes/) for customization options.

## Adding Content

- Pages use front matter to specify layout and metadata
- Available layouts from Minimal Mistakes: `single`, `splash`, `home`, `posts`, `categories`, `tags`, `collection`, `archive`
- Assets go in `/assets/` directory (e.g., `/assets/images/`)
