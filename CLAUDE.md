# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static portfolio website for Natalie Allen, a PhD student in Conservation Genomics. The site is built with vanilla HTML, CSS, and JavaScript to be hosted on GitHub Pages for free. No build process or framework dependencies are required.

## Site Structure

The website consists of four main pages:

1. **index.html** - Home/About page with profile information, social/academic links (Google Scholar, LinkedIn, ORCID), CV download, and photo gallery
2. **research.html** - Research interests AND a Projects section with figure + blurb cards for highlighted work
3. **publications.html** - Publications list formatted in AMA citation style
4. **contact.html** - Contact page with email mailto link and social/academic links

All pages share:
- A consistent navigation bar (sticky header) with About, Research, Publications, Contact
- A `.page-banner` element directly under the nav for an optional wide hero image
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
2. **Publications**: Add/edit publication entries in `publications.html` following AMA format. Add a `<a class="publication-link" href="DOI URL">doi:...</a>` inside the `.publication-text` paragraph for published work.
3. **Research areas**: Modify research cards in the "Research Interests" section of `research.html`
4. **Projects**: Edit the `.project-card` blocks in `research.html`. Each card has a `.project-figure` (background image) and a `.project-body` with title, blurb, and meta line. Replace the figure placeholder by uncommenting the `background-image` in the inline style and pointing it at your image (e.g. `images/project-1.jpg`).
5. **Banner images**: Each page has an empty `<div class="page-banner"></div>` directly under the nav. Add an inline `style="background-image: url('images/banner-research.jpg');"` to set a banner. Recommended size: ~2000x500px landscape.
6. **Contact email**: Update the `mailto:` link and visible address in `contact.html`.
7. **Images**: Add images to `images/` directory:
   - `profile.jpg` - main profile photo
   - `field-[1-4].jpg` - gallery images
   - `banner-{home,research,publications,contact}.jpg` - per-page banners (optional)
   - `project-[1-3].jpg` - project card figures
8. **CV**: Add PDF to root directory and update download link in `index.html`
9. **Colors**: Modify CSS custom properties in `:root` selector in `styles.css`

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
├── research.html       # Research interests + Projects section
├── publications.html   # Publications list
├── contact.html        # Contact page (email, links)
├── styles.css          # All styles (CSS variables, responsive design)
├── images/             # Image assets
├── CLAUDE.md          # This file
├── README.md          # User-facing documentation
└── .gitignore         # Git ignore rules
```

## Spacing Conventions

The site uses tight vertical spacing for a denser, less white-space-heavy feel.
If you adjust padding, keep it consistent across components:
- Section padding: ~1.25–1.75rem (not 3rem)
- Hero padding: ~1.75rem 0
- Card padding: ~1.25rem 1.5rem
- Footer padding: ~1.25rem with 2.5rem top margin

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
