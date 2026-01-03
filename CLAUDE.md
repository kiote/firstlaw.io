# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo static site generator project - a personal blog/portfolio website hosted at https://firstlaw.io/. The site covers technology, software development, and research topics.

## Development Commands

```bash
# Start local development server (with live reload)
hugo server

# Build static site (outputs to /public)
hugo

# Create new blog post
hugo new posts/my-new-post.md
```

## Architecture

- **Static site generator:** Hugo
- **Theme:** Binario (configured in hugo.toml)
- **Content format:** Markdown with YAML frontmatter

### Directory Structure

- `content/` - Markdown content (pages and posts)
  - `about.md` - About page
  - `posts/` - Blog post collection
- `themes/` - Hugo themes (git submodules, only binario is active)
- `archetypes/` - Templates for new content
- `public/` - Generated static site output
- `hugo.toml` - Hugo configuration

## Content Creation

Blog posts use standard Hugo frontmatter:

```yaml
---
title: "Post Title"
date: 2024-01-01
draft: false
tags: ["tag1", "tag2"]
---
```

## Configuration

Main configuration is in `hugo.toml`:
- Base URL: https://firstlaw.io/
- Language: English
- Theme color: orange
- Menu items: About, Showcase
