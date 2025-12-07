# Complete Portfolio Website Prompt - HTML/CSS/JS Only

## IMPORTANT: GitHub Pages Compatibility
**Build using ONLY HTML, CSS, and vanilla JavaScript** - GitHub Pages supports these perfectly!
No React, TypeScript, or build tools needed. Pure static files work best.

---

## TECH STACK (GitHub Pages Compatible)
- **HTML5** - Semantic markup
- **CSS3** - Modern styling with CSS Variables, Grid, Flexbox
- **Vanilla JavaScript** - No frameworks, pure JS for interactions
- **Font Awesome** - For icons (CDN)
- **Google Fonts** - Inter font family (CDN)

---

## PROJECT STRUCTURE
```
portfolio/
├── index.html          # Single page with all sections
├── styles.css          # All styling
├── script.js           # All JavaScript interactions
└── README.md           # Documentation
```

---

## DESIGN & COLOR SCHEME
- **Primary Background:** #0a192f (Deep navy blue)
- **Secondary Background:** #112240 (Lighter navy)
- **Card Background:** #1e293b, #1a2332 (Semi-transparent dark blue)
- **Accent Blue:** #6366f1 (Electric blue)
- **Accent Purple:** #8b5cf6 (Purple)
- **Primary Gradient:** linear-gradient(135deg, #6366f1, #8b5cf6)
- **Text Primary:** #ffffff (White)
- **Text Secondary:** #e2e8f0 (Light gray)
- **Text Muted:** #94a3b8 (Muted gray)

---

## CRITICAL CSS FIXES (MUST IMPLEMENT)

### 1. Social Icons Alignment Fix
**Problem:** Icons appearing misaligned or floating incorrectly
**Solution:**
```css
.social-links {
    display: flex;
    gap: 20px;
    justify-content: center;
    margin-bottom: 40px;
    align-items: center;  /* CRITICAL: Prevents misalignment */
}

.social-icon {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: var(--card-bg);
    display: flex;
    align-items: center;      /* CRITICAL */
    justify-content: center;  /* CRITICAL */
    color: var(--text-primary);
    font-size: 20px;
    text-decoration: none;
    transition: var(--transition);
}
```

### 2. CSS Class Name Spacing
**CRITICAL:** Ensure NO SPACES in CSS class selectors
- ✅ CORRECT: `.social-links {`
- ❌ WRONG: `. social-links {`
- ✅ CORRECT: `.nav-buttons {`
- ❌ WRONG: `.na v-buttons {`

Check these classes specifically:
- `.social-links`
- `.nav-buttons`
- `.timeline-item`
- `.timeline-content`
- `.contact-card`
- `.about-image`
- `.cert-item`
- `.project-date`
- `.fade-in-delay-1`
- `.scroll-top`

---

## LAYOUT STRUCTURE

### Navigation Bar (Sticky)
```html
<nav class="navbar" id="navbar">
    <div class="container nav-container">
        <div class="logo">
            <span class="gradient-text">Mustafa Nasser</span>
        </div>
        <div class="nav-menu" id="navMenu">
            <a href="#home" class="nav-link">Home</a>
            <a href="#about" class="nav-link">About</a>
            <a href="#skills" class="nav-link">Skills</a>
            <a href="#experience" class="nav-link">Experience</a>
            <a href="#projects" class="nav-link">Projects</a>
            <a href="#contact" class="nav-link">Contact</a>
        </div>
        <div class="nav-buttons">
            <a href="#contact" class="btn btn-primary">Contact Me</a>
            <a href="#projects" class="btn btn-outline">View My Work</a>
        </div>
        <button class="hamburger" id="hamburger">
            <span></span>
            <span></span>
            <span></span>
        </button>
    </div>
</nav>
```

**Features:**
- Fixed position with backdrop-filter: blur(10px)
- Glassmorphism effect
- Smooth scroll to sections
- Mobile hamburger menu
- Gradient text on logo

---

### Hero Section
```html
<section class="hero" id="home">
    <div class="hero-background">
        <div class="orb orb-1"></div>
        <div class="orb orb-2"></div>
        <div class="orb orb-3"></div>
    </div>
    <div class="container hero-content">
        <h1 class="hero-title fade-in">
            Hi, I'm <span class="gradient-text typing-text" id="typingName">Mustafa Nasser</span>
        </h1>
        <p class="hero-subtitle fade-in-delay-1" id="typingRole">AI & Automation Engineer | Web Scraper Expert</p>
        <p class="hero-tagline fade-in-delay-2">
            Passionate about building intelligent systems that automate complex workflows,<br>
            extract insights from data, and solve real-world problems using cutting-edge AI technologies.
        </p>
        <div class="social-links fade-in-delay-3">
            <a href="https://github.com/mostafanasser" target="_blank" class="social-icon">
                <i class="fab fa-github"></i>
            </a>
            <a href="https://linkedin.com/in/mostafanasser" target="_blank" class="social-icon">
                <i class="fab fa-linkedin"></i>
            </a>
            <a href="https://wa.me/201098974486" target="_blank" class="social-icon">
                <i class="fab fa-whatsapp"></i>
            </a>
            <a href="mailto:mostafanasser3786@gmail.com" class="social-icon">
                <i class="fas fa-envelope"></i>
            </a>
        </div>
        <a href="#about" class="btn btn-primary btn-hero fade-in-delay-4">Learn More About Me</a>
        <div class="scroll-indicator">
            <div class="mouse">
                <div class="wheel"></div>
            </div>
        </div>
    </div>
</section>
```

**Features:**
- Animated gradient orbs background
- Typing animation effect
- Social icons with hover animations (rotate 360deg)
- Scroll indicator with bounce animation
- Fade-in animations with delays

---


### About Section
**Two-column responsive layout:**
- Left: Bio text (3-4 paragraphs)
- Right: Profile image with gradient border
- Info items: Location, Experience, Email with icons
- Two cards: "What I Do" and "Key Services"

**Hover Effects:**
- Cards lift up: `transform: translateY(-8px)`
- Box shadow with colored glow
- Fade-in on scroll using Intersection Observer

---

### Skills Section
**Grid Layout:** 3 columns (desktop), 2 (tablet), 1 (mobile)

**Skill Categories:**
1. AI & Machine Learning (Blue #6366f1)
2. Web Scraping & API Integration (Green #10b981)
3. Desktop & Web Automation (Orange #f59e0b)
4. Data Processing & Analysis (Pink #ec4899)
5. Programming & Scripting (Purple #8b5cf6)
6. Tools & Platforms (Cyan #06b6d4)

**Card Features:**
- Colored icon with gradient background
- Category title
- Bullet list of technologies
- Hover: `scale(1.05)` + colored glow
- Staggered fade-in animation

---

### Experience Section (Timeline Style)
**Timeline with vertical line and dots**

**Job Cards:**
- Date badge (colored background)
- Job title (bold)
- Company name with link
- Location with icon
- Bullet points of responsibilities
- Left colored border
- Hover: slide right + shadow expansion

---

### Projects Section
**Grid Layout:** 2 columns (desktop), 1 (mobile)

**Project Cards:**
- Colored top border (unique per project)
- Icon with colored background
- Date badge
- Project title
- Description
- Technology tags
- "View Project" link with arrow
- Hover: lift + colored glow

---

### Contact Section
**Three contact cards in row:**
1. Email Card (Blue gradient icon)
2. Location Card (Green gradient icon)
3. Phone/WhatsApp Card (Purple gradient icon)

**Features:**
- Copy to clipboard functionality
- Social media links below
- Hover effects: lift + glow

---

### Footer
- Copyright text with dynamic year
- Scroll to top button (fixed bottom-right)
- Floating WhatsApp button (fixed bottom-right, above scroll button)

---

## ANIMATIONS & INTERACTIONS (Vanilla JS)

### 1. Smooth Scroll
```javascript
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
        e.preventDefault();
        const target = document.querySelector(this.getAttribute('href'));
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
    });
});
```

### 2. Scroll Animations (Intersection Observer)
```javascript
const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -100px 0px'
};

const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.classList.add('animated');
        }
    });
}, observerOptions);

document.querySelectorAll('.animate-on-scroll').forEach(el => observer.observe(el));
```

### 3. Navbar Scroll Effect
```javascript
window.addEventListener('scroll', () => {
    const navbar = document.getElementById('navbar');
    if (window.scrollY > 50) {
        navbar.classList.add('scrolled');
    } else {
        navbar.classList.remove('scrolled');
    }
});
```

### 4. Mobile Menu Toggle
```javascript
const hamburger = document.getElementById('hamburger');
const navMenu = document.getElementById('navMenu');

hamburger.addEventListener('click', () => {
    navMenu.classList.toggle('active');
    hamburger.classList.toggle('active');
});
```

### 5. Copy to Clipboard
```javascript
document.querySelectorAll('.copy-btn').forEach(btn => {
    btn.addEventListener('click', function() {
        const text = this.parentElement.dataset.clipboard;
        navigator.clipboard.writeText(text);
        this.textContent = 'Copied!';
        setTimeout(() => this.textContent = 'Copy', 2000);
    });
});
```

### 6. Scroll to Top Button
```javascript
const scrollTopBtn = document.getElementById('scrollTop');

window.addEventListener('scroll', () => {
    if (window.scrollY > 300) {
        scrollTopBtn.classList.add('visible');
    } else {
        scrollTopBtn.classList.remove('visible');
    }
});

scrollTopBtn.addEventListener('click', () => {
    window.scrollTo({ top: 0, behavior: 'smooth' });
});
```

### 7. Typing Animation (Optional)
```javascript
const typingText = document.getElementById('typingName');
const text = 'Mustafa Nasser';
let index = 0;

function type() {
    if (index < text.length) {
        typingText.textContent += text.charAt(index);
        index++;
        setTimeout(type, 100);
    }
}
// Call type() on page load if needed
```

---

## CSS ANIMATIONS

### Fade In
```css
@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}

.fade-in {
    animation: fadeIn 1s ease forwards;
}

.fade-in-delay-1 {
    animation: fadeIn 1s ease 0.2s forwards;
    opacity: 0;
}
```

### Gradient Shift
```css
@keyframes gradient-shift {
    0%, 100% {
        filter: hue-rotate(0deg);
    }
    50% {
        filter: hue-rotate(20deg);
    }
}

.gradient-text {
    background: linear-gradient(135deg, #6366f1, #8b5cf6);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: gradient-shift 3s ease infinite;
}
```

### Floating Orbs
```css
@keyframes float {
    0%, 100% {
        transform: translate(0, 0) scale(1);
    }
    33% {
        transform: translate(50px, -50px) scale(1.1);
    }
    66% {
        transform: translate(-50px, 50px) scale(0.9);
    }
}

.orb {
    animation: float 20s infinite ease-in-out;
}
```

### Scroll Indicator
```css
@keyframes scroll {
    0% {
        opacity: 1;
        top: 10px;
    }
    100% {
        opacity: 0;
        top: 30px;
    }
}

.wheel {
    animation: scroll 2s infinite;
}
```

### Pulse (WhatsApp Button)
```css
@keyframes pulse {
    0%, 100% {
        box-shadow: 0 10px 30px rgba(139, 92, 246, 0.4);
    }
    50% {
        box-shadow: 0 10px 40px rgba(139, 92, 246, 0.6);
    }
}

.floating-contact {
    animation: pulse 2s infinite;
}
```

---

## RESPONSIVE DESIGN

### Breakpoints
```css
/* Desktop: > 1024px (default) */

/* Tablet: 768px - 1024px */
@media (max-width: 1024px) {
    .skills-grid {
        grid-template-columns: repeat(2, 1fr);
    }
    .about-grid {
        grid-template-columns: 1fr;
    }
}

/* Mobile: < 768px */
@media (max-width: 768px) {
    .nav-menu, .nav-buttons {
        display: none;
    }
    .hamburger {
        display: flex;
    }
    .hero-title {
        font-size: 2.5rem;
    }
    .skills-grid {
        grid-template-columns: 1fr;
    }
    .projects-grid {
        grid-template-columns: 1fr;
    }
    .contact-cards {
        grid-template-columns: 1fr;
    }
}

/* Small Mobile: < 480px */
@media (max-width: 480px) {
    .hero-title {
        font-size: 2rem;
    }
    .btn {
        padding: 8px 20px;
        font-size: 0.9rem;
    }
}
```

---

## PERSONAL INFORMATION (REPLACE WITH YOUR DATA)

### Basic Info
```javascript
const personalInfo = {
    name: "Mustafa Nasser Anwar",
    title: "AI & Automation Engineer | Web Scraper Expert",
    tagline: "Passionate about building intelligent systems that automate complex workflows, extract insights from data, and solve real-world problems using cutting-edge AI technologies.",
    location: "Giza, Egypt",
    experience: "3+ Years",
    email: "mostafanasser3786@gmail.com",
    phone: "+201098974486",
    whatsapp: "201098974486"
};
```

### Social Links
```javascript
const socialLinks = {
    github: "https://github.com/mostafanasser",
    linkedin: "https://linkedin.com/in/mostafanasser",
    upwork: "https://www.upwork.com/freelancers/mostafanasser",
    whatsapp: "https://wa.me/201098974486",
    email: "mailto:mostafanasser3786@gmail.com"
};
```

### About Me
```javascript
const aboutMe = [
    "I'm an AI & Automation Engineer with 3+ years of experience in building intelligent systems that automate complex workflows, automate data extraction, and generate insights from structured and unstructured data using Python, machine learning, and advanced automation frameworks.",
    
    "Based in Giza, Egypt, I specialize in creating scalable solutions that bridge the gap between complex data sources and actionable business intelligence. My expertise spans web scraping, machine learning, process automation, and API development.",
    
    "I've successfully delivered 50+ projects on Upwork with 100% client satisfaction, working with international clients to solve complex automation challenges and extract valuable insights from data."
];
```

### Skills
```javascript
const skills = [
    {
        category: "AI & Machine Learning",
        icon: "fa-brain",
        color: "#6366f1",
        technologies: [
            "Data Preprocessing & Cleaning",
            "Model Training & Evaluation",
            "Scikit-learn, TensorFlow, Deep Learning APIs",
            "OpenCV, Data Augmentation"
        ]
    },
    {
        category: "Web Scraping & API Integration",
        icon: "fa-spider",
        color: "#10b981",
        technologies: [
            "BeautifulSoup, Selenium, Requests",
            "AJAX & JavaScript-heavy sites",
            "HTTP Requests, FastAPI",
            "Telegram Bots Automation"
        ]
    },
    {
        category: "Desktop & Web Automation",
        icon: "fa-robot",
        color: "#f59e0b",
        technologies: [
            "PyAutoGUI, Pywinuto",
            "UIAutomation (Windows)",
            "Selenium & Playwright",
            "Browser Integration"
        ]
    },
    {
        category: "Data Processing & Analysis",
        icon: "fa-chart-bar",
        color: "#ec4899",
        technologies: [
            "Pandas, NumPy",
            "Data Cleaning, Boolean Filtering",
            "Grouping, Aggregation",
            "Real-Time Visualization (Streamlit)"
        ]
    },
    {
        category: "Programming & Scripting",
        icon: "fa-code",
        color: "#8b5cf6",
        technologies: [
            "Python (Professional)",
            "Java (Professional)",
            "Node.js (Professional)",
            "C++ (Professional)"
        ]
    },
    {
        category: "Tools & Platforms",
        icon: "fa-tools",
        color: "#06b6d4",
        technologies: [
            "Git & GitHub",
            "Microsoft Office Suite",
            "Frida (Mobile Reverse Engineering)",
            "Various Development Tools"
        ]
    }
];
```

### Experience
```javascript
const experience = [
    {
        title: "HTML Parser & ML Engineering",
        company: "UNSEND App",
        companyUrl: null,
        location: "Remote",
        startDate: "Sep 2024",
        endDate: "Present",
        responsibilities: [
            "Developing advanced HTML parsing systems and integrating AI/LLM technologies for automated data processing and extraction",
            "Training language models (LM) to enhance text analysis capabilities",
            "Processing large-scale HTML documents with custom parsing algorithms",
            "Integrating LLM and API services for intelligent data processing",
            "Building scalable automation workflows for data extraction"
        ]
    },
    {
        title: "AI & Automation Engineer | Web Scraper Expert",
        company: "Freelance / Remote - Upwork",
        companyUrl: "https://www.upwork.com/freelancers/mostafanasser",
        location: "Remote",
        startDate: "Jan 2022",
        endDate: "Present",
        responsibilities: [
            "Specialized in building intelligent automation systems and advanced web scraping solutions for international clients",
            "Developed advanced web scraping solutions using Python, Selenium, BeautifulSoup",
            "Built scalable automation pipelines with FastAPI and database integration",
            "Created intelligent Telegram bots and desktop automation tools",
            "Delivered 50+ successful projects with 100% client satisfaction"
        ]
    }
];
```

### Projects
```javascript
const projects = [
    {
        title: "Intelligent Product Analytics & Sentiment Engine",
        description: "Comprehensive e-commerce intelligence platform that automatically scrapes product data from multiple sites, performs advanced sentiment analysis using NLP models, and generates actionable business insights through real-time dashboards.",
        icon: "fa-chart-line",
        color: "#6366f1",
        startDate: "May 2025",
        endDate: "June 2025",
        technologies: ["Python", "NLP", "Streamlit", "FastAPI"],
        link: null
    },
    {
        title: "Trading Bot Strategy-Based Automation",
        description: "Designed and implemented an automated trading bot using the Mt5 Executor library with actions based on configurable strategies.",
        icon: "fa-chart-candlestick",
        color: "#10b981",
        startDate: "Mar 2025",
        endDate: "May 2025",
        technologies: ["Python", "Mt5 Executor", "Trading Algorithms", "Automation"],
        link: null
    },
    {
        title: "Horse Racing Intelligence & ML Platform",
        description: "Comprehensive end-to-end platform combining advanced web scraping, data processing, and machine learning for horse racing analytics. Features intelligent data extraction, automated data cleaning, ML dataset generation, and predictive modeling.",
        icon: "fa-horse-head",
        color: "#f59e0b",
        startDate: "Jan 2024",
        endDate: "May 2024",
        technologies: ["Python", "Web Scraping", "Machine Learning", "Data Engineering", "Predictive Analytics"],
        link: null
    },
    {
        title: "Apple Account Management Tool",
        description: "Designed and built Apple account management automation tool that can run HTTP requests to simulate account creation, password reset, and region changes without browser automation.",
        icon: "fa-apple",
        color: "#ec4899",
        startDate: "Feb 2024",
        endDate: "Aug 2024",
        technologies: ["Python", "HTTP Requests", "Automation", "API Integration"],
        link: null
    },
    {
        title: "X API Reverse Engineering Specialist",
        description: "Comprehensive testing suite for X (Twitter) login flow analysis. Developed advanced tools for HAR file analysis, TLS client implementation, authentication flow replication, reverse engineering techniques, and automated tweet publishing tools.",
        icon: "fa-twitter",
        color: "#8b5cf6",
        startDate: "Recent Project",
        endDate: "",
        technologies: ["Python", "Reverse Engineering", "API Analysis", "TLS Client", "Security Testing"],
        link: null
    },
    {
        title: "Smart Home Automation Project",
        description: "Designed a smart home system using IoT devices and machine learning for predictive automation based on user behavior patterns.",
        icon: "fa-home",
        color: "#06b6d4",
        startDate: "Mar 2024",
        endDate: "June 2024",
        technologies: ["IoT", "Machine Learning", "Python", "Automation"],
        link: null
    }
];
```

---

## WHAT I DO & KEY SERVICES

### What I Do
- AI & Machine Learning Solutions
- Web Scraping & Data Extraction
- Process Automation
- API Development & Integration

### Key Services
- Custom Automation Tools
- Data Analysis & Visualization
- Telegram Bot Development
- Desktop & Web Automation

---

## CDN LINKS (Add to HTML <head>)

```html
<!-- Google Fonts -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">

<!-- Font Awesome -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
```

---

## META TAGS (SEO)

```html
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Mustafa Nasser - AI & Automation Engineer | Web Scraper Expert">
<meta property="og:title" content="Mustafa Nasser - AI & Automation Engineer">
<meta property="og:description" content="AI & Automation Engineer specializing in web scraping, machine learning, and intelligent automation systems">
<meta property="og:type" content="website">
<title>Mustafa Nasser - AI & Automation Engineer</title>
```

---
## COMMON ISSUES & SOLUTIONS

### Issue 1: Social Icons Misaligned
**Solution:** Add `align-items: center` to `.social-links`

### Issue 2: CSS Not Loading
**Solution:** Check file paths are relative (e.g., `href="styles.css"` not `href="/styles.css"`)

### Issue 3: Animations Not Working
**Solution:** Ensure Intersection Observer is implemented correctly

### Issue 4: Mobile Menu Not Closing
**Solution:** Add click event to close menu when nav link is clicked

### Issue 5: Smooth Scroll Not Working
**Solution:** Use `scroll-behavior: smooth` in CSS and JavaScript fallback

---

## PERFORMANCE OPTIMIZATION

1. **Minify CSS/JS** before deployment
2. **Optimize images** (use WebP format, compress)
3. **Lazy load images** below fold
4. **Use CDN** for fonts and icons
5. **Enable caching** with proper headers
6. **Reduce animations** on mobile for better performance

---

## ACCESSIBILITY

- Use semantic HTML tags
- Add ARIA labels to buttons and links
- Ensure keyboard navigation works
- Maintain proper heading hierarchy
- Provide alt text for images
- Ensure sufficient color contrast

---

## BROWSER COMPATIBILITY

- Chrome/Edge: Full support
- Firefox: Full support
- Safari: Full support (test backdrop-filter)
- Mobile browsers: Full support

---

## FINAL CHECKLIST

✅ All personal information updated  
✅ Social links working  
✅ Email and phone numbers correct  
✅ All sections present and styled  
✅ Animations smooth and professional  
✅ Responsive on all devices  
✅ No CSS spacing errors  
✅ JavaScript interactions working  
✅ Copy to clipboard functional  
✅ Smooth scroll implemented  
✅ Mobile menu working  
✅ GitHub Pages compatible  
✅ SEO meta tags added  
✅ Performance optimized  

---

**Version:** 3.0 - Complete & Production Ready  
**Last Updated:** December 2024  
**GitHub Pages:** ✅ Fully Compatible  
**Status:** Ready for Deployment 🚀
