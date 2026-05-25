# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**my-profile-site** is a personal portfolio and todo application built with vanilla HTML, CSS, and JavaScript. It's a static site with no build process or dependencies.

## Project Structure

```
my-profile-site/
├── index.html       # Portfolio website (main page)
├── todo.html        # Simple todo list application
└── CLAUDE.md        # This file
```

## Key Technologies

- **HTML5** - Semantic markup
- **CSS3** - Custom styles + Tailwind CSS (via CDN)
- **JavaScript (Vanilla)** - No frameworks
- **Tailwind CSS** - Utility-first CSS framework loaded from CDN

## Development

### Running Locally

Since this is a static site, you can serve it locally using:

```powershell
# Using Python (Python 3)
python -m http.server 8000

# Using Node.js (if available)
npx http-server

# Using Python (Python 2)
python -m SimpleHTTPServer 8000
```

Then open `http://localhost:8000` in your browser.

### File Descriptions

**index.html** - Portfolio website with:
- Navigation header (responsive)
- Hero section with animated background (gradient animations, floating bubbles)
- About section
- Skills/Tech Stack section (HTML, CSS, JavaScript, React, Node.js, Python)
- Projects showcase (3 project cards)
- Contact section
- Footer with links
- Smooth scroll behavior and fade-in animations on scroll

**todo.html** - Todo list application with:
- Input field for adding todos
- Checkbox to mark todos as complete
- Delete button for each todo
- Statistics (total, completed, remaining)
- LocalStorage persistence (todos saved in browser)
- Dark theme matching portfolio design

## Design System

### Color Palette

- **Background**: `#000000` (pure black)
- **Primary Accent**: `#6495FF` (cornflower blue) - used for buttons, icons, stats
- **Text**: `#FFFFFF` (white), `#d4d4d8` (light gray)
- **Secondary**: `#666666`, `#999999` (various gray shades)
- **Borders**: `#333333`, `#222222` (subtle grays)

### Animation Details

- **Fade-in**: Elements fade in when scrolling into view (0.8s duration)
- **Background Gradient**: Animated gradient shift (15s infinite loop)
- **Floating Bubbles**: Layered radial gradients with floating animation (20-30s duration)
- **Project Cards**: Scale on hover (1.02)
- **Button Hover**: Color change + slight translateY effect

## Important Notes

- Tailwind CSS is loaded from CDN, so no npm install needed
- LocalStorage is used for todo persistence (localStorage.getItem/setItem)
- All animations use CSS transitions and keyframes (no JS animation library)
- Responsive design uses Tailwind's `md:` breakpoint for tablet+ screens
- Smooth scrolling and intersection observer for fade-in animations

## Deployment

For deployment, simply upload all HTML files to a static hosting service:
- GitHub Pages
- Netlify
- Vercel
- AWS S3 + CloudFront

No build process required - serve the HTML files directly.

## User Information

- Name: 이재영 (Lee Jaeyoung)
- Email: leejy01022870502@gmail.com
- GitHub: https://github.com/leejy0222/my-profile-site
