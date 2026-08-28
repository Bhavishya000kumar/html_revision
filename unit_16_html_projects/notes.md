# Unit 16 — Real-World HTML Capstone Projects Architecture (Master Study Notes)

Welcome to **Unit 16: Real-World HTML Capstone Projects Architecture**! Is final unit me hum HTML ke sabhi 15 units ke concepts (`<!DOCTYPE>`, Headings, Text Formatting, Links, Images, Lists, Tables, Advanced Forms, Semantic Tags, Global Attributes, Multimedia, a11y, and SEO) ko integrate karke **8 Capstone HTML Projects** ki architecture, file structure, aur building blueprints ko detail me samjhenge.

---

## 1. Overview & Priority System

- ⭐⭐⭐ **Project Architecture & Folder Conventions**: MUST KNOW (Professional project layout `/assets`, `/pages`, `index.html`).
- ⭐⭐⭐ **Multi-Page Website Routing in Pure HTML**: MUST KNOW (Connecting connected HTML pages via relative paths).
- ⭐⭐⭐ **Form Application Architecture**: MUST KNOW (Structuring complex user registration & multi-input forms).
- ⭐⭐⭐ **Semantic Layout Assembly**: MUST KNOW (Assembling `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`).

---

## 2. Professional HTML Project Directory Conventions ⭐⭐⭐

Real-world production repositories me files arbitrary tarike se nahi rakhi jaati, balki standard folder conventions follow ki jaati hain:

```
my-multi-page-website/
├── index.html                      <-- Home / Landing Page
├── README.md                       <-- Project Documentation
├── assets/                         <-- Static Assets Directory
│   ├── images/                     <-- Compressed WebP / PNG / SVG images
│   │   ├── logo.svg
│   │   └── hero-banner.webp
│   └── docs/                       <-- Downloadable PDFs / Files
│       └── syllabus.pdf
└── pages/                          <-- Secondary HTML Pages
    ├── about.html
    ├── courses.html
    └── contact.html
```

---

## 3. Blueprint & Architecture of the 8 Capstone Projects ⭐⭐⭐

### Project 1: 📄 Personal Developer Profile Card
- **Goal**: Basic HTML structure, Headings, Text Formatting, Images, Lists, and Social Links.
- **Key Tags Used**: `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`, `<h1>`, `<p>`, `<img>`, `<ul>`, `<li>`, `<a>`.
- **Architectural Flow**:
  - `<h1>`: Developer Name
  - `<img>`: Profile photo with `alt` and explicit `width`/`height`.
  - `<p>`: Bio description with `<strong>` and `<em>`.
  - `<ul>`: Tech Stack Skills list.
  - `<a>`: GitHub / LinkedIn social links (`target="_blank" rel="noopener"`).

---

### Project 2: 📝 Professional Resume Page
- **Goal**: Semantic text hierarchy, Data Tables, and Section Dividers.
- **Key Tags Used**: `<header>`, `<main>`, `<section>`, `<h2>`, `<table>`, `<thead>`, `<tbody>`, `<hr>`, `<small>`.
- **Architectural Flow**:
  - Header: Contact Info (`mailto:`, `tel:`).
  - Education Table (`<table>` with `<thead>` headers: Degree, College, Year, GPA).
  - Work Experience section with nested `<ul>` bullet accomplishments.
  - Footer with copyright.

---

### Project 3: 🏫 College / Student Information Portal
- **Goal**: Tabular grade records, cell spanning (`colspan`/`rowspan`), and media embeds.
- **Key Tags Used**: `<table>`, `<thead>`, `<tbody>`, `<tfoot>`, `colspan`, `rowspan`, `<iframe>` (Google Map embed).
- **Architectural Flow**:
  - Student Marks Table using `colspan` for Total Marks and `rowspan` for Department grouping.
  - Campus Map embedded via `<iframe src="https://maps.google.com..." sandbox title="Campus Location">`.

---

### Project 4: 📋 User Registration & Settings Form Application
- **Goal**: Comprehensive Form Controls, Fieldsets, Native HTML5 Validations, and File Uploads.
- **Key Tags Used**: `<form action="/api/register" method="POST" enctype="multipart/form-data">`, `<fieldset>`, `<legend>`, `<label for>`, `<input>` (text, password, email, date, file, checkbox, radio), `<select>`, `<textarea>`, `<button type="submit">`.
- **Architectural Flow**:
  - Fieldset 1: Account Credentials (Username, Email, Password with `minlength`).
  - Fieldset 2: Personal Info (DOB `type="date"`, Profile Photo `type="file" accept="image/*"`).
  - Fieldset 3: Preferences (Role selection dropdown `<select>`, Terms checkbox `required`).
  - Submit Button `<button type="submit">`.

---

