# Unit 02 — Practice Exercises

Welcome to the **Unit 02 Practice Suite**! Solve these 15 hands-on questions to master headings, text formatting, preformatted blocks, and HTML entities. Every question has a corresponding solution in [practice_solutions.md](practice_solutions.md).

---

## 🟢 Level 1 — Basic Concept Questions

### Question 1.1: Standard Heading Hierarchy
- **Difficulty**: Level 1 (Basic)
- **Goal**: Build a 3-level document heading structure.
- **Requirements**:
  - Create a page with a single `<h1>` reading `"Web Development Roadmap 2026"`.
  - Add two `<h2>` subheadings: `"Frontend Stack"` and `"Backend Stack"`.
  - Under `"Frontend Stack"`, add an `<h3>` heading: `"HTML & CSS Fundamentals"`.
  - Add a short paragraph under each section.
- **Expected Output**: A logical document structure with decreasing heading sizes.

### Question 1.2: Formatting Chemical & Mathematical Formulas
- **Difficulty**: Level 1 (Basic)
- **Goal**: Use subscript (`<sub>`) and superscript (`<sup>`) elements.
- **Requirements**:
  - Render the chemical formula for Water: `H2O` (2 should be subscript).
  - Render the chemical formula for Carbon Dioxide: `CO2` (2 should be subscript).
  - Render the mathematical formula: `a2 + b2 = c2` (2s should be superscript).
  - Render ordinal date: `August 28th` (th should be superscript).
- **Expected Output**: Accurately baseline-aligned subscript and superscript characters in browser.

### Question 1.3: High Importance vs Visual Bold
- **Difficulty**: Level 1 (Basic)
- **Goal**: Apply `<strong>` and `<b>` appropriately.
- **Requirements**:
  - Write a security alert paragraph using `<strong>` for `"CRITICAL ERROR:"`.
  - Write a paragraph describing tech tools using `<b>` for `"VS Code"` and `"Chrome"`.
- **Expected Output**: Both render as bold text, but `<strong>` carries semantic weight for screen readers.

### Question 1.4: Highlight & Fine Print
- **Difficulty**: Level 1 (Basic)
- **Goal**: Use `<mark>` and `<small>` tags.
- **Requirements**:
  - Create a paragraph with the sentence: `"Search results found 3 matches for React in catalog."`, highlighting the word `"React"`.
  - Create a copyright footer paragraph using `<small>` containing `"© 2026 Developer Inc. All rights reserved."`.
- **Expected Output**: "React" has a yellow background highlight, and the copyright text appears in smaller font size.

### Question 1.5: Using Line Breaks vs Paragraphs
- **Difficulty**: Level 1 (Basic)
- **Goal**: Correctly apply `<br>` vs `<p>`.
- **Requirements**:
  - Write a multi-line company office address inside a single `<p>` tag using `<br>` between lines.
  - Write a separate `<p>` tag below it for contact telephone.
- **Expected Output**: Address lines stay closely spaced inside one paragraph block; contact telephone appears after a paragraph margin gap.

---

## 🟡 Level 2 — Concept-Based Questions & Debugging

### Question 2.1: Debugging Heading Order Violations
- **Difficulty**: Level 2 (Concept-Based)
- **Given Code**:
  ```html
  <h1>Company Portal</h1>
  <h4>Contact Support</h4>
  <p>Email: support@company.com</p>
  <h2>About Us</h2>
  ```
- **Task**: Identify 2 structural/SEO errors in this code and rewrite it according to proper HTML5 standards.

### Question 2.2: Escaping HTML Tags with Entities
- **Difficulty**: Level 2 (Concept-Based)
- **Goal**: Display raw HTML tags as plain visible text.
- **Requirements**:
  - Write a paragraph that explains HTML syntax: `"To create a heading in HTML, use the <h1> tag."`
  - Ensure the browser displays `<h1>` as literal text without rendering an actual heading element.
- **Expected Output**: Visible text on screen displaying `To create a heading in HTML, use the <h1> tag.`

### Question 2.3: Displaying Source Code Snippets
- **Difficulty**: Level 2 (Concept-Based)
- **Goal**: Combine `<pre>` and `<code>` elements.
- **Requirements**:
  - Render a multi-line JavaScript function block preserving 4-space indentation and line breaks:
    ```javascript
    function multiply(a, b) {
        return a * b;
    }
    ```
- **Expected Output**: Monospace-font indented code block rendered cleanly.

