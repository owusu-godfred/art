# Artist Portfolio Website

A clean, modern, and vibrant single-page portfolio website designed for visual artists to showcase their work across multiple mediums including paintings, sculptures, digital art, mixed media, photography, and video installations.

## 🎨 Features

- **Single-Page Design** - Smooth scrolling navigation between sections
- **Interactive Gallery** - Filterable artwork collection by series/category
- **Lightbox Viewer** - Click images to view in full-screen mode
- **Video Support** - Autoplay videos with intelligent viewport detection
- **Responsive Design** - Looks great on desktop, tablet, and mobile devices
- **Contact Form** - Built-in form with validation for inquiries
- **Social Media Integration** - Links to Instagram, Facebook, Twitter, and Pinterest
- **Artistic Patterns** - Thematic background patterns throughout the site
- **Vibrant Colors** - Multi-color artistic palette with smooth gradients

## 📁 File Structure

```
artist-portfolio/
│
├── index.html          # Main HTML structure
├── styles.css          # All styling and design
├── script.js           # Interactive functionality
├── README.md           # Documentation (this file)
│
└── assets/             # (Create these folders as needed)
    ├── images/         # Your artwork images
    │   ├── artwork1.jpg
    │   ├── artwork2.jpg
    │   └── ...
    │
    ├── videos/         # Your artwork videos
    │   ├── video1.mp4
    │   └── ...
    │
    └── icons/          # (Optional) Custom icons
```

## 🚀 Getting Started

### Quick Setup

1. **Download or Clone** this repository
2. **Open** `index.html` in a web browser to preview
3. **Customize** the content (see Customization Guide below)
4. **Deploy** to GitHub Pages or any web hosting service

### Deploying to GitHub Pages

1. Create a new repository on GitHub
2. Upload all files (`index.html`, `styles.css`, `script.js`)
3. Go to **Settings** → **Pages**
4. Under "Source", select **main branch** and **root folder**
5. Click **Save**
6. Your site will be live at `https://yourusername.github.io/repository-name`

## ✏️ Customization Guide

### 1. Updating Your Personal Information

#### Artist Name/Logo
**File:** `index.html` (Line ~15)
```html
<div class="logo">ARTIST</div>
```
Replace `ARTIST` with your name or brand.

#### Hero Section
**File:** `index.html` (Lines ~31-36)
```html
<h1 class="hero-title">Visual Artist</h1>
<p class="hero-subtitle">Exploring the boundaries of creativity through diverse mediums</p>
```
Update the title and subtitle with your own tagline.

#### About Section Bio
**File:** `index.html` (Lines ~198-202)
```html
<p class="about-text">Lorem ipsum dolor sit amet...</p>
```
Replace all Lorem ipsum text with your actual biography.

#### Artist Statement
**File:** `index.html` (Lines ~204-205)
```html
<h3 class="statement-title">Artist Statement</h3>
<p class="statement-text">Lorem ipsum dolor sit amet...</p>
```
Add your personal artist statement here.

### 2. Adding Your Artwork

Each artwork is contained in a `gallery-item` div. Here's the structure:

**For Images:**
```html
<div class="gallery-item" data-category="abstract">
    <div class="artwork-card">
        <img src="assets/images/your-image.jpg" alt="Description" class="artwork-image">
        <div class="artwork-overlay">
            <h3 class="artwork-title">Artwork Title</h3>
            <p class="artwork-medium">Medium (e.g., Acrylic on Canvas)</p>
            <p class="artwork-price">$1,200</p>
            <span class="artwork-status available">Available</span>
        </div>
    </div>
</div>
```

**For Videos:**
```html
<div class="gallery-item" data-category="urban">
    <div class="artwork-card">
        <video class="artwork-video" autoplay muted loop playsinline>
            <source src="assets/videos/your-video.mp4" type="video/mp4">
        </video>
        <div class="artwork-overlay">
            <h3 class="artwork-title">Video Title</h3>
            <p class="artwork-medium">Video Installation</p>
            <p class="artwork-price">$3,500</p>
            <span class="artwork-status sold">Sold</span>
        </div>
    </div>
</div>
```

#### Important Attributes:
- `data-category` - Must match filter button values (abstract, nature, urban, or create your own)
- `artwork-status` - Use either `available` or `sold`

### 3. Customizing Categories/Filters

**File:** `index.html` (Lines ~42-47)
```html
<button class="filter-btn active" data-filter="all">All Works</button>
<button class="filter-btn" data-filter="abstract">Abstract Series</button>
<button class="filter-btn" data-filter="nature">Nature Studies</button>
<button class="filter-btn" data-filter="urban">Urban Landscapes</button>
```

