# Unit 01 — Practice Exercises

Welcome to the **Unit 01 Practice Suite**! Complete these hands-on exercises in your own test HTML files to solidify your understanding of HTML document structure, tags, elements, attributes, metadata, and browser rendering.

---

## 🟢 Level 1 — Basic Concept Tasks

### Task 1.1: HTML Boilerplate Creation
- **Objective**: Write a complete HTML5 standard skeleton from scratch without copying and pasting.
- **Requirements**:
  - Include `<!DOCTYPE html>`.
  - Include `<html lang="en">`.
  - Include `<head>` with UTF-8 charset and Viewport meta tag.
  - Set title to `"Level 1 - Task 1.1"`.
  - Add an `<h1>` element inside `<body>` with text `"HTML Boilerplate Created"`.
- **Expected Result**: A valid HTML5 file that opens in Chrome with a visible heading and browser tab title.

### Task 1.2: Working with Comments
- **Objective**: Practice single-line and multi-line HTML comments.
- **Requirements**:
  - Create an HTML file with 2 visible paragraph elements (`<p>`).
  - Add a single-line comment above the first paragraph explaining what it contains.
  - Add a multi-line comment between the two paragraphs explaining that comments are ignored by the browser.
- **Expected Result**: When opened in Chrome, only the 2 paragraphs are displayed on screen. When viewing page source or Inspecting, the comments are visible.

### Task 1.3: HTML Attributes Assignment
- **Objective**: Apply global attributes (`id`, `class`, `title`).
- **Requirements**:
  - Create an `<h1>` tag with `id="main-title"` and `title="This is the main title tooltip"`.
  - Create a `<p>` tag with `class="intro-text"`.
- **Expected Result**: Hovering over the `<h1>` heading in your browser reveals the tooltip pop-up.

### Task 1.4: Void Element Demonstration
- **Objective**: Use line break (`<br>`) and horizontal rule (`<hr>`) void elements.
- **Requirements**:
  - Write a paragraph containing 3 lines of address separated by `<br>` tags.
  - Place a horizontal line (`<hr>`) after the address paragraph.
- **Expected Result**: The address renders on 3 distinct lines inside a single paragraph, followed by a visible horizontal divider rule.

### Task 1.5: Character Encoding Verification
- **Objective**: Verify that `UTF-8` character encoding displays emojis and non-English scripts.
- **Requirements**:
  - Add `<meta charset="UTF-8">` in `<head>`.
  - Inside `<body>`, add a paragraph with text containing Hindi script and emojis (e.g. `"कोडिंग की दुनिया 🚀🔥"`).
- **Expected Result**: The text and emojis display cleanly without junk symbols (like ``).

---

## 🟡 Level 2 — Concept-Based Questions & Debugging

### Task 2.1: Debugging Invalid Nesting
- **Objective**: Identify and fix invalid nesting syntax.
- **Given Code**:
  ```html
  <body>
      <p>Welcome to <strong>my personal profile page</p></strong>
  </body>
  ```
- **Task**: Explain why this nesting is invalid according to W3C standards and write the corrected code.

### Task 2.2: Tag vs Element Identification
- **Objective**: Distinguish between tags and elements.
- **Given Snippet**:
  `<h2 id="section-1">Learning Web Development</h2>`
- **Questions**:
  1. What is the opening tag?
  2. What is the closing tag?
  3. What is the attribute name and value?
  4. What constitutes the complete HTML element?

### Task 2.3: Head vs Body Placement Check
- **Objective**: Correct misplaced HTML elements.
- **Given Code**:
  ```html
  <!DOCTYPE html>
  <html>
  <head>
      <h1>My Tech Blog</h1>
      <title>Tech Blog</title>
  </head>
  <body>
      <p>Latest articles on JavaScript and HTML.</p>
  </body>
  </html>
  ```
- **Task**: Point out the error in this HTML file and rewrite it cleanly.

### Task 2.4: Void Tag Syntax Bug Fix
- **Objective**: Fix invalid closing tag syntax on void elements.
- **Given Code**:
  ```html
  <hr>Content inside line</hr>
  <br>Line break text</br>
  ```
- **Task**: Explain why this code throws errors/unexpected browser behavior and fix it.

### Task 2.5: Attribute Syntax Audit
- **Objective**: Fix common attribute syntax errors.
- **Given Code**:
  ```html
  <p class=intro text id="101" title=Welcome>Hello</p>
  ```
- **Task**: Identify 2 attribute syntax mistakes and write the compliant HTML code.

---

## 🟠 Level 3 — Practical Webpage Creation Tasks

### Task 3.1: Developer Bookmark Page
- **Objective**: Build a clean HTML structure from scratch.
- **Requirements**:
  - Page title: `"Developer Resource Bookmark"`.
  - Primary heading (`<h1>`): `"Essential Web Dev Links"`.
  - Two section headings (`<h2>`): `"JavaScript Documentation"` and `"HTML5 Standards"`.
  - Paragraph description under each heading with `id` attributes set.
  - Horizontal rules separating the sections.
- **Expected Result**: A well-structured HTML page containing clean headings, paragraphs, and dividers.

### Task 3.2: Multi-Language Announcement Card
- **Objective**: Practice document language and nested container structure.
- **Requirements**:
  - Root element with `lang="en"`.
  - A container `<div>` with `id="announcement-card"`.
  - An `<h1>` heading `"Global Tech Conference 2026"`.
  - Paragraph 1 in English.
  - Paragraph 2 in Hindi (`<p lang="hi">`).
- **Expected Result**: A clean card container containing multi-lingual content rendered properly by the browser.

### Task 3.3: Inspecting DOM Nodes with Chrome DevTools
- **Objective**: Observe browser parsing mechanics.
- **Steps**:
  1. Open your created HTML file from Task 3.1 in Chrome.
  2. Press `F12` (or Right Click → Inspect).
  3. Go to the **Elements** tab.
  4. Expand the `<html>`, `<head>`, and `<body>` tags.
  5. Edit the text inside `<h1>` directly within DevTools DOM tree and observe the live browser window.
- **Deliverable**: Write a 2-line summary in your notes about what happens when you edit DOM nodes in DevTools vs modifying the original file.

---

## 🔴 Level 4 — Mini Real-World Challenge

### Challenge: Course Enrollment Confirmation Card
- **Goal**: Create an HTML-only enrollment confirmation card for a Full Stack MERN Course.
- **Specifications**:
  - **File Name**: `my_enrollment.html`
  - **Document Metadata**:
    - Proper HTML5 DOCTYPE declaration.
    - Title: `"Enrollment Confirmation - Full Stack Course"`.
    - Character set UTF-8 and responsive viewport meta tag.
  - **Visible Viewport Structure**:
    - Main Header (`<h1>`): `"Full Stack Development Course"` with `id="course-header"`.
    - Subheading (`<h2>`): `"Student Profile Details"`.
    - Paragraph containing Student Name, Registration ID (use `<br>` for line breaks).
    - Subheading (`<h2>`): `"Enrolled Modules"`.
    - Nested `<div>` container with `id="module-box"` containing:
      - Paragraph 1: `"Module 1: JavaScript Fundamentals (Completed ✅)"`
      - Paragraph 2: `"Module 2: HTML5 & Web Architecture (In Progress ⏳)"`
    - Horizontal divider rule (`<hr>`).
    - Footer paragraph with copyright notice and `title` attribute.
  - **Comments**: Include at least 3 descriptive HTML comments explaining the sections.

---

*Once you complete Level 4, attempt [mini_challenge.html](mini_challenge.html) in your editor!* 🚀
