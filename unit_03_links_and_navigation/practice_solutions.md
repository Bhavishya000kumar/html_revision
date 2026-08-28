# Unit 03 — Practice Solutions

This document provides the complete, runnable HTML code, detailed explanations, and key learning points for all 15 practice questions in [practice.md](practice.md).

---

## 🟢 Level 1 Solutions — Basic Concept Questions

### Solution 1.1: Basic External Link

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.1 - External Link</title>
</head>
<body>
    <h1>React Documentation Link</h1>

    <p>
        Learn React from the official docs:
        <a href="https://react.dev" target="_blank" rel="noopener noreferrer" title="Official React Documentation Website">
            Official React Documentation
        </a>
    </p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- **`href="https://react.dev"`**: Absolute URL to external destination.
- **`target="_blank"`**: Opens destination page in a new tab.
- **`rel="noopener noreferrer"`**: Prevents tabnabbing security vulnerability.
- **`title="..."`**: Shows hover tooltip in browser.

---

### Solution 1.2: Relative Path in Same Folder

#### Complete HTML Code (`index.html`):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.2 - Same Folder Relative Link</title>
</head>
<body>
    <h1>Home Page</h1>

    <!-- Both implicit and explicit same-directory syntax -->
    <p><a href="about.html">About Us (Implicit relative path)</a></p>
    <p><a href="./about.html">About Us (Explicit dot-slash relative path)</a></p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- `about.html` and `./about.html` both resolve to the file located in the exact same directory as `index.html`.

---

### Solution 1.3: Jump to Section Anchor Link

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.3 - Jump Anchor Link</title>
</head>
<body>
    <h1>Page Navigation</h1>

    <!-- Link pointing to section id -->
    <p><a href="#faq">Jump to Frequently Asked Questions</a></p>

    <div style="height: 600px;">
        <p>(Scrollable page content...)</p>
    </div>

    <!-- Target Section with matching ID -->
    <section id="faq">
        <h2>Frequently Asked Questions</h2>
        <p>Q: What is HTML? A: HyperText Markup Language.</p>
    </section>
</body>
</html>
```

#### Explanation & Browser Behavior:
- The `#` prefix in `href="#faq"` signals an internal anchor target matching `id="faq"`.

---

### Solution 1.4: Telephone Dialing Link

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.4 - Phone Link</title>
</head>
<body>
    <h1>Customer Support</h1>

    <p>Need urgent assistance? Call us directly:</p>
    <p>
        <a href="tel:+919876543210" title="Call customer support dialer">Call Customer Care</a>
    </p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- `tel:` protocol opens phone dialer on mobile devices or VOIP apps (Skype/FaceTime) on desktop.

---

### Solution 1.5: Basic Email Link

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 1.5 - Email Link</title>
</head>
<body>
    <h1>Contact Us</h1>

    <p>Have questions? Send us an email:</p>
    <p>
        <a href="mailto:contact@company.com" title="Open email client">Email Us</a>
    </p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- `mailto:` opens the device's default mail client (Gmail, Outlook, Apple Mail) with the recipient pre-filled.

---

## 🟡 Level 2 Solutions — Concept-Based Questions & Debugging

### Solution 2.1: Relative Directory Traversal Upwards (`../`)

#### Complete HTML Code (`pages/contact.html`):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Contact Page</title>
</head>
<body>
    <h1>Contact Page</h1>

    <!-- Navigating UP one directory level to root index.html -->
    <p><a href="../index.html">&larr; Return to Home Page</a></p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- `../` tells the browser parser to exit `pages/` subfolder into parent `project/` directory to locate `index.html`.

---

### Solution 2.2: Tabnabbing Security Audit

#### Analysis of Vulnerability:
- Opening external links with `target="_blank"` without `rel="noopener noreferrer"` allows the newly opened tab to access `window.opener.location` on your origin page, exposing users to phishing tabnabbing attacks.

#### Corrected HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.2 - Security Fix</title>
</head>
<body>
    <p>
        <a href="https://external-partner.com" target="_blank" rel="noopener noreferrer">
            Partner Website
        </a>
    </p>
</body>
</html>
```

---

### Solution 2.3: Pre-filled Email Link Construction

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.3 - Pre-filled Email</title>
</head>
<body>
    <h1>Admissions Support</h1>

    <p>
        <a href="mailto:admissions@college.edu?subject=Course%20Inquiry&body=Hello,%20I%20want%20details%20about%20the%20Full%20Stack%20MERN%20course.">
            Send Course Inquiry Email
        </a>
    </p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- Uses URL query parameters `?subject=` and `&body=` with `%20` encoding for spaces.

---

### Solution 2.4: Accessibility Audit for Link Text

#### Analysis of Bad Practice:
- "Click here" text provides zero context when read out-of-context by screen reader link lists.
- Search engines cannot index destination page topic relevance from "click here".

#### Corrected HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.4 - Accessible Link</title>
</head>
<body>
    <p>Explore our complete <a href="pricing.html">Full Stack Development Course Pricing Plans</a>.</p>
</body>
</html>
```

---

### Solution 2.5: Forced File Download Link

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 2.5 - Forced Download</title>
</head>
<body>
    <h1>Course Syllabus</h1>

    <p>
        <a href="assets/brochure.pdf" download="Tech_Course_Brochure.pdf">
            Download Course Brochure (PDF)
        </a>
    </p>
