# Unit 04 — Practice Exercises

Welcome to the **Unit 04 Practice Suite**! Solve these 15 hands-on questions to master images, `alt` accessibility text, CLS prevention attributes, semantic `<figure>` containers, and native lazy loading performance. Every question has a corresponding solution in [practice_solutions.md](practice_solutions.md).

---

## 🟢 Level 1 — Basic Concept Questions

### Question 1.1: Basic Image Embedding with Dimensions
- **Difficulty**: Level 1 (Basic)
- **Goal**: Embed an image with explicit width, height, and alt text.
- **Requirements**:
  - Embed an image using `src="https://placehold.co/400x200"`.
  - Set `width="400"` and `height="200"`.
  - Set descriptive `alt="Sample placeholders image for basic concept test"`.
- **Expected Output**: A rendered 400x200 placeholder graphic.

### Question 1.2: Broken Image Fallback Test
- **Difficulty**: Level 1 (Basic)
- **Goal**: Verify browser behavior when `src` path fails.
- **Requirements**:
  - Write an `<img>` tag with a intentionally broken path `src="missing_photo.png"`.
  - Add descriptive fallback `alt="Student Profile Photo (Image unavailable)"`.
  - Set dimensions `width="150"` and `height="150"`.
- **Expected Output**: Browser renders a broken image placeholder displaying the descriptive fallback `alt` text.

### Question 1.3: Clickable Logo Link
- **Difficulty**: Level 1 (Basic)
- **Goal**: Create a clickable image logo linking to home page.
- **Requirements**:
  - Wrap an `<img>` element inside an `<a>` anchor tag.
  - Anchor `href="index.html"`.
  - Image `src="https://placehold.co/200x60/007bff/ffffff?text=Logo"`.
  - Set `alt="Company Logo - Click to return home"`.
- **Expected Output**: Hovering mouse changes cursor to pointer, clicking navigates to `index.html`.

### Question 1.4: Decorative Image with Empty Alt
- **Difficulty**: Level 1 (Basic)
- **Goal**: Mark a purely decorative background pattern.
- **Requirements**:
  - Embed decorative graphic `src="https://placehold.co/100x20/cccccc/ffffff?text=Divider"`.
  - Apply empty alt attribute `alt=""`.
- **Expected Output**: Screen readers ignore announcing the graphic, fulfilling accessibility standards.

### Question 1.5: Native Lazy Loading Attribute
- **Difficulty**: Level 1 (Basic)
- **Goal**: Configure native lazy loading for off-screen image.
- **Requirements**:
  - Embed an image with `src="https://placehold.co/600x300"`.
  - Add performance attribute `loading="lazy"`.
  - Set `width="600"` and `height="300"`.
- **Expected Output**: Browser defers fetching image until user scrolls near its position.

---

## 🟡 Level 2 — Concept-Based Questions & Debugging

### Question 2.1: CLS Prevention Audit
- **Difficulty**: Level 2 (Concept-Based)
- **Given Code**:
  ```html
  <img src="large_banner.jpg" alt="Company Hero Banner">
  ```
- **Task**: Explain what rendering issue (CLS) occurs with this code during network loading and rewrite it to adhere to PageSpeed best practices.

### Question 2.2: Refactoring Non-Semantic Image Captions
- **Difficulty**: Level 2 (Concept-Based)
- **Given Code**:
  ```html
  <div class="photo-box">
      <img src="sales_chart.png" alt="Sales Chart">
      <p>Figure 1: Q1 Revenue Analysis</p>
  </div>
  ```
- **Task**: Explain why this markup is non-semantic and refactor it using HTML5 `<figure>` and `<figcaption>` elements.

### Question 2.3: Inline SVG Vector Graphic Embedding
- **Difficulty**: Level 2 (Concept-Based)
- **Goal**: Embed a basic resolution-independent SVG circle graphic.
- **Requirements**:
  - Write an inline `<svg>` element with `width="100"` and `height="100"`.
  - Include a `<circle>` with `cx="50"`, `cy="50"`, `r="40"`, and `fill="green"`.
- **Expected Output**: A sharp green circle rendered via SVG XML code.

### Question 2.4: Accessible Image Alt Text Refactoring
- **Difficulty**: Level 2 (Concept-Based)
- **Given Code**:
  ```html
  <img src="chart_sales_2026.png" alt="image">
  <img src="profile_bhavishya.jpg" alt="photo.jpg">
  ```
