# Unit 02 — Practice Solutions

This document provides the complete, runnable HTML code, detailed explanations, and key learning points for all 15 practice questions in [practice.md](practice.md).

---

## 🟢 Level 1 Solutions — Basic Concept Questions

### Solution 1.1: Standard Heading Hierarchy

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.1 - Heading Hierarchy</title>
</head>
<body>
    <h1>Web Development Roadmap 2026</h1>
    <p>A comprehensive guide to mastering modern web development.</p>

    <h2>Frontend Stack</h2>
    <p>Frontend development focuses on client-side user interface construction.</p>

    <h3>HTML &amp; CSS Fundamentals</h3>
    <p>Building semantic structure and beautiful visual layouts.</p>

    <h2>Backend Stack</h2>
    <p>Backend development manages server logic, APIs, and databases.</p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- **`<h1>`**: Serves as the unique primary title of the page outline.
- **`<h2>`**: Defines major structural sections ("Frontend Stack" and "Backend Stack").
- **`<h3>`**: Sub-topic nested logically inside the Frontend section.
- **Key Takeaway**: Maintains sequential heading order (`H1` → `H2` → `H3`) without skipping levels.

---

### Solution 1.2: Formatting Chemical & Mathematical Formulas

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.2 - Formulas</title>
</head>
<body>
    <h1>Scientific &amp; Mathematical Formulas</h1>

    <p>Water Chemical Formula: H<sub>2</sub>O</p>
    <p>Carbon Dioxide Formula: CO<sub>2</sub></p>
    <p>Pythagorean Theorem: a<sup>2</sup> + b<sup>2</sup> = c<sup>2</sup></p>
    <p>Event Date: August 28<sup>th</sup>, 2026</p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- **`<sub>`**: Lowers character baseline for chemical numbers (`H₂O`).
- **`<sup>`**: Raises character baseline for exponents ($a^2$) and ordinal suffixes ($28^{th}$).

---

### Solution 1.3: High Importance vs Visual Bold

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.3 - Strong vs B</title>
</head>
<body>
    <h1>Security &amp; Tech Stack Overview</h1>

    <p><strong>CRITICAL ERROR:</strong> Unauthorized access attempt detected. Change your master password immediately!</p>

    <p>Our development workflow utilizes <b>VS Code</b> for editing code and <b>Chrome</b> for browser rendering inspection.</p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- **`<strong>`**: Indicates high importance and urgent priority. Screen readers announce this with vocal emphasis.
- **`<b>`**: Bolds text for visual drawing attention without semantic weight.

---

### Solution 1.4: Highlight & Fine Print

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.4 - Mark and Small</title>
</head>
<body>
    <h1>Catalog Search Results</h1>

    <p>Search results found 3 matches for <mark>React</mark> in catalog.</p>

    <hr>

    <p><small>&copy; 2026 Developer Inc. All rights reserved.</small></p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- **`<mark>`**: Highlights matching search terms with a default yellow background.
- **`<small>`**: Renders legal disclaimers and copyright notices at reduced font scale.

---

### Solution 1.5: Using Line Breaks vs Paragraphs

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.5 - Address Line Breaks</title>
</head>
<body>
    <h1>Contact Information</h1>

    <p>
        Bhavishya Tech Headquarters<br>
        Plot No. 42, Tech Park Avenue<br>
        New Delhi, India - 110001
    </p>

    <p>Telephone: +91 98765 43210</p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- **`<br>`**: Keeps address lines together inside a single paragraph block without adding vertical paragraph margins.
- **Separate `<p>`**: Placed below to create a clean margin gap for phone details.

---

## 🟡 Level 2 Solutions — Concept-Based Questions & Debugging

### Solution 2.1: Debugging Heading Order Violations

#### Analysis of Errors:
1. **Skipped Heading Level**: Jumped from `<h1>` directly to `<h4>` ("Contact Support"), breaking screen reader navigation.
2. **Disorganized Structure**: `<h2>About Us` appears after `<h4>`, creating a broken document outline.

#### Corrected HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.1 - Corrected Headings</title>
</head>
<body>
    <h1>Company Portal</h1>

    <h2>About Us</h2>
    <p>Welcome to our official corporate portal.</p>

    <h2>Contact Support</h2>
    <p>Email: support@company.com</p>
</body>
</html>
```

---

### Solution 2.2: Escaping HTML Tags with Entities

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.2 - Escaping Tags</title>
</head>
<body>
    <h1>HTML Syntax Guide</h1>

    <p>To create a heading in HTML, use the &lt;h1&gt; tag.</p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- **`&lt;`**: Represents `<` (Less than).
- **`&gt;`**: Represents `>` (Greater than).
- Prevents browser from treating `<h1>` as an actual heading element.

---

### Solution 2.3: Displaying Source Code Snippets

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.3 - Code Block</title>
</head>
<body>
    <h1>JavaScript Function Syntax</h1>

<pre><code>function multiply(a, b) {
    return a * b;
}</code></pre>
</body>
</html>
```

#### Explanation & Browser Behavior:
- **`<pre>`**: Preserves line breaks and 4-space indentation.
- **`<code>`**: Signals to browsers and search engines that the content is computer code.

---

### Solution 2.4: Semantic Emphasis Audit

#### Analysis of Mistakes:
- Original code used `<i>` for urgent mandatory action ("must") and `<em>` for Latin term ("et cetera").
- **Correction**: `<em>` should be used for stress emphasis, and `<i>` for foreign phrases.