### Question 2.4: Semantic Emphasis Audit
- **Difficulty**: Level 2 (Concept-Based)
- **Given Code**:
  ```html
  <p>You <i>must</i> click save before exiting.</p>
  <p>The Latin term <em>et cetera</em> means and so on.</p>
  ```
- **Task**: Explain why the tag choices in this code are semantically inverted and fix the code.

### Question 2.5: Special Currency & Symbol Rendering
- **Difficulty**: Level 2 (Concept-Based)
- **Goal**: Use HTML entities for currency and trademark symbols.
- **Requirements**:
  - Display price in Indian Rupees: `₹ 1,499` (using entity `&#8377;`).
  - Display price in Euros: `€ 49` (using entity `&euro;`).
  - Display brand name with Registered Trademark: `TechCorp®` (using entity `&reg;`).
- **Expected Output**: Clean rendering of currency and trademark symbols.

---

## 🟠 Level 3 — Practical Building Tasks

### Question 3.1: Technical Blog Article Structure
- **Difficulty**: Level 3 (Practical)
- **Goal**: Combine headings, text formatting, code, and entities in a blog post snippet.
- **Requirements**:
  - Main Title (`<h1>`): `"Understanding JavaScript Scope"`.
  - Author & Date (`<small>`): `"Published by Bhavishya on August 28th, 2026"`.
  - Subheading (`<h2>`): `"What is Block Scope?"`.
  - Paragraph containing `<strong>` for important terms and inline `<code>` for `let` and `const`.
  - A `<pre><code>` block showing a 3-line code example.
- **Expected Output**: A structured technical article layout.

### Question 3.2: Academic Paper Abstract Component
- **Difficulty**: Level 3 (Practical)
- **Goal**: Format academic/scientific text with sub/superscripts and emphasis.
- **Requirements**:
  - `<h1>` title: `"Study on Water Purification (H2O)"`.
  - Abstract paragraph containing mathematical notation $E = mc^2$, chemical formula $H_2SO_4$, highlighted key terms, and Latin terms in `<i>`.
  - Divider rule (`<hr>`).
  - Citation fine print in `<small>`.
- **Expected Output**: Well-formatted academic abstract.

### Question 3.3: Product Release Announcement Page
- **Difficulty**: Level 3 (Practical)
- **Goal**: Use `<mark>`, `<strong>`, `<small>`, and special entities.
- **Requirements**:
  - `<h1>`: `"Announcing ProApp™ 2.0"`.
  - High importance paragraph with `<strong>` warning about legacy support.
  - Marked feature text (`<mark>`).
  - Price: `₹ 2,999` with Copyright fine print footer.
- **Expected Output**: Professional product announcement snippet.

### Question 3.4: HTML & CSS Cheat Sheet Component
- **Difficulty**: Level 3 (Practical)
- **Goal**: Use entities to display HTML tags in a cheat sheet table layout.
- **Requirements**:
  - Heading (`<h1>`): `"HTML Tag Cheat Sheet"`.
  - Paragraphs explaining tags: `&lt;h1&gt;` through `&lt;h6&gt;`, `&lt;p&gt;`, `&lt;br&gt;`, `&lt;hr&gt;`.
  - Use `<code>` formatting for all tag references.
- **Expected Output**: Clean, readable tag reference guide.

---

## 🔴 Level 4 — Mini Real-World Challenge

### Challenge: Documentation Page for a Developer Tool
- **Difficulty**: Level 4 (Mini Real-World Challenge)
- **Goal**: Build a complete, single-page HTML documentation snippet for a JavaScript utility library.
- **File Name**: `dev_tool_docs.html`
- **Specifications**:
  1. Single `<h1>`: `"StringUtil® Library Documentation"`.
  2. Subtitle in `<small>` with author copyright notice.
  3. `<h2>`: `"Overview"`. Paragraph explaining the library with `<strong>` and `<em>`.
  4. `<h2>`: `"Installation & Usage"`.
  5. `<h3>`: `"CLI Command"`. Code snippet in `<code>`.
  6. `<h3>`: `"Code Example"`. Multi-line code inside `<pre><code>`.
  7. `<h2>`: `"Syntax Reference"`. Text explaining HTML entities (`&lt;`, `&gt;`, `&amp;`).
  8. Use `<hr>` dividers between major sections.
  9. Add a `<mark>` highlight on the latest version number (`v2.4.0`).

---

*Once you attempt these questions, verify your answers in [practice_solutions.md](practice_solutions.md)!* 🚀
