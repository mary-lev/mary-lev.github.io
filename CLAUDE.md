# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Jekyll-based academic portfolio website built with the al-folio theme. It showcases NLP research, projects, publications, and blog posts for Maria Levchenko, an NLP Engineer/Python Developer. The site is hosted on GitHub Pages and includes features like academic CV, project galleries, blog posts, and bibliography management.

## Architecture

- **Jekyll Static Site Generator**: Uses Jekyll with al-folio theme for academic portfolios
- **Content Organization**: 
  - `_pages/`: Main site pages (about, CV, projects, publications, blog)
  - `_posts/`: Blog posts about NLP projects and research
  - `_projects/`: Individual project showcases
  - `_data/`: Structured data (CV info, repositories, venues)
  - `_bibliography/`: Academic papers and citations
- **Styling**: SCSS in `_sass/` with Bootstrap and custom academic theme
- **Assets**: Images, PDFs, Jupyter notebooks, and other media in `assets/`
- **Plugins**: Extensive Jekyll plugin ecosystem for academic features

## Development Commands

### Local Development
```bash
# Install dependencies
bundle install

# Serve locally (development)
bundle exec jekyll serve --watch --port=4000

# Build for production
bundle exec jekyll build
```

### Docker Development
```bash
# Run with Docker Compose
docker-compose up

# Access at http://localhost:8080
# Includes live reload and automatic config file watching
```

### Code Formatting
```bash
# Format Liquid templates and HTML
npx prettier --write "**/*.{html,liquid}" --plugin=@shopify/prettier-plugin-liquid
```

## Key Configuration

- **Main config**: `_config.yml` - Contains all site settings, theme options, plugin configuration
- **Content management**: Collections for news, projects, and posts
- **Academic features**: Jekyll Scholar for bibliography, imagemagick for responsive images
- **Social integration**: Links to GitHub, LinkedIn, Telegram, ORCID, Kaggle
- **Analytics**: Google Analytics enabled

## Content Types

- **Blog posts**: Markdown files in `_posts/` focusing on NLP projects, corpus linguistics, ML competitions
- **Projects**: Individual project pages with images and descriptions
- **Publications**: Managed via BibTeX files in `_bibliography/`
- **CV data**: YAML format in `_data/cv.yml`
- **Jupyter notebooks**: Integrated display of `.ipynb` files for data science projects

## Theme Customization

The site uses the al-folio academic theme with customizations:
- Custom SCSS variables and overrides in `_sass/`
- Academic-focused layouts in `_layouts/`
- Specialized includes for CV sections, publications, projects
- Dark/light theme support (currently disabled)
- Responsive image optimization with ImageMagick