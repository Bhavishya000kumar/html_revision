# Unit 04 — Practice Solutions

This document provides the complete, runnable HTML code, detailed explanations, and key learning points for all 15 practice questions in [practice.md](practice.md).

---

## 🟢 Level 1 Solutions — Basic Concept Questions

### Solution 1.1: Basic Image Embedding with Dimensions

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.1 - Basic Image</title>
</head>
<body>
    <h1>Basic Image Embedding</h1>

    <img src="https://placehold.co/400x200" 
         alt="Sample placeholders image for basic concept test" 
         width="400" 
         height="200">
</body>
</html>
```

#### Explanation & Browser Behavior:
- **`src`**: Specifies the URL location of the image file.
- **`width="400" height="200"`**: Allocates exact pixel space before image finishes downloading, preventing Cumulative Layout Shift (CLS).
- **`alt="..."`**: Provides descriptive fallback text.

---

### Solution 1.2: Broken Image Fallback Test

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.2 - Broken Image Fallback</title>
</head>
<body>
    <h1>Broken Image Fallback Test</h1>

    <!-- Intentionally broken src path -->
    <img src="missing_photo.png" 
         alt="Student Profile Photo (Image unavailable)" 
         width="150" 
         height="150">
</body>
</html>
```

#### Explanation & Browser Behavior:
- When `src` returns a 404 error, the browser displays a broken graphic icon alongside the descriptive fallback text inside the 150x150 reserved area.

---

### Solution 1.3: Clickable Logo Link

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.3 - Clickable Logo</title>
</head>
<body>
    <h1>Clickable Brand Logo Header</h1>

    <a href="index.html" title="Return to Home Page">
        <img src="https://placehold.co/200x60/007bff/ffffff?text=Logo" 
             alt="Company Logo - Click to return home" 
             width="200" 
             height="60">
    </a>
</body>
</html>
```

#### Explanation & Browser Behavior:
- Wrapping `<img>` inside `<a>` makes the entire graphic clickable, converting it into a navigation hyperlink.

---

### Solution 1.4: Decorative Image with Empty Alt

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.4 - Decorative Alt</title>
</head>
<body>
    <h1>Decorative Graphics</h1>

    <p>Welcome to our platform!</p>

    <!-- Empty alt="" attribute instructs screen readers to skip this graphic -->
    <img src="https://placehold.co/100x20/cccccc/ffffff?text=Divider" 
         alt="" 
         width="100" 
         height="20">
</body>
</html>
```

#### Explanation & Browser Behavior:
- `alt=""` signals to assistive technologies (screen readers) that the graphic is purely decorative and should not be vocalized.

---

### Solution 1.5: Native Lazy Loading Attribute

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.5 - Native Lazy Loading</title>
</head>
<body>
    <h1>Off-Screen Image Lazy Loading</h1>

    <img src="https://placehold.co/600x300" 
         alt="Off-screen lazy loaded placeholder image" 
         width="600" 
         height="300" 
         loading="lazy">
</body>
</html>
```

#### Explanation & Browser Behavior:
- `loading="lazy"` instructs the browser network manager to defer fetching the image asset until the user scrolls near its viewport position.

---

## 🟡 Level 2 Solutions — Concept-Based Questions & Debugging

### Solution 2.1: CLS Prevention Audit

#### Analysis of Problem:
- Omitting `width` and `height` causes the browser to render 0px height initially. When the image downloads, text below it gets suddenly pushed down, triggering a severe Cumulative Layout Shift (CLS).

#### Corrected HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.1 - CLS Fix</title>
</head>
<body>
    <img src="https://placehold.co/800x300?text=Hero+Banner" 
         alt="Company Hero Banner" 
         width="800" 
         height="300">
</body>
</html>
```

---

### Solution 2.2: Refactoring Non-Semantic Image Captions

#### Analysis of Problem:
- Using `<div class="photo-box">` and `<p>` provides no semantic context linking the text caption to the image element.

#### Corrected HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.2 - Semantic Figure</title>
</head>
<body>
    <figure>
        <img src="https://placehold.co/500x250?text=Sales+Chart" 
             alt="Bar chart displaying 40 percent Q1 revenue growth" 
             width="500" 
             height="250">
        <figcaption>Figure 1: Q1 Revenue Analysis Chart.</figcaption>
    </figure>