To add/change categories:
1. Update the button text and `data-filter` value
2. Ensure your artwork items have matching `data-category` attributes
3. The `data-filter="all"` button should always remain

### 4. Changing Colors

**File:** `styles.css` (Lines ~2-15)
```css
:root {
    --primary-color: #FF6B6B;      /* Main red/pink */
    --secondary-color: #4ECDC4;    /* Teal */
    --accent-color: #95E1D3;       /* Mint green */
    --purple: #AA96DA;             /* Purple */
    --pink: #FCBAD3;               /* Light pink */
    --yellow: #FFFFD2;             /* Cream yellow */
    --coral: #F38181;              /* Coral */
    --mint: #A8E6CF;               /* Mint */
    --dark: #2C3E50;               /* Dark text */
    --light: #ECF0F1;              /* Light background */
    --white: #FFFFFF;              /* White */
}
```

Simply change the hex color codes to your preferred colors. These variables are used throughout the site for consistency.

### 5. Updating Social Media Links

**File:** `index.html` (Lines ~207-222)
```html
<div class="social-links">
    <a href="#" class="social-link" aria-label="Instagram">
        <i class="fab fa-instagram"></i>
    </a>
    <a href="#" class="social-link" aria-label="Facebook">
        <i class="fab fa-facebook"></i>
    </a>
    <!-- ... more links -->
</div>
```

Replace `#` with your actual social media URLs:
- Instagram: `https://instagram.com/yourusername`
- Facebook: `https://facebook.com/yourpage`
- Twitter: `https://twitter.com/yourusername`
- Pinterest: `https://pinterest.com/yourusername`

