# NASA GeoAI Landing Page

A clean, minimal, academic-style landing page for the NASA GeoAI project, built with HTML and CSS for GitHub Pages.

## Quick Start

### 1. Setup Your GitHub Repository

Create a new repository named `geoai.github.io` under your GitHub organization:

```
https://github.com/YOUR-ORG/geoai.github.io
```

### 2. Add Files to Your Repository

Copy these files to your repository root:
- `index.html` - Main landing page
- `style.css` - Styling

### 3. Enable GitHub Pages

Your site will automatically be published at `https://geoai.github.io/` when you push to the `main` branch.

## Customization Guide

### Update Header Information

Edit the `<header>` section in `index.html`:

```html
<h1>NASA GeoAI</h1>
<p class="tagline">Geospatial Artificial Intelligence for Earth Observation</p>
```

### Add Your Projects

Each project is a `<article class="project-card">` block. Customize the template:

```html
<article class="project-card">
    <div class="project-image">
        <img src="YOUR_IMAGE_URL" alt="Project Name">
    </div>
    <div class="project-content">
        <h3>Your Project Title</h3>
        <p class="project-description">
            Your 2-3 sentence project description here.
        </p>
        <div class="project-tags">
            <span class="tag">Tag 1</span>
            <span class="tag">Tag 2</span>
            <span class="tag">Tag 3</span>
        </div>
        <div class="project-authors">
            <strong>Authors:</strong> Your Name, Co-Author Name
        </div>
        <div class="project-links">
            <a href="https://github.com/your-repo" class="btn btn-primary">View Code</a>
            <a href="https://arxiv.org/abs/XXXX.XXXXX" class="btn btn-secondary">Read Paper</a>
        </div>
    </div>
</article>
```

#### Image Options

**Option A: Use Placeholder (Quick Start)**
```html
<img src="https://via.placeholder.com/400x250?text=Project+Name" alt="Project">
```

**Option B: Host Images in Your Repository**
1. Create an `images/` folder in your repo
2. Add your project images (e.g., `images/project1.jpg`)
3. Link them in the HTML:
```html
<img src="images/project1.jpg" alt="Project 1">
```

**Option C: Link to External Image URL**
```html
<img src="https://example.com/your-image.jpg" alt="Project">
```

**Image Recommendations:**
- Dimensions: 400x250px (aspect ratio 16:10)
- Format: JPG or PNG
- Size: <200KB for fast loading
- Content: Project visualization, diagram, or research illustration

### Update Project Links

Replace placeholders with your actual links:

```html
<!-- GitHub Repository Link -->
<a href="https://github.com/your-org/your-repo" class="btn btn-primary">View Code</a>

<!-- Paper Link (arXiv, Journal, or PDF) -->
<a href="https://arxiv.org/abs/XXXX.XXXXX" class="btn btn-secondary">Read Paper</a>
```

### Update Resources Section

Customize the footer resources boxes:

```html
<div class="resource-box">
    <h3>Your Resource</h3>
    <p>Description of the resource.</p>
    <a href="https://example.com/" target="_blank">Visit Resource →</a>
</div>
```

### Change Colors

Edit the CSS variables at the top of `style.css`:

```css
:root {
    --primary-color: #0B4F8C;      /* Main blue */
    --secondary-color: #1a73e8;    /* Link blue */
    --accent-color: #f57c00;       /* Orange accents */
    --text-dark: #1a1a1a;
    --text-light: #666666;
    --background: #ffffff;
    --border-color: #e0e0e0;
    --light-bg: #f8f9fa;
}
```

### Adjust Grid Layout

The current layout shows 2 columns on desktop. To change the number of columns:

```css
.projects-grid {
    grid-template-columns: repeat(2, 1fr);  /* Change the number here */
    gap: 2rem;
}
```

### Add More Projects

Simply duplicate a `<article class="project-card">` block and update the content. The grid will automatically adjust.

## Deployment

### Push to GitHub

```bash
git add .
git commit -m "Initial commit: NASA GeoAI landing page"
git push origin main
```

Your site will be live at `https://geoai.github.io/` within seconds.

### Update Content

Simply edit the files and push to GitHub. Changes appear automatically.

## Optional Enhancements

### Add a Custom Domain

In repository settings, add your custom domain (e.g., `nasogeoai.org`) and update DNS records.

### Add a Favicon

Place a `favicon.ico` file in the repository root and add to `<head>`:

```html
<link rel="icon" href="favicon.ico">
```

### Add Google Analytics

Add this before `</head>` in `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=YOUR-GA-ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'YOUR-GA-ID');
</script>
```

### Add a Newsletter Signup

Add a form section before the footer to collect emails.

## File Structure

```
geoai.github.io/
├── index.html          # Main landing page
├── style.css           # Styling
├── README.md           # This file
├── images/             # (Optional) Project images
│   ├── project1.jpg
│   ├── project2.jpg
│   └── ...
└── .gitignore          # (Optional) Git ignore file
```

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance Tips

- Compress images to under 200KB
- Use modern formats (WebP with JPG fallback)
- Test on mobile devices
- Check load time at PageSpeed Insights

## License

This template is provided as-is. Feel free to customize for your project.

## Support

For questions about GitHub Pages, see the [official documentation](https://docs.github.com/en/pages).
