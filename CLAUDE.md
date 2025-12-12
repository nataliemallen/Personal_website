# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static portfolio website for Natalie Allen, a PhD student in Conservation Genomics. The site is built with vanilla HTML, CSS, and JavaScript to be hosted on GitHub Pages for free. No build process or framework dependencies are required.

## Site Structure

The website consists of three main pages:

1. **index.html** - Home/About page with profile information, social/academic links (Google Scholar, LinkedIn, ORCID), CV download, and photo gallery
2. **publications.html** - Publications list formatted in AMA citation style
3. **research.html** - Research interests and areas of focus in conservation genomics

All pages share:
- A consistent navigation bar (sticky header)
- Unified styling via `styles.css`
- Responsive design that works on mobile, tablet, and desktop
- Professional green color scheme reflecting conservation/nature themes

## Key Design Decisions

- **No build process**: Pure HTML/CSS/JS means direct editing and immediate preview
- **GitHub Pages ready**: Files can be deployed as-is to GitHub Pages
- **Responsive-first**: Mobile-friendly grid and flexbox layouts with media queries
- **Accessible**: Semantic HTML, proper heading hierarchy, ARIA-friendly structure
- **Professional academic aesthetic**: Clean, minimal design appropriate for academic portfolios

## Content Customization

To update site content:

1. **Profile links**: Edit `href` attributes in `index.html` social links section
2. **Publications**: Add/edit publication entries in `publications.html` following AMA format
3. **Research areas**: Modify research cards in `research.html`
4. **Images**: Add images to `images/` directory:
   - `profile.jpg` - main profile photo
   - `field-[1-4].jpg` - gallery images
5. **CV**: Add PDF to root directory and update download link in `index.html`
6. **Colors**: Modify CSS custom properties in `:root` selector in `styles.css`

## Development Workflow

### Testing Locally

Open HTML files directly in a browser or use a local server:
```bash
python -m http.server 8000
# Visit http://localhost:8000
```

### Deploying to GitHub Pages

1. Push code to GitHub repository
2. Enable GitHub Pages in repository settings (Settings > Pages > Source: main branch)
3. Site will be live at `https://username.github.io/repo-name/`

## File Organization

```
/
├── index.html          # Home page (About)
├── research.html       # Research interests
├── publications.html   # Publications list
├── styles.css          # All styles (CSS variables, responsive design)
├── images/             # Image assets
├── CLAUDE.md          # This file
├── README.md          # User-facing documentation
└── .gitignore         # Git ignore rules
```

## Styling System

The site uses CSS custom properties (variables) for theming:
- `--primary-color`: Main green (#2c5f2d)
- `--secondary-color`: Light green accent (#97bc62)
- `--accent-color`: Mid-tone green (#4a7c59)

The CSS is organized by component:
1. Reset and base styles
2. Navigation
3. Hero section
4. Content sections
5. Responsive breakpoints (768px, 480px)

## Image Requirements

When adding images:
- Profile photo: 400x400px minimum, square or portrait
- Gallery images: 600x400px minimum, landscape orientation
- Formats: JPEG or PNG
- Optimize for web (compress to reduce file size)

## Browser Compatibility

The site uses modern CSS (Grid, Flexbox, Custom Properties) and works in:
- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

No polyfills or fallbacks needed for modern browsers.