To add more social icons, visit [Font Awesome Icons](https://fontawesome.com/icons) and use the format:
```html
<a href="YOUR_URL" class="social-link" aria-label="Platform Name">
    <i class="fab fa-icon-name"></i>
</a>
```

### 6. Contact Form Setup

The current contact form displays a success message but doesn't actually send emails. To make it functional:

#### Option A: Use a Form Service (Recommended for Beginners)
Services like [Formspree](https://formspree.io/), [Netlify Forms](https://www.netlify.com/products/forms/), or [EmailJS](https://www.emailjs.com/) can handle form submissions.

**Example with Formspree:**
```html
<form class="contact-form" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

#### Option B: Custom Backend
If you have server-side capabilities, update the form submission logic in `script.js` (Lines ~152-177) to send data to your backend API.

### 7. Replacing Placeholder Images

The site currently uses placeholder images from `via.placeholder.com`. Replace these with your actual artwork:

1. Create an `assets/images/` folder in your project
2. Add your artwork images to this folder
3. In `index.html`, replace placeholder URLs:

**Before:**
```html
<img src="https://via.placeholder.com/600x800/FF6B6B/FFFFFF?text=Abstract+1" alt="Abstract Artwork 1" class="artwork-image">
```

**After:**
```html
<img src="assets/images/my-artwork-1.jpg" alt="Crimson Dreams" class="artwork-image">
```

#### Image Guidelines:
- **Format:** JPG or PNG
- **Recommended Size:** 600-1200px width, maintain portrait orientation
- **File Size:** Keep under 1MB for faster loading
- **Naming:** Use descriptive names (e.g., `abstract-crimson-dreams.jpg`)

### 8. Replacing Placeholder Videos

1. Create an `assets/videos/` folder
2. Add your video files (MP4 format recommended)
3. Replace placeholder video URLs:

**Before:**
```html
<source src="https://commondatastorage.googleapis.com/gtv-videos-bucket/sample/ForBiggerBlazes.mp4" type="video/mp4">
```

**After:**
```html
<source src="assets/videos/my-video-installation.mp4" type="video/mp4">
```

#### Video Guidelines:
- **Format:** MP4 (H.264 codec)
- **Duration:** 10-60 seconds for best performance
- **Resolution:** 1080p or 720p
- **File Size:** Keep under 10MB if possible
- **Note:** Videos autoplay muted and loop automatically

### 9. Changing Section Content

#### Gallery Section Description
**File:** `index.html` (Line ~40)
```html
<p class="section-description">Lorem ipsum dolor sit amet...</p>
```

#### Contact Section Description
**File:** `index.html` (Line ~230)
```html
<p class="section-description">Interested in purchasing artwork...</p>
```

### 10. Modifying Navigation

To add or remove sections from the navigation:

**File:** `index.html` (Lines ~16-21)
```html
<ul class="nav-links">
    <li><a href="#home" class="nav-link active">Home</a></li>
    <li><a href="#gallery" class="nav-link">Gallery</a></li>
    <li><a href="#about" class="nav-link">About</a></li>
    <li><a href="#contact" class="nav-link">Contact</a></li>
</ul>
```

Ensure the `href` values match the `id` of your sections.

## 🎯 Advanced Customization

### Changing Fonts

**Option 1: Using Google Fonts**
Add to `<head>` in `index.html`:
```html
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&display=swap" rel="stylesheet">
```

Update in `styles.css`:
```css
body {
    font-family: 'Playfair Display', serif;
}
```

### Adding More Gallery Items

Simply duplicate an existing `gallery-item` div and modify:
1. Change image/video source
2. Update artwork information
3. Set appropriate `data-category`
4. Adjust status (available/sold)

### Modifying Animations

All animations are defined in `styles.css` (Lines ~577-603). You can:
- Adjust animation duration
- Change animation timing functions
- Create new animations using CSS keyframes

### Customizing Background Patterns

Background patterns are created using CSS gradients. Find them in:
- Hero pattern: `styles.css` (Lines ~100-104)
- Gallery pattern: `styles.css` (Lines ~119-126)
- Contact pattern: `styles.css` (Lines ~419-426)

## 🛠️ Technical Details

### Technologies Used
- **HTML5** - Structure and content
- **CSS3** - Styling, animations, and responsive design
- **Vanilla JavaScript** - Interactivity (no frameworks required)
- **Font Awesome 6.4.0** - Social media icons
- **CSS Grid & Flexbox** - Layout system

### Browser Compatibility
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

### Performance Features
- Lazy video loading with Intersection Observer
- Debounced scroll events
- Optimized CSS animations
- Responsive images

## 📱 Responsive Breakpoints

The site adapts to different screen sizes:
- **Desktop:** 1200px and above
- **Tablet:** 768px - 1199px
- **Mobile:** 480px - 767px
- **Small Mobile:** Below 480px

## 🐛 Troubleshooting

### Images Not Displaying
- Check file paths are correct
- Ensure images are in the correct folder
- Verify image file extensions match the HTML

### Videos Not Autoplaying
- Ensure videos are muted (required for autoplay)
- Check video format is MP4
- Verify video file paths

### Contact Form Not Working
- Implement a form service (see Contact Form Setup)
- Check browser console for JavaScript errors

### Layout Issues on Mobile
- Clear browser cache
- Test in multiple browsers
- Check for any custom CSS overrides

### Navigation Not Scrolling
- Ensure section IDs match navigation href values
- Check JavaScript console for errors
- Verify `script.js` is properly linked

## 📝 Content Checklist

Before going live, make sure you've updated:

- [ ] Artist name/logo in navigation
- [ ] Hero title and subtitle
- [ ] About section biography
- [ ] Artist statement
- [ ] All placeholder images replaced
- [ ] All placeholder videos replaced
- [ ] Artwork titles, mediums, and prices
- [ ] Gallery categories/filters
- [ ] Social media links
- [ ] Contact form (connected to email service)
- [ ] Footer copyright year
- [ ] Page title and meta description
- [ ] Favicon (optional but recommended)

## 🎨 SEO & Optimization Tips

### Adding a Favicon
Create a `favicon.ico` file and add to `<head>`:
```html
<link rel="icon" type="image/x-icon" href="favicon.ico">
```

### Meta Tags for Social Sharing
Add these to `<head>` in `index.html`:
```html
<meta property="og:title" content="Your Name - Visual Artist">
<meta property="og:description" content="Your artist description">
<meta property="og:image" content="URL_to_preview_image.jpg">
<meta property="og:url" content="https://yourwebsite.com">
<meta name="twitter:card" content="summary_large_image">
```

### Image Optimization
- Compress images using [TinyPNG](https://tinypng.com/) or [Squoosh](https://squoosh.app/)
- Use WebP format for better compression (with JPG fallback)
- Add descriptive alt text for accessibility

## 📄 License

This portfolio template is free to use for personal and commercial projects. Attribution is appreciated but not required.

## 🤝 Support

If you encounter issues or need help customizing:
1. Check this README thoroughly
2. Review the code comments in each file
3. Search for solutions online (Stack Overflow, MDN Web Docs)
4. Consider hiring a web developer for complex customizations

## 🎉 Credits

- **Icons:** [Font Awesome](https://fontawesome.com/)
- **Placeholder Images:** [Placeholder.com](https://placeholder.com/)
- **Placeholder Videos:** Google Test Videos

---

**Made with ❤️ for visual artists. Good luck with your portfolio!**