</body>
</html>
```

---

### Solution 2.3: Inline SVG Vector Graphic Embedding

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.3 - Inline SVG</title>
</head>
<body>
    <h1>Inline SVG Vector Graphic</h1>

    <svg width="100" height="100">
        <circle cx="50" cy="50" r="40" fill="green" />
    </svg>
</body>
</html>
```

#### Explanation & Browser Behavior:
- SVG graphics are XML-based vector code, rendering razor-sharp shapes at any display zoom without pixelation.

---

### Solution 2.4: Accessible Image Alt Text Refactoring

#### Analysis of Errors:
- `alt="image"` and `alt="photo.jpg"` are non-descriptive violations that fail Web Accessibility (a11y) standards.

#### Corrected HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.4 - Accessible Alt Text</title>
</head>
<body>
    <img src="https://placehold.co/400x200?text=Sales+2026" 
         alt="Annual sales growth bar chart for 2026 fiscal year" 
         width="400" 
         height="200">

    <img src="https://placehold.co/150x150?text=Bhavishya" 
         alt="Bhavishya Kumar headshot profile portrait" 
         width="150" 
         height="150">
</body>
</html>
```

---

### Solution 2.5: Image Format Selection Scenario

#### Answer & Selection Breakdown:
1. **Brand Logo requiring crisp vector scaling**: **SVG** (Infinite scaling, zero pixelation).
2. **Product Catalog Photograph (Camera photo)**: **JPG** or **WebP** (High color depth photo compression).
3. **Product Icon with transparent background**: **PNG** or **WebP** (Alpha channel transparency support).
4. **Web Banner needing high compression for modern browsers**: **WebP** (30% smaller file size than JPG/PNG).

---

## 🟠 Level 3 Solutions — Practical Building Tasks

### Solution 3.1: Technical Article Figure Component

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 3.1 - Technical Figure</title>
</head>
<body>
    <h1>DOM Tree Construction</h1>

    <figure>
        <img src="https://placehold.co/550x250/333333/ffffff?text=DOM+Tree+Diagram" 
             alt="DOM Tree diagram showing HTML root node branching into head and body children" 
             width="550" 
             height="250">
        <figcaption>Figure 2.1: Hierarchical DOM Tree Node Structure parsed from HTML5 source.</figcaption>
    </figure>
</body>
</html>
```

---

### Solution 3.2: E-Commerce Product Thumbnail Gallery

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 3.2 - Product Gallery</title>
</head>
<body>
    <h1>Wireless Noise-Canceling Headphones</h1>

    <!-- Main Image -->
    <img src="https://placehold.co/500x350/007bff/ffffff?text=Main+Product+Photo" 
         alt="Front view of black Wireless Noise-Canceling Headphones" 
         width="500" 
         height="350" 
         loading="eager">

    <!-- Thumbnails Figure -->
    <figure>
        <img src="https://placehold.co/150x100/6c757d/ffffff?text=Angle+1" alt="Headphones side angle view" width="150" height="100">
        <img src="https://placehold.co/150x100/6c757d/ffffff?text=Angle+2" alt="Headphones folded carrying case view" width="150" height="100">
        <img src="https://placehold.co/150x100/6c757d/ffffff?text=Angle+3" alt="Headphones audio cable connectivity view" width="150" height="100">
        <figcaption>Product Angle Gallery Views.</figcaption>
    </figure>
</body>
</html>
```

---

### Solution 3.3: Below-the-Fold Lazy Loaded News Feed

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 3.3 - News Feed Performance</title>
</head>
<body>
    <h1>Tech News Portal</h1>

    <!-- Above-the-fold hero image -->
    <img src="https://placehold.co/600x300/003366/ffffff?text=Breaking+News+Hero" 
         alt="Breaking tech news hero banner graphic" 
         width="600" 
         height="300" 
         loading="eager">

    <p style="margin-bottom: 500px;">(Scroll down to load secondary article graphics...)</p>

    <!-- Below-the-fold lazy loaded images -->
    <h2>Secondary Articles</h2>
    
    <img src="https://placehold.co/400x200/28a745/ffffff?text=Article+1+Image" 
         alt="AI software release infographic" 
         width="400" 
         height="200" 
         loading="lazy">

    <img src="https://placehold.co/400x200/17a2b8/ffffff?text=Article+2+Image" 
         alt="Cloud database architecture diagram" 
         width="400" 
         height="200" 
         loading="lazy">
</body>
</html>
```

