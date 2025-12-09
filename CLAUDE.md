# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo static site generator project with the following structure:
- **Hugo version**: 0.152.2 (extended)
- **Theme**: PaperMod (currently configured in hugo.yaml)
- **Alternative theme**: Ananke (available as git submodule)
- **Site title**: "XuanjingBlog"
- **Base URL**: https://xuanjingblog.netlify.app/

## Development Commands

### Building and Serving
- `hugo` - Build the site to `public/` directory
- `hugo server` - Start development server with live reload
- `hugo server -D` - Include draft content in development server

### Content Management
- `hugo new posts/my-post.md` - Create new blog post
- `hugo new page/about.md` - Create new page
- `hugo list all` - List all content

### Site Configuration
- `hugo config` - Display site configuration
- `hugo version` - Check Hugo version

## Architecture

### Theme System
- **Primary theme**: PaperMod (located in `themes/PaperMod/`)
- **Alternative theme**: Ananke (git submodule in `themes/ananke/`)
- Theme switching: Update `theme: "PaperMod"` in `hugo.yaml`

### Content Structure
- **Archetypes**: Default content templates in `archetypes/default.md`
- **Content**: Clean, minimal content focused on personal blogging
- **Static files**: Site assets and static content
- **Public output**: Generated site in `public/` directory

### Theme Features (PaperMod)
- Asset generation with pipelining, fingerprinting, bundling, and minification
- 3 display modes: Regular, Home-Info, Profile
- Table of Contents generation
- Light/Dark theme with automatic switching
- SEO optimization
- Search functionality with Fuse.js
- Multilingual support
- No webpack or Node.js dependencies required

## Git Submodules

- `themes/ananke` is managed as a git submodule
- Use `git submodule update --init` to initialize submodules

## Development Workflow

1. **Content creation**: Use `hugo new` commands to create posts/pages
2. **Local development**: Run `hugo server` for live preview
3. **Build**: Run `hugo` to generate static site in `public/`
4. **Deployment**: Deploy `public/` directory to hosting service

## Configuration

Main configuration file: `hugo.yaml`
- Site metadata (title, baseURL, language)
- Theme selection
- Build settings

## Git Commit Guidelines

- Keep commit messages concise and descriptive
- Avoid including AI tool references in commit messages
- Focus on what changed and why, not how it was implemented

## Deployment Workflow

### Netlify Deployment
- **No local build required**: Push changes directly to GitHub repository
- **Automatic deployment**: Netlify automatically builds and deploys on push
- **Preview URL**: https://xuanjingblog.netlify.app/
- **Preview changes**: View deployment results directly on Netlify

### Development Workflow
1. Create/edit content files in `content/` directory
2. Commit changes to Git
3. Push to GitHub repository
4. Netlify automatically builds and deploys
5. View results at https://xuanjingblog.netlify.app/

### Local Development (Optional)
- Use `hugo server` for local preview only
- Generated `public/` folder is ignored by Git (see .gitignore)
- No need to build locally for deployment

## Notes

- The site has clean, minimal content ready for personal blogging
- PaperMod theme documentation: https://github.com/adityatelange/hugo-PaperMod/wiki
- Hugo documentation: https://gohugo.io/