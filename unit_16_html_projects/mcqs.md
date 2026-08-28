# Unit 16 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your knowledge of HTML project architecture, multi-page site navigation, semantic page assembly, form application structures, and full-stack integration.

---

### Q1. What is the standard root filename for the primary home/landing page in a web project?

A. `main.html`  
B. `index.html`  
C. `home.html`  
D. `default.html`  

**Answer:** B

**Explanation:** Web servers (Apache, Nginx, Express) default to serving `index.html` as the directory landing page.

---

### Q2. What folder convention is standard for storing media assets like images, SVGs, and PDFs in web projects?

A. `/code`  
B. `/assets` (or `/assets/images`)  
C. `/temp`  
D. `/src_files`  

**Answer:** B

**Explanation:** `/assets/images` is the industry-standard folder structure for organizing project static image assets.

---

### Q3. How should a link inside `pages/about.html` navigate back to `index.html` in the root project folder?

A. `<a href="index.html">`  
B. `<a href="../index.html">`  
C. `<a href="root/index.html">`  
D. `<a href="./index.html">`  

**Answer:** B

**Explanation:** `../index.html` moves one directory level UP out of the `pages/` subfolder into the root directory to locate `index.html`.

---

### Q4. Which HTML tag structure is recommended for building a site's top navigation bar?

A. `<div class="nav">`  
B. `<header>` containing a `<nav>` with a `<ul>` list of `<a>` links  
C. `<main>` containing `<p>` links  
D. `<footer>` containing `<button>`  

**Answer:** B

**Explanation:** Encapsulating `<ul>` links inside `<nav>` within `<header>` provides the standard accessible navigation header architecture.

---

### Q5. What attribute MUST be set on a `<form>` when building a user registration page that accepts profile image uploads?

A. `method="GET"`  
B. `enctype="multipart/form-data"`  
C. `type="upload"`  
D. `file="true"`  

**Answer:** B

**Explanation:** `enctype="multipart/form-data"` is required on forms to transmit binary file uploads to backend servers.

---

### Q6. Which semantic tag is ideal for wrapping individual blog post preview cards in a portfolio project?

A. `<div>`  
B. `<article>`  
C. `<aside>`  
D. `<span>`  

**Answer:** B

**Explanation:** Each blog post card is a self-contained, independent unit best represented by `<article>`.

---

### Q7. How do you prevent Cumulative Layout Shift (CLS) on project image cards?

A. Add `loading="lazy"` only  
B. Set explicit `width` and `height` attributes on all `<img>` tags  
C. Hide images  
D. Use GIF format  

**Answer:** B

**Explanation:** Specifying explicit `width` and `height` pixel dimensions allows the browser to reserve layout space during page loading, preventing CLS jumps.

---

### Q8. What element should encapsulate a technical system diagram alongside its figure caption text?

A. `<figure>` containing `<img>` and `<figcaption>`  
B. `<div>` containing `<img>` and `<p>`  
C. `<table>`  

**Answer:** A

**Explanation:** `<figure>` and `<figcaption>` provide the semantic HTML5 structure for diagrams and media captions.

---

### Q9. What HTML element should wrap the sidebar containing author bio and related links on a blog page?

A. `<main>`  
B. `<aside>`  
C. `<header>`  

**Answer:** B

**Explanation:** `<aside>` represents secondary content tangentially related to the main page content, such as sidebars.

---

### Q10. What HTML attribute on `<a href="resume.pdf">` forces the browser to download the PDF rather than previewing it inline?

A. `download="My_Resume.pdf"`  
B. `target="_blank"`  
C. `rel="nofollow"`  

**Answer:** A

**Explanation:** The `download` attribute instructs the browser to trigger a direct file download action.

---

### Q11. Which input type should be used to securely collect user account passwords during registration?

A. `<input type="text">`  
B. `<input type="password">`  
C. `<input type="hidden">`  

**Answer:** B

**Explanation:** `type="password"` masks entered characters into dots for visual privacy.

---

### Q12. How do you format currency values like Indian Rupees in HTML project templates safely?

A. Write `Rs` string  
B. Use the HTML Entity `&#8377;` (e.g. `&#8377; 999`)  
C. Use `<script>`  

**Answer:** B

**Explanation:** HTML entity `&#8377;` displays the official Indian Rupee symbol `₹` consistently across all operating systems.

---

### Q13. Which element should contain the unique primary content of a project page?

A. `<main>`  
B. `<header>`  
C. `<footer>`  

**Answer:** A

**Explanation:** `<main>` encloses the primary content unique to that specific page.

---

### Q14. What form attribute connects an input to a `<datalist id="skills">` for search suggestions?

A. `list="skills"`  
B. `datalist="skills"`  
C. `target="skills"`  

**Answer:** A

**Explanation:** The `list` attribute on `<input>` connects it to the corresponding `<datalist id="...">`.

---

### Q15. In a resume project, what table section tag should wrap column headers like "Degree", "University", and "Year"?

A. `<tbody>`  
B. `<thead>`  
C. `<tfoot>`  

**Answer:** B

**Explanation:** `<thead>` contains header rows (`<tr><th>...</th></tr>`) for table columns.

---

### Q16. What is the benefit of adding `rel="noopener noreferrer"` to external social media links on a portfolio page?

A. Changes link color  
B. Prevents tabnabbing security vulnerabilities when opening links in new tabs (`target="_blank"`)  
C. Hides links  

**Answer:** B

**Explanation:** `rel="noopener noreferrer"` protects against security attacks by severing `window.opener` access in newly opened tabs.

---

### Q17. How should decorative icons (like star dividers) be configured for screen reader accessibility?

A. Use `alt="star icon"`  
B. Use `alt=""` or `aria-hidden="true"`  
C. Omit the image  

**Answer:** B

**Explanation:** Decorative graphics should use `alt=""` or `aria-hidden="true"` so screen readers skip announcing irrelevant visual noise.

---

### Q18. What HTML tag creates a native collapsible FAQ accordion without writing custom JavaScript?

A. `<details>` and `<summary>`  
B. `<accordion>`  
C. `<toggle>`  

**Answer:** A

**Explanation:** `<details>` wraps the accordion container, and `<summary>` serves as the clickable heading tag.

---

### Q19. How many `<main>` tags should exist on a single HTML project page?

A. Multiple  
B. Exactly 1  
C. Zero  

**Answer:** B

**Explanation:** Each HTML page must contain exactly one `<main>` element for semantic and accessibility compliance.

---

### Q20. What is the complete technical stack sequence represented by MERN?

A. HTML, CSS, JS, React  
B. MongoDB, Express.js, React, Node.js  
C. MySQL, Enterprise, Ruby, Node  

**Answer:** B

**Explanation:** MERN stands for MongoDB (Database), Express.js (Backend Framework), React (Frontend Library), and Node.js (JavaScript Runtime).

---

*End of Unit 16 MCQs! All 20 questions completed.* 🚀