### Project 5: 🛍️ E-Commerce Product Details Page
- **Goal**: Product Gallery, Pricing, Native Accordion Details, and Order Form.
- **Key Tags Used**: `<figure>`, `<figcaption>`, `<img>`, `<mark>`, `<sub>`, `<details>`, `<summary>`, `<form>`, `<input type="number">`.
- **Architectural Flow**:
  - Product Image Gallery inside `<figure>`.
  - Price display (`₹ 2,999` using `&#8377;` entity and `<mark>` badge).
  - Product Specifications Accordion using `<details>` and `<summary>`.
  - Quantity Selector `<input type="number" min="1" max="10" value="1">` and Add to Cart button.

---

### Project 6: 🍽️ Restaurant Menu & Order Form Page
- **Goal**: Tables, Description Lists (`<dl>`), Radio Choice Groups, and Special Instructions Textarea.
- **Key Tags Used**: `<dl>`, `<dt>`, `<dd>`, `<table>`, `<input type="radio">`, `<textarea>`.
- **Architectural Flow**:
  - Menu Items formatted using Description Lists (`<dt>` Dish Name, `<dd>` Ingredients & Price).
  - Special Offers Table.
  - Delivery Order Form with radio buttons grouped by `name="paymentMethod"`.

---

### Project 7: 💼 Developer Portfolio Page
- **Goal**: Complete Semantic Layout (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`), ARIA accessibility, and Project Cards.
- **Key Tags Used**: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<time>`, `aria-label`, `<a download>`.
- **Architectural Flow**:
  - Top Navigation Bar (`<nav>`).
  - Hero Section (`<section>`) with `<a download="Resume.pdf">` Resume Download Link.
  - Featured Projects grid using multiple `<article>` cards.
  - Author Bio Sidebar (`<aside>`).
  - Contact Form Footer (`<footer>`).

---

### Project 8: 🌐 Multi-Page Business Website
- **Goal**: Multi-file relative directory navigation, boilerplates, and connected sitemap architecture.
- **File Hierarchy**:
  - `index.html` (Home Landing Page)
  - `pages/about.html` (Company Profile)
  - `pages/services.html` (Service Cards)
  - `pages/contact.html` (Interactive Contact Form)
- **Architectural Flow**:
  - Every page shares identical `<header><nav>` navigation link structures (`<a href="../index.html">Home</a>`).
  - Every page links cleanly using relative directory paths (`../pages/about.html`).

---

## 4. Concept Comparisons & Best Practices

### HTML Component Assembly Checklist:

| Component Area | Recommended Semantic Tags | Key Attributes |
|---|---|---|
| **Site Navigation** | `<header>`, `<nav>`, `<ul>`, `<li>`, `<a>` | `aria-label="Main Navigation"` |
| **Hero Banner** | `<section>`, `<h1>`, `<p>`, `<img>` | `width`, `height`, `loading="eager"` |
| **Feature Cards** | `<section>`, `<article>`, `<h2>`, `<p>` | Semantic `<article>` wrapping |
| **Data Tables** | `<table>`, `<thead>`, `<tbody>`, `<tfoot>` | `<caption>`, `colspan`, `rowspan` |
| **Forms** | `<form>`, `<fieldset>`, `<label>`, `<input>`, `<button>` | `action`, `method`, `name`, `required` |
| **Footer** | `<footer>`, `<p>`, `<small>`, `<a>` | `&copy;` entity, social links |

---

## 5. MERN Stack Full Architecture Blueprint ⚛️

Web Application building blocks:

```
HTML Structure (Unit 01 - 16)
        ↓
CSS Layout & Styling
        ↓
JavaScript DOM & Event Listeners
        ↓
React JSX Component Modularization
        ↓
Node.js / Express REST API Backend
        ↓
MongoDB Database Storage
```

---

## 6. Quick Revision Table ⚡

| Project Type | Primary Focus | Crucial HTML Tags |
|---|---|---|
| Profile Card | Basic Text & Media | `<h1>`, `<p>`, `<img>`, `<ul>`, `<a>` |
| Resume | Data Tables & Sections | `<table>`, `<thead>`, `<hr>`, `<ul>` |
| Portal | Cell Spanning & Embeds | `colspan`, `rowspan`, `<iframe>` |
| Form App | User Inputs & Validations | `<form>`, `<input>`, `<select>`, `required` |
| Product Page | Media & Accordion | `<figure>`, `<details>`, `<summary>` |
| Portfolio | Complete Semantics | `<header>`, `<nav>`, `<main>`, `<article>`, `<aside>`, `<footer>` |
| Multi-Page Site | Directory Routing | `<a href="../pages/about.html">` |

---

## 7. Placement Must Know 🎯

1. Production HTML repositories organize files logically: `index.html` in root, secondary pages in `/pages/`, and media in `/assets/images/`.
2. Every HTML page in a multi-page site should share a consistent `<header><nav>` structure connecting pages via valid relative paths.
3. Forms that collect file uploads (`<input type="file">`) MUST specify `enctype="multipart/form-data"` on the `<form>` tag.
4. All images across portfolio and e-commerce projects MUST specify explicit `width` and `height` attributes to prevent Cumulative Layout Shift (CLS).
5. Using semantic containers (`<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>`) ensures 100% W3C standards compliance, optimal SEO indexation, and maximum screen reader accessibility (a11y).
