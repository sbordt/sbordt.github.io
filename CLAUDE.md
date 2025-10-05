# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a static personal academic website (GitHub Pages) for Sebastian Bordt, hosted at sbordt.github.io. The site is a single-page application built with vanilla HTML, CSS, and JavaScript.

## Architecture

**Single-Page Design**: The entire website is contained in `index.html` (760 lines), with all styling embedded via `<style>` tags and all interactivity in inline `<script>` tags.

**Core Sections**:
- Hero section with profile image and bio
- News section (reverse chronological)
- Publications section (selected works)
- Fixed navigation header with smooth scrolling

**Responsive Design**: Uses CSS Grid and media queries with breakpoints at 1024px, 768px, and 480px. Mobile navigation uses a hamburger menu.

**Assets**:
- `images/`: Profile photo and social media icons
- `files/`: PDFs (CV, papers, presentations)
- `old_website/`: Legacy content (not actively used)

## Development

This is a static site with no build process. Changes to `index.html` are immediately reflected when committed and pushed to GitHub Pages.

**To view locally**: Open `index.html` directly in a browser, or use a simple HTTP server:
```bash
python3 -m http.server 8000
```

**Deployment**: Automatic via GitHub Pages when changes are pushed to the `master` branch.

## Content Updates

**Adding News Items**: Insert new `<div class="news-item">` at the top of the news grid (around line 594).

**Adding Publications**: Insert new `<div class="publication-item">` at the top of the publications grid (around line 642). Use `<div class="publication-spotlight">Spotlight</div>` for highlighted papers.

**Updating Bio**: Modify the hero description paragraph text (around line 557).

## Styling

All CSS uses CSS custom properties (CSS variables) defined in `:root` (lines 14-31) for consistent theming. The color scheme is slate-based with `--primary-color: #475569`.

## JavaScript

Minimal vanilla JavaScript for:
- Mobile menu toggle
- Smooth scroll behavior
- Header shadow on scroll
- Auto-close menu on navigation or outside click
