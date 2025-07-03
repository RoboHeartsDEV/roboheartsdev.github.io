# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Jekyll-based static site generator project** that serves as the documentation and tutorial site for **RoboHearts DEV**. The site focuses on NAO robot programming education and uses a custom GitBook-style theme.

### Technology Stack
- **Jekyll** (Ruby-based static site generator)
- **Remote theme**: `RoboHeartsDEV/guide-to-nao` (custom GitBook-style theme)
- **Kramdown** markdown processor with Rouge syntax highlighting
- **FontAwesome** icons and custom fonts
- **Multiple search implementations** (search-pro, lunr, etc.)

### Key Features
- GitBook-style documentation layout
- Syntax highlighting with multiple themes
- Table of contents generation
- Email spam protection in configuration
- Responsive design with mobile support

## Development Commands

### Local Development
```bash
# Install dependencies
bundle install

# Start local development server
bundle exec jekyll serve

# Build site
bundle exec jekyll build

# Clean build files
bundle exec jekyll clean
```

### Development Notes
- **No npm/yarn scripts** - this is pure Jekyll/Ruby
- **No modern JavaScript build process** - uses traditional Jekyll asset pipeline
- **Ruby/Jekyll setup required** for local development
- Uses `Gemfile` for dependency management

## Site Architecture

### Content Structure
- **`_posts/`** - Dated tutorial articles about NAO programming (main content)
- **`_pages/`** - Static pages (about, contact, etc.)
- **`README.md`** - Actually serves as the homepage content
- **`_config.yml`** - Main site configuration
- **`assets/`** - CSS, JavaScript, images, and other static assets

### Layouts and Includes
- Uses standard Jekyll layouts and includes system
- Custom GitBook-style theme provides consistent styling
- Responsive design with mobile-first approach

### NAO Programming Content Focus
The site covers three main NAO programming approaches:
1. **Visual programming** with Choregraphe
2. **Python 2/3 programming** with SDKs  
3. **ROS integration** for advanced robotics

## Configuration Details

### Important Config Settings
- **Remote theme**: Uses `RoboHeartsDEV/guide-to-nao` for styling
- **Base URL**: `/landing` (GitHub Pages setup)
- **URL**: `https://roboheartsdev.github.io` (GitHub Pages hosting)
- **Markdown processor**: Kramdown with GFM input
- **Syntax highlighting**: Rouge with colorful theme
- **Search**: Multiple search implementations available

### Contact Information
- **Email**: contact@robohearts.eu
- **GitHub**: RoboHeartsDEV organization
- **Twitter**: @EmileAndHisBots (for development questions)

## Development Guidelines

### Content Guidelines
- **Educational focus**: All content should be instructional for NAO programming
- **Three programming tracks**: Visual (Choregraphe), Python, and ROS
- **Beginner-friendly**: Assume readers are new to robotics programming
- **RoboHearts DEV branding**: Maintain consistent branding throughout

### Technical Requirements
- **Ruby/Jekyll environment** required for local development
- **No CI/CD setup** - manual deployment process
- **GitHub Pages compatible** - follows Jekyll constraints

## Common Development Tasks

### Adding New Content
1. Create new post in `_posts/` with date prefix: `YYYY-MM-DD-title.md`
2. Use appropriate frontmatter with category, layout, etc.
3. Follow existing content structure and style

### Updating Theme
- Theme is remote - updates come from upstream repository
- Local customizations should be minimal to avoid conflicts

### Testing Changes
- Always test locally with `bundle exec jekyll serve`
- Check responsiveness and mobile compatibility
- Verify search functionality works with new content

## Front Matter Structure
```yaml
---
title: "Post Title"
author: "Emile Kroeger"
date: YYYY-MM-DD
category: NAO
layout: post
---
```

## Development Environment Setup
1. Ensure Ruby is installed
2. Run `bundle install` to install Jekyll and dependencies
3. Use `bundle exec jekyll serve` for local development
4. Site will be available at `http://localhost:4000/landing`

This site is specifically focused on NAO robot programming education under the RoboHearts DEV brand and follows Jekyll best practices with a custom GitBook-style theme for technical documentation.