# Modern Portfolio Website

A professional, modern portfolio website built with HTML, CSS, and JavaScript. Fully responsive and optimized for GitHub Pages deployment.

## Features

- ✨ Modern dark theme with gradient accents
- 🎨 Smooth animations and transitions
- 📱 Fully responsive design (mobile, tablet, desktop)
- 🚀 Optimized performance
- 💫 Interactive elements with hover effects
- 📊 Scroll animations using Intersection Observer
- 🎯 Smooth scrolling navigation
- 📋 Copy-to-clipboard functionality
- 🌟 Glassmorphism effects
- ⚡ Fast loading and lightweight

## Sections

1. **Navigation Bar** - Sticky navigation with smooth scroll
2. **Hero Section** - Eye-catching introduction with animated background
3. **About** - Professional bio and key information
4. **Skills** - Categorized technical skills with icons
5. **Experience** - Timeline-style work history
6. **Education** - Academic background and certifications
7. **Projects** - Featured projects showcase
8. **Contact** - Contact information with copy functionality
9. **Footer** - Copyright and scroll-to-top button

## Customization Guide

### 1. Personal Information

Edit `index.html` and replace the following:

- **Name**: Search for "Your Name" and replace with your actual name
- **Title/Role**: Replace "Full Stack Developer" with your role
- **Tagline**: Update the hero tagline text
- **Location**: Replace "Cairo, Egypt" with your location
- **Email**: Replace "your.email@example.com" with your email
- **Phone**: Replace "+20 123 456 7890" with your phone number

### 2. Social Links

Update all social media links in the HTML:
- GitHub: `https://github.com/yourusername`
- LinkedIn: `https://linkedin.com/in/yourusername`
- WhatsApp: `https://wa.me/1234567890`
- Twitter: `https://twitter.com/yourusername`

### 3. Profile Image

Replace the placeholder image URL in the About section:
```html
<img src="https://via.placeholder.com/400" alt="Profile Picture">
```
Upload your image to the repository and update the src path.

### 4. About Section

Edit the three paragraphs in the About section with your personal story.

### 5. Skills

Update the skill cards with your actual skills. Each card has:
- Icon (Font Awesome class)
- Category name
- List of technologies

### 6. Experience

Update the timeline items with your work history:
- Job title
- Company name and link
- Date range
- Location
- Responsibilities (bullet points)

### 7. Education

Update with your educational background:
- Degree name
- University
- Date range
- Description

### 8. Certifications

Add your certifications with:
- Certification name
- Provider/platform

### 9. Projects

Update project cards with your actual projects:
- Project name
- Description
- Technologies used
- Date range
- Project link (optional)

### 10. Contact Information

Update the contact cards with your actual information:
- Email
- Location
- WhatsApp number

## Deployment to GitHub Pages

### Step 1: Create a GitHub Repository

1. Go to GitHub and create a new repository
2. Name it `yourusername.github.io` (replace with your GitHub username)
3. Make it public

### Step 2: Upload Files

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository settings
2. Navigate to "Pages" section
3. Under "Source", select "main" branch
4. Click "Save"

Your website will be live at: `https://yourusername.github.io`

## File Structure

```
portfolio/
├── index.html          # Main HTML file
├── styles.css          # All CSS styles
├── script.js           # JavaScript functionality
└── README.md           # Documentation
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Performance

- Lightweight (< 100KB total)
- Fast loading time
- Optimized animations (60fps)
- Minimal dependencies (only Font Awesome for icons)

## Credits

- Font: Inter (Google Fonts)
- Icons: Font Awesome 6.4.0
- Design: Custom modern dark theme

## License

Free to use for personal portfolios. Please customize with your own information.

---

**Note**: Remember to replace all placeholder content with your actual information before deploying!
