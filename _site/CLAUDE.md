# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is an **al-folio** Jekyll academic website template designed for academics, researchers, and students. It's optimized for GitHub Pages deployment and provides comprehensive functionality for showcasing academic work, including publications, CV, projects, blog posts, and more.

## Development Commands

### Local Development Setup

**Docker (Recommended):**
```bash
# Start development server on http://localhost:8080
docker compose pull
docker compose up

# Slim version (faster, smaller image)
docker compose -f docker-compose-slim.yml up

# Build custom docker image
docker compose up --build

# Debug docker issues
docker compose up -d
docker compose logs
docker compose exec -it jekyll /bin/bash
```

**Native Ruby Setup:**
```bash
# Install dependencies
bundle install

# Local development server on http://localhost:4000
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

### Code Quality and Deployment

```bash
# Format code with Prettier
npx prettier --write .

# Manual deployment to GitHub Pages
# (Automatic deployment is configured via GitHub Actions)

# Clean CSS for production
purgecss -c purgecss.config.js

# Build to custom destination
bundle exec jekyll build --destination /path/to/destination
```

## Architecture Overview

### Core Jekyll Structure
- **`_config.yml`**: Main site configuration, theme settings, plugin configuration
- **`_layouts/`**: HTML templates (about, post, CV, publications, distill)
- **`_includes/`**: Reusable components (header, footer, CV sections, social links)
- **`_sass/`**: SCSS stylesheets with theme variables and responsive design
- **`_pages/`**: Static pages (about, CV, publications, projects, blog)
- **`_posts/`**: Blog posts following Jekyll naming convention (YYYY-MM-DD-title.md)

### Academic-Specific Features
- **`_bibliography/`**: BibTeX files for publications (managed by jekyll-scholar)
- **`_data/`**: YAML data files (CV, social links, repositories, coauthors)
- **`_projects/`**: Project showcase pages with metadata
- **`_news/`**: News/announcements displayed on homepage
- **`_books/`**: Book reviews and reading lists
- **`assets/`**: Static assets including JSON resume, PDFs, images

### Key Plugins and Dependencies
- **jekyll-scholar**: Bibliography management and citation formatting
- **jekyll-imagemagick**: Responsive image processing and WebP conversion
- **jekyll-jupyter-notebook**: Jupyter notebook support for blog posts
- **jekyll-minifier + jekyll-terser**: Asset optimization
- **jekyll-paginate-v2**: Advanced pagination for collections
- **jekyll-feed**: RSS/Atom feed generation

## Configuration and Customization

### Site Configuration (`_config.yml`)
- **Personal info**: Update title, name, contact details, social links
- **URL settings**: Set `url` and `baseurl` for deployment environment
- **Collections**: Enable/configure projects, news, books collections
- **Jekyll Scholar**: Bibliography style, source directory, filtering
- **Theme options**: Dark mode, navbar, footer, analytics integration
- **Third-party libraries**: CDN versions and integrity hashes

### Content Management
- **Publications**: Add BibTeX entries to `_bibliography/papers.bib`
- **CV**: Update `_data/cv.yml` or `assets/json/resume.json`
- **Projects**: Create markdown files in `_projects/` with front matter
- **Blog posts**: Follow Jekyll naming convention in `_posts/`
- **News**: Add announcements to `_news/` for homepage display

### Styling and Theming
- **Theme colors**: Modify `--global-theme-color` in `_sass/_themes.scss`
- **Custom styles**: Add to `_sass/_base.scss` or create new SCSS files
- **Responsive images**: Configure in `_config.yml` under `imagemagick`
- **Font integration**: Font Awesome, Academicons, and Tabler Icons included

## Deployment Workflow

### GitHub Pages (Automatic)
- **Trigger**: Push to `master` branch
- **Workflow**: `.github/workflows/jekyll-build-deploy.yml`
- **Process**: Ruby 3.2 → bundle install → jekyll build → deploy to gh-pages
- **URL**: `https://changhongyan123.github.io`

### Development Tips
- **Live reload**: Both Docker and native serve support auto-regeneration
- **Bibliography**: Changes to `.bib` files require server restart
- **Asset optimization**: Images automatically processed for responsive display
- **Search functionality**: Built-in search indexes posts, pages, and bibliography
- **Theme switching**: Automatic dark/light mode based on system preference

### Common File Patterns
- **Posts**: `_posts/YYYY-MM-DD-title.md`
- **Projects**: `_projects/project-name.md`
- **News**: `_news/announcement.md`
- **Pages**: `_pages/page-name.md`
- **Assets**: `assets/img/`, `assets/pdf/`, `assets/json/`

### Important Notes
- **Repository name**: Must be `changhongyan123.github.io` for user site
- **Branch**: Deployment from `master` branch to `gh-pages`
- **Dependencies**: ImageMagick required for responsive images
- **Ruby version**: 3.2 (specified in GitHub Actions workflow)
- **Node.js**: Only used for Prettier code formatting