</body>
</html>
```

#### Explanation & Browser Behavior:
- `download="Tech_Course_Brochure.pdf"` forces browser download action instead of opening PDF in browser viewer.

---

## 🟠 Level 3 Solutions — Practical Building Tasks

### Solution 3.1: Multi-Page Navigation Bar Component

#### Complete HTML Code (`index.html`):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 3.1 - Navigation Header</title>
</head>
<body>
    <header>
        <nav>
            <a href="index.html">Home</a> | 
            <a href="pages/about.html">About Us</a> | 
            <a href="pages/services.html">Services</a> | 
            <a href="pages/contact.html">Contact</a>
        </nav>
    </header>

    <h1>Welcome to Main Portal</h1>
</body>
</html>
```

---

### Solution 3.2: Single-Page Table of Contents Navigation

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 3.2 - Table of Contents</title>
</head>
<body>
    <h1 id="top">Documentation Index</h1>

    <nav>
        <ul>
            <li><a href="#intro">Introduction</a></li>
            <li><a href="#setup">Setup Guide</a></li>
            <li><a href="#examples">Code Examples</a></li>
        </ul>
    </nav>

    <hr>

    <section id="intro">
        <h2>Introduction</h2>
        <p>This library provides fast DOM utilities.</p>
        <p><a href="#top">&uarr; Back to Top</a></p>
    </section>

    <hr>

    <section id="setup">
        <h2>Setup Guide</h2>
        <p>Run npm install to configure dependencies.</p>
        <p><a href="#top">&uarr; Back to Top</a></p>
    </section>

    <hr>

    <section id="examples">
        <h2>Code Examples</h2>
        <p>View code blocks in Unit 02 notes.</p>
        <p><a href="#top">&uarr; Back to Top</a></p>
    </section>
</body>
</html>
```

---

### Solution 3.3: Developer Portfolio Header Links

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 3.3 - Portfolio Header</title>
</head>
<body>
    <h1>Bhavishya - Full Stack MERN Developer</h1>

    <p>
        <a href="tel:+919876543210">Call: +91 98765 43210</a> | 
        <a href="mailto:bhavishya@example.com">Email Me</a> | 
        <a href="https://github.com/Bhavishya" target="_blank" rel="noopener noreferrer">GitHub Profile</a> | 
        <a href="assets/resume.pdf" download="Bhavishya_Resume.pdf">Download Resume (PDF)</a>
    </p>
</body>
</html>
```

---

### Solution 3.4: Parent Folder Directory Traversal Component

#### Complete HTML Code (`pages/dashboard/user.html`):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Solution 3.4 - Two Level Directory Traversal</title>
</head>
<body>
    <h1>User Dashboard</h1>

    <!-- Navigating UP 2 directory levels (../../) into assets folder -->
    <p>
        <a href="../../assets/guide.pdf" download="User_Guide.pdf">
            Download User Guide PDF
        </a>
    </p>
</body>
</html>
```

---

## 🔴 Level 4 Solution — Mini Real-World Challenge

### Solution 4.1: Educational Portal (`portal_index.html`)

#### Complete HTML Code:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TechEdu Portal 2026 - Unit 03 Challenge</title>
</head>
<body>

    <!-- Main Header & Anchor -->
    <h1 id="top">TechEdu Portal 2026</h1>

    <!-- Top Navigation Header -->
    <nav>
        <p>
            <a href="#top">Home</a> | 
            <a href="#courses-section">Available Courses</a> | 
            <a href="https://developer.mozilla.org" target="_blank" rel="noopener noreferrer" title="External Web Docs">
                External Web Docs (New Tab)
            </a> | 
            <a href="#contact-section">Support &amp; Contact</a>
        </p>
    </nav>

    <hr>

    <!-- Courses Section -->
    <section id="courses-section">
        <h2>Available Courses</h2>
        <p>Explore our current web development curriculum:</p>
        <ul>
            <li><a href="pages/html_course.html">HTML5 &amp; Web Architecture Course</a></li>
            <li><a href="pages/js_course.html">JavaScript Deep Dive Masterclass</a></li>
        </ul>
        <p><a href="#top">&uarr; Return to Top</a></p>
    </section>

    <hr>

    <!-- Support & Contact Section -->
    <section id="contact-section">
        <h2>Support &amp; Contact Information</h2>
        <p>
            Need help? 
            <a href="mailto:support@techedu.com?subject=Portal%20Help&body=Hello%20Support%20Team,">
                Send Support Email (Pre-filled Subject)
            </a>
        </p>
        <p>
            Phone Helpline: 
            <a href="tel:+919876543210">+91 98765 43210</a>
        </p>
        <p>
            Offline Guide: 
            <a href="assets/portal_guide.pdf" download="TechEdu_Portal_Guide.pdf">
                Download Portal Guide (PDF)
            </a>
        </p>
        <p><a href="#top">&uarr; Return to Top</a></p>
    </section>

    <hr>

    <footer>
        <p><small>&copy; 2026 TechEdu Portal. All rights reserved.</small></p>
    </footer>

</body>
</html>
```

---

*All 15 practice solutions verified! Proceed to [mcqs.md](mcqs.md) for 20 self-assessment MCQs.* 🚀
