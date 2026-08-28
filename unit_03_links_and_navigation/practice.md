# Unit 03 — Practice Exercises

Welcome to the **Unit 03 Practice Suite**! Solve these 15 hands-on questions to master links, relative file paths, internal page anchors, security best practices, and special protocols. Every question has a corresponding solution in [practice_solutions.md](practice_solutions.md).

---

## 🟢 Level 1 — Basic Concept Questions

### Question 1.1: Basic External Link
- **Difficulty**: Level 1 (Basic)
- **Goal**: Create an external link opening in a new tab securely.
- **Requirements**:
  - Create an anchor tag pointing to `https://react.dev`.
  - Open the link in a new browser tab (`target="_blank"`).
  - Apply the security attribute `rel="noopener noreferrer"`.
  - Add a hover tooltip using the `title` attribute.
  - Link display text should be `"Official React Documentation"`.
- **Expected Output**: Clicking the link opens `https://react.dev` in a new tab securely.

### Question 1.2: Relative Path in Same Folder
- **Difficulty**: Level 1 (Basic)
- **Goal**: Create relative links between files in the same directory.
- **Requirements**:
  - Write an HTML link on `index.html` pointing to `about.html` in the same directory.
  - Use both implicit (`href="about.html"`) and explicit (`href="./about.html"`) relative path notation.
- **Expected Output**: Clicking the link navigates to `about.html`.

### Question 1.3: Jump to Section Anchor Link
- **Difficulty**: Level 1 (Basic)
- **Goal**: Create an internal page jump link.
- **Requirements**:
  - Create a `<section id="faq">` element on the page.
  - Create an anchor link at the top of the page pointing to `#faq`.
  - Link text: `"Jump to Frequently Asked Questions"`.
- **Expected Output**: Clicking the link scrolls the browser window directly to the FAQ section.

### Question 1.4: Telephone Dialing Link
- **Difficulty**: Level 1 (Basic)
- **Goal**: Implement a `tel:` protocol link.
- **Requirements**:
  - Create an anchor link pointing to telephone number `+91 98765 43210`.
  - Display text: `"Call Customer Care"`.
- **Expected Output**: Clicking on mobile opens phone dialer with number pre-filled.

### Question 1.5: Basic Email Link
- **Difficulty**: Level 1 (Basic)
- **Goal**: Create a simple `mailto:` link.
- **Requirements**:
  - Link pointing to `contact@company.com`.
  - Display text: `"Email Us"`.
- **Expected Output**: Opens default email composer addressed to `contact@company.com`.

---

## 🟡 Level 2 — Concept-Based Questions & Debugging

### Question 2.1: Relative Directory Traversal Upwards (`../`)
- **Difficulty**: Level 2 (Concept-Based)
- **Folder Structure**:
  ```
  project/
  ├── index.html
  └── pages/
      └── contact.html
  ```
- **Task**: Write the relative anchor link inside `contact.html` that navigates UP one directory to `index.html`.

### Question 2.2: Tabnabbing Security Audit
- **Difficulty**: Level 2 (Concept-Based)
- **Given Code**:
  ```html
  <a href="https://external-partner.com" target="_blank">Partner Website</a>
  ```
- **Task**: Explain the security vulnerability in this code and write the corrected production-standard code.

### Question 2.3: Pre-filled Email Link Construction
- **Difficulty**: Level 2 (Concept-Based)
- **Goal**: Build a `mailto:` link with pre-filled subject and body text.
- **Requirements**:
  - Recipient: `admissions@college.edu`.
  - Subject: `"Course Inquiry"`.
  - Body: `"Hello, I want details about the Full Stack MERN course."`
- **Expected Output**: Opens mail client with recipient, subject, and body pre-filled.

### Question 2.4: Accessibility Audit for Link Text
- **Difficulty**: Level 2 (Concept-Based)
- **Given Code**:
  ```html
  <p>To view our complete pricing plans, <a href="pricing.html">click here</a>.</p>
  ```
- **Task**: Explain why `"click here"` is bad for Web Accessibility (a11y) and SEO, and rewrite the sentence cleanly.

### Question 2.5: Forced File Download Link
- **Difficulty**: Level 2 (Concept-Based)
- **Goal**: Force browser file download instead of inline PDF preview.
- **Requirements**:
  - Point to relative path `assets/brochure.pdf`.
  - Apply `download` attribute with suggested filename `"Tech_Course_Brochure.pdf"`.
- **Expected Output**: Browser prompts file save dialog on link click.

---

## 🟠 Level 3 — Practical Building Tasks

### Question 3.1: Multi-Page Navigation Bar Component
- **Difficulty**: Level 3 (Practical)
- **Goal**: Build a reusable multi-page navigation header bar.
- **Requirements**:
  - `<nav>` element containing 4 links:
    1. Home (`index.html`)
    2. About Us (`pages/about.html`)
    3. Services (`pages/services.html`)
    4. Contact (`pages/contact.html`)
  - Assume current file location is `index.html`.
- **Expected Output**: Clean HTML navigation bar linking to subfolders.

### Question 3.2: Single-Page Table of Contents Navigation
- **Difficulty**: Level 3 (Practical)
- **Goal**: Build a single-page documentation outline with jump links and top-of-page anchors.
- **Requirements**:
  - Top header `<h1>` with `id="top"`.
  - Table of contents list with 3 links: `#intro`, `#setup`, `#examples`.
  - 3 content sections with matching `id` attributes.
  - Under each section, add a `"< Back to Top"` link pointing to `#top`.
- **Expected Output**: Functional single-page jump navigation.

### Question 3.3: Developer Portfolio Header Links
- **Difficulty**: Level 3 (Practical)
- **Goal**: Combine email, phone, GitHub external link, and download resume link.
- **Requirements**:
  - Developer Name `<h1>`.
  - Contact links: Phone (`tel:`), Email (`mailto:`), GitHub (external with `target="_blank"` & `rel="noopener"`), Download Resume (`download`).
- **Expected Output**: Complete portfolio contact action header.

### Question 3.4: Parent Folder Directory Traversal Component
- **Difficulty**: Level 3 (Practical)
- **Folder Structure**:
  ```
  root/
  ├── assets/
  │   └── guide.pdf
  └── pages/
      └── dashboard/
          └── user.html
  ```
- **Task**: Write the anchor link inside `user.html` that navigates UP 2 levels to download `guide.pdf` inside the `assets` folder.

---

## 🔴 Level 4 — Mini Real-World Challenge

### Challenge: Multi-Page Educational Portal Navigation Architecture
- **Difficulty**: Level 4 (Mini Real-World Challenge)
- **Goal**: Create the primary `index.html` landing page for a multi-page education portal with clean links, path navigation, special contact actions, and page anchors.
- **File Name**: `portal_index.html`
- **Specifications**:
  1. Main Header (`<h1>`): `"TechEdu Portal 2026"`.
  2. Navigation Header (`<nav>`):
     - Home (`#top`)
     - Courses (`#courses-section`)
     - External Docs (`https://developer.mozilla.org` in new secure tab)
     - Contact (`#contact-section`)
  3. Section 1 (`<section id="courses-section">`):
     - List of 2 course pages: `pages/html_course.html` and `pages/js_course.html`.
  4. Section 2 (`<section id="contact-section">`):
     - Support Email (`mailto:` with pre-filled subject `"Portal Help"`).
     - Phone Support (`tel:`).
     - Download Portal Guide PDF (`download`).
  5. Back-to-Top link (`#top`).

---

*Once you attempt these questions, verify your answers in [practice_solutions.md](practice_solutions.md)!* 🚀
