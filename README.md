# Natalie Allen - Portfolio Website

A professional portfolio website for Natalie Allen, PhD student in Conservation Genomics.

## Features

- **About Page**: Home page with profile information, links to academic profiles (Google Scholar, LinkedIn, ORCID), and CV download
- **Research Page**: Overview of research interests in conservation genomics
- **Publications Page**: List of publications in AMA format
- **Responsive Design**: Mobile-friendly layout that works on all devices

## Setup Instructions

### Adding Content

1. **Profile Image**: Add your profile photo as `images/profile.jpg`
2. **Gallery Images**: Add field/research photos as `images/field-1.jpg`, `images/field-2.jpg`, etc.
3. **CV**: Add your CV file (e.g., `cv.pdf`) and update the download link in `index.html`
4. **Links**: Update the `href` attributes in `index.html` with your actual profile URLs:
   - LinkedIn profile URL
   - Google Scholar profile URL
   - ORCID iD URL
5. **Publications**: Edit `publications.html` to add your actual publications in AMA format
6. **Research Content**: Customize the research areas in `research.html` to match your specific interests

### Deploying to GitHub Pages

1. Create a new repository on GitHub (e.g., `natalie-allen.github.io` or `portfolio`)

2. Initialize git and push your code:
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Portfolio website"
   git branch -M main
   git remote add origin https://github.com/YOUR-USERNAME/REPO-NAME.git
   git push -u origin main
   ```

3. Enable GitHub Pages:
   - Go to your repository settings
   - Navigate to "Pages" section
   - Under "Source", select "main" branch
   - Click "Save"

4. Your site will be available at:
   - If repository is named `YOUR-USERNAME.github.io`: `https://YOUR-USERNAME.github.io`
   - Otherwise: `https://YOUR-USERNAME.github.io/REPO-NAME`

## File Structure

```
natalie-website/
├── index.html          # Home/About page
├── research.html       # Research interests page
├── publications.html   # Publications page
├── styles.css          # All styling
├── images/             # Image assets
│   ├── profile.jpg
│   ├── field-1.jpg
│   └── ...
├── cv.pdf              # Your CV file
└── README.md
```

## Customization

- **Colors**: Edit CSS variables in `styles.css` under `:root` to change the color scheme
- **Content**: All text content is in the HTML files and can be edited directly
- **Layout**: Modify the HTML structure and CSS grid/flexbox properties to adjust layouts

## Browser Support

This website works on all modern browsers including Chrome, Firefox, Safari, and Edge.
