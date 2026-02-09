# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a minimal Jekyll blog hosted on GitHub Pages at `BITliudong.github.io`. The site includes a blog, about page, and Atom feed. It uses basic Jekyll features without custom plugins or complex includes.

## Common Development Tasks

- **Local Development**: Run `jekyll serve` (or `bundle exec jekyll serve` if a Gemfile is present) to start a local server at `http://localhost:4000`. The `_site/` directory is ignored by git.
- **Building**: Run `jekyll build` to generate the static site in `_site/`.
- **Adding Blog Posts**: Create new Markdown files in `_posts/` with filename format `YYYY-MM-DD-title.md` and front matter including `layout: post`, `title`, and `date`.
- **Adding Pages**: Create HTML or Markdown files in appropriate directories (e.g., `about/index.html`) with front matter specifying `layout: default` and `title`.

## Architecture

- **Layouts**: Two layouts in `_layouts/`:
  - `default.html`: Provides navigation (Home, About, CV, Blog) and footer.
  - `post.html`: Extends `default` and displays post title, date, and content.
- **Pages**:
  - `index.html`: Homepage with a brief blurb.
  - `about/index.html`: About page with contact links.
  - `cv/index.html`: Academic-style curriculum vitae with research profile.
  - `blog/index.html`: Lists all posts using Liquid `{% for post in site.posts %}`.
  - `blog/atom.xml`: Atom feed for the blog.
- **Styling**: Single CSS file at `css/main.css` with basic typography and layout rules.
- **Configuration**: `_config.yml` sets site name, markdown processor, and permalink style.

## Deployment

GitHub Pages automatically builds and deploys the site when changes are pushed to the `main` branch. No manual build step is required for deployment.