- **Task**: Point out 2 accessibility violations in these `alt` attributes and rewrite them with descriptive, screen-reader-friendly text.

### Question 2.5: Image Format Selection Scenario
- **Difficulty**: Level 2 (Concept-Based)
- **Scenario**: You are building an e-commerce website. Match the 4 assets to their optimal format (**SVG, WebP, PNG, JPG**):
  1. Company brand logo requiring crisp vector scaling.
  2. Product catalog photograph (camera photo of shoes).
  3. Product icon with transparent background.
  4. Web banner needing high compression for modern browsers.

---

## 🟠 Level 3 — Practical Building Tasks

### Question 3.1: Technical Article Figure Component
- **Difficulty**: Level 3 (Practical)
- **Goal**: Create a technical diagram figure with detailed caption.
- **Requirements**:
  - Main Heading (`<h1>`): `"DOM Tree Construction"`.
  - `<figure>` container wrapping:
    - Image `src="https://placehold.co/550x250/333333/ffffff?text=DOM+Tree+Diagram"`.
    - `width="550"` and `height="250"`.
    - Descriptive `alt="DOM Tree diagram showing HTML root node branching into head and body children"`.
    - `<figcaption>`: `"Figure 2.1: Hierarchical DOM Tree Node Structure parsed from HTML5 source."`
- **Expected Output**: Clean semantic technical figure component.

### Question 3.2: E-Commerce Product Thumbnail Gallery
- **Difficulty**: Level 3 (Practical)
- **Goal**: Build a product media gallery layout with clickable thumbnails and main image.
- **Requirements**:
  - Main Product Image: `width="500" height="350"` with `loading="eager"`.
  - 3 Thumbnail Images inside a `<figure>` gallery:
    - Thumbnail 1: `width="150" height="100"`.
    - Thumbnail 2: `width="150" height="100"`.
    - Thumbnail 3: `width="150" height="100"`.
    - Captioned under `<figcaption>`: `"Product Angle Gallery Views."`
- **Expected Output**: Multi-image product gallery layout.

### Question 3.3: Below-the-Fold Lazy Loaded News Feed
- **Difficulty**: Level 3 (Practical)
- **Goal**: Implement loading performance strategy for article feed.
- **Requirements**:
  - Hero News Article Image (Above the fold): `loading="eager"`.
  - Add spacing paragraph (`margin-bottom: 500px`).
  - 2 Secondary News Images (Below the fold): `loading="lazy"`.
  - Set explicit `width` and `height` on all 3 images.
- **Expected Output**: Deferral of non-critical image requests until user scrolls.

### Question 3.4: Clickable Brand Partner Banner List
- **Difficulty**: Level 3 (Practical)
- **Goal**: Build an external partner logo bar using clickable images.
- **Requirements**:
  - Heading (`<h2>`): `"Our Tech Partners"`.
  - 3 clickable partner logos (`<a href="..." target="_blank" rel="noopener noreferrer"><img ...></a>`).
  - Each logo must have explicit dimensions (`width="180" height="60"`) and descriptive `alt` text.
- **Expected Output**: Secure, clickable partner logo gallery.

---

## 🔴 Level 4 — Mini Real-World Challenge

### Challenge: Photo Portfolio Showcase Component (`portfolio_gallery.html`)
- **Difficulty**: Level 4 (Mini Real-World Challenge)
- **Goal**: Build a complete photo showcase webpage containing a hero banner, multi-image figure gallery, SVG brand badge, lazy-loaded showcase items, and clickable social links.
- **File Name**: `portfolio_gallery.html`
- **Specifications**:
  1. Main Header (`<h1>`): `"Bhavishya - Developer Photography Portfolio"`.
  2. Clickable Header Logo Link (`<a href="index.html"><img ...></a>`).
  3. Inline SVG Badge (`<svg>`) representing a camera or verified badge icon.
  4. Hero Section: Primary photo inside `<figure>` with `loading="eager"`, explicit `width="800"` & `height="400"`, and detailed `<figcaption>`.
  5. Gallery Section: 3 showcase images inside a `<figure>` group using `loading="lazy"` and explicit dimensions (`width="250" height="180"`).
  6. All images MUST have descriptive `alt` text and explicit `width`/`height` attributes to prevent CLS.
  7. Footer: Copyright in `<small>` and decorative icon with `alt=""`.

---

*Once you attempt these questions, verify your answers in [practice_solutions.md](practice_solutions.md)!* 🚀