#### Corrected HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.4 - Semantic Fix</title>
</head>
<body>
    <p>You <em>must</em> click save before exiting.</p>
    <p>The Latin term <i>et cetera</i> means and so on.</p>
</body>
</html>
```

---

### Solution 2.5: Special Currency & Symbol Rendering

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.5 - Entities</title>
</head>
<body>
    <h1>Product Pricing &amp; Branding</h1>

    <p>India Price: &#8377; 1,499</p>
    <p>Europe Price: &euro; 49</p>
    <p>Brand Name: TechCorp&reg;</p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- **`&#8377;`**: Renders `₹`.
- **`&euro;`**: Renders `€`.
- **`&reg;`**: Renders `®`.

---

## 🟠 Level 3 Solutions — Practical Building Tasks

### Solution 3.1: Technical Blog Article Structure

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 3.1 - Blog Article</title>
</head>
<body>
    <h1>Understanding JavaScript Scope</h1>
    <p><small>Published by Bhavishya on August 28<sup>th</sup>, 2026</small></p>

    <hr>

    <h2>What is Block Scope?</h2>
    <p>
        In JavaScript, <strong>Block Scope</strong> means variables declared inside a <code>{}</code> block cannot be accessed from outside.
        Variables declared with <code>let</code> and <code>const</code> follow block scoping rules.
    </p>

<pre><code>if (true) {
    let message = "Hello Scope";
    console.log(message);
}</code></pre>
</body>
</html>
```

---

### Solution 3.2: Academic Paper Abstract Component

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 3.2 - Academic Abstract</title>
</head>
<body>
    <h1>Study on Water Purification (H<sub>2</sub>O)</h1>

    <p>
        <strong>Abstract:</strong> This research analyzes the catalytic breakdown of chemical compounds such as H<sub>2</sub>SO<sub>4</sub> under energy equation E = mc<sup>2</sup>.
        Experiments performed <i>in vitro</i> produced a high <mark>purity rating</mark>.
    </p>

    <hr>

    <p><small>&copy; 2026 International Journal of Science. ISSN 1234-5678.</small></p>
</body>
</html>
```

---

### Solution 3.3: Product Release Announcement Page

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 3.3 - Product Release</title>
</head>
<body>
    <h1>Announcing ProApp&trade; 2.0</h1>

    <p><strong>IMPORTANT NOTICE:</strong> Support for legacy version 1.0 will end on December 31<sup>st</sup>, 2026.</p>

    <p>New features include <mark>AI Auto-Completion</mark> and cloud synchronization.</p>

    <p>Price: &#8377; 2,999 / year</p>

    <hr>

    <p><small>&copy; 2026 ProApp&reg; Software Systems.</small></p>
</body>
</html>
```

---

### Solution 3.4: HTML & CSS Cheat Sheet Component

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 3.4 - HTML Tag Cheat Sheet</title>
</head>
<body>
    <h1>HTML Tag Cheat Sheet</h1>

    <p><code>&lt;h1&gt;</code> to <code>&lt;h6&gt;</code>: Heading elements for document structure.</p>
    <p><code>&lt;p&gt;</code>: Paragraph block for text content.</p>
    <p><code>&lt;br&gt;</code>: Void element for single line break.</p>
    <p><code>&lt;hr&gt;</code>: Void element for thematic section divider line.</p>
    <p><code>&lt;pre&gt;</code>: Preserves whitespace and line breaks.</p>
</body>
</html>
```

---

## 🔴 Level 4 Solution — Mini Real-World Challenge

### Solution 4.1: Documentation Page (`dev_tool_docs.html`)

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>StringUtil Documentation - Unit 02 Challenge</title>
</head>
<body>

    <!-- Main Title -->
    <h1>StringUtil&reg; Library Documentation</h1>
    <p><small>&copy; 2026 Bhavishya Open Source Labs. Released under MIT License.</small></p>

    <hr>

    <!-- Overview Section -->
    <h2>Overview</h2>
    <p>
        <strong>StringUtil</strong> is a lightweight JavaScript helper library designed for <em>fast text manipulation</em> and string sanitization.
        Latest stable release: <mark>v2.4.0</mark>.
    </p>

    <hr>

    <!-- Installation Section -->
    <h2>Installation &amp; Usage</h2>

    <h3>CLI Command</h3>
    <p>Install the library using terminal command: <code>npm install string-util-lib</code></p>

    <h3>Code Example</h3>
    <p>Import and call the <code>capitalize()</code> method as shown below:</p>

<pre><code>// Importing StringUtil library
const { capitalize } = require('string-util-lib');

const result = capitalize("hello full stack developer");
console.log(result); // Output: "Hello Full Stack Developer"</code></pre>

    <hr>

    <!-- Syntax & Entity Reference Section -->
    <h2>Syntax Reference &amp; Entity Guide</h2>
    <p>
        To output literal <code>&lt;script&gt;</code> tags in your application without executing JavaScript code, escape reserved characters using <code>&amp;lt;script&amp;gt;</code>.
    </p>
    <p>Special characters: &amp;lt; (Less Than), &amp;gt; (Greater Than), &amp;amp; (Ampersand).</p>

    <hr>

    <p><small>Documentation generated on August 28<sup>th</sup>, 2026. Price: &#8377; 0 (Free Community Edition).</small></p>

</body>
</html>
```

---

*All 15 practice solutions verified! Proceed to [mcqs.md](mcqs.md) for 20 self-assessment MCQs.* 🚀