---

### Solution 3.4: Clickable Brand Partner Banner List

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 3.4 - Partner Banner Bar</title>
</head>
<body>
    <h2>Our Tech Partners</h2>

    <p>
        <a href="https://google.com" target="_blank" rel="noopener noreferrer" title="Google Partner">
            <img src="https://placehold.co/180x60/ea4335/ffffff?text=Google" alt="Google Corporate Logo Link" width="180" height="60">
        </a>

        <a href="https://microsoft.com" target="_blank" rel="noopener noreferrer" title="Microsoft Partner">
            <img src="https://placehold.co/180x60/00a4ef/ffffff?text=Microsoft" alt="Microsoft Corporate Logo Link" width="180" height="60">
        </a>

        <a href="https://github.com" target="_blank" rel="noopener noreferrer" title="GitHub Partner">
            <img src="https://placehold.co/180x60/24292e/ffffff?text=GitHub" alt="GitHub Corporate Logo Link" width="180" height="60">
        </a>
    </p>
</body>
</html>
```

---

## 🔴 Level 4 Solution — Mini Real-World Challenge

### Solution 4.1: Photo Portfolio Showcase (`portfolio_gallery.html`)

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bhavishya - Developer Photography Portfolio</title>
</head>
<body>

    <!-- Header Logo & Title -->
    <header>
        <a href="index.html" title="Return to Home Page">
            <img src="https://placehold.co/180x50/007bff/ffffff?text=Bhavishya+Dev" 
                 alt="Bhavishya Dev Personal Logo Mark" 
                 width="180" 
                 height="50">
        </a>

        <!-- Inline SVG Verified Badge -->
        <svg width="24" height="24" viewBox="0 0 24 24" style="vertical-align: middle;">
            <circle cx="12" cy="12" r="10" fill="#28a745" />
            <path d="M9 12l2 2 4-4" stroke="white" stroke-width="2" fill="none" />
        </svg>

        <h1>Bhavishya - Developer Photography Portfolio</h1>
    </header>

    <hr>

    <!-- Main Hero Section -->
    <main>
        <h2>Featured Showcase Photograph</h2>

        <figure>
            <img src="https://placehold.co/800x400/003366/ffffff?text=Featured+Landscape+Photograph" 
                 alt="Panoramic mountain sunset landscape photograph during golden hour" 
                 width="800" 
                 height="400" 
                 loading="eager">
            <figcaption>Figure 1.1: Himalayan Mountain Sunset at Golden Hour. Captured in 2026.</figcaption>
        </figure>

        <hr>

        <!-- Gallery Showcase Section -->
        <h2>Project Gallery Showcase</h2>

        <figure>
            <img src="https://placehold.co/250x180/17a2b8/ffffff?text=City+Architecture" 
                 alt="Modern glass skyscraper reflection architecture photo" 
                 width="250" 
                 height="180" 
                 loading="lazy">

            <img src="https://placehold.co/250x180/fd7e14/ffffff?text=Nature+Macro" 
                 alt="Macro close up photograph of water droplet on leaf" 
                 width="250" 
                 height="180" 
                 loading="lazy">

            <img src="https://placehold.co/250x180/6f42c1/ffffff?text=Night+Astrophotography" 
                 alt="Long exposure Milky Way night sky photograph" 
                 width="250" 
                 height="180" 
                 loading="lazy">

            <figcaption>Figure 1.2: Specialized Portfolio Collections (Architecture, Nature Macro, and Astrophotography).</figcaption>
        </figure>
    </main>

    <hr>

    <!-- Footer -->
    <footer>
        <p>
            <!-- Decorative Icon with empty alt -->
            <img src="https://placehold.co/20x20/6c757d/ffffff?text=*" alt="" width="20" height="20">
            <small>&copy; 2026 Bhavishya Photography &amp; Web Development. All rights reserved.</small>
        </p>
    </footer>

</body>
</html>
```

---

*All 15 practice solutions verified! Proceed to [mcqs.md](mcqs.md) for 20 self-assessment MCQs.* 🚀
