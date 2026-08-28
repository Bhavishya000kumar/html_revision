# Unit 09 — Semantic HTML & Layout Structure (Master Study Notes)

Welcome to **Unit 09: Semantic HTML & Layout Structure**! Web development me "Div Soup" (har jagah sirf `<div>` use karna) ek sabse badi bad habit hai. Is unit me hum HTML5 **Semantic Tags** (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<time>`) ko detail me samjhenge.

---

## 1. Overview & Priority System

- ⭐⭐⭐ **Semantic HTML Foundations (`<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, `<footer>`)**: MUST KNOW (Core layout architecture).
- ⭐⭐⭐ **Section vs Article vs Div**: MUST KNOW (Top frontend placement interview question).
- ⭐⭐ **Time Element (`<time datetime="...">`)**: Important (Publish dates & machine-readable time).
- ⭐⭐ **Aside Element (`<aside>`)**: Important (Sidebars, related links, callout widgets).

---

## 2. What is Semantic HTML & Why Does It Matter? ⭐⭐⭐

### What is Semantic HTML?
**Semantic HTML** ka matlab hota hai aise tags use karna jo browser, screen reader, aur search engine ko **content ke meaning/role** ke baare me batate hain.
- **Non-Semantic**: `<div>`, `<span>` (Zero meaning/role about inner content).
- **Semantic**: `<header>`, `<nav>`, `<article>`, `<footer>` (Clear meaning/role).

```
   NON-SEMANTIC (Div Soup)               SEMANTIC HTML5
 ┌─────────────────────────┐        ┌─────────────────────────┐
 │   <div id="header">     │        │        <header>         │
 ├─────────────────────────┤        ├─────────────────────────┤
 │     <div id="nav">      │        │          <nav>          │
 ├─────────────────────────┤        ├─────────────────────────┤
 │    <div id="content">   │        │         <main>          │
 ├─────────────────────────┤        ├─────────────────────────┤
 │    <div id="footer">    │        │        <footer>         │
 └─────────────────────────┘        └─────────────────────────┘
```

### Why does Semantic HTML Matter?
1. **Search Engine Optimization (SEO)**: Google crawlers semantic hierarchy ke basis par page topic score determine karte hain.
2. **Web Accessibility (a11y)**: Screen readers landmarks (`<main>`, `<nav>`) detect karke visually impaired users ko direct navigation shortcuts dete hain.
3. **Clean Code & Maintenance**: Team developers code dekhte hi structure samajh jaate hain.

---

## 3. Core Semantic Layout Elements ⭐⭐⭐

### 1. `<header>`
Document ya section ka introductory header (Logo, title, search bar, navigation links).
```html
<header>
    <h1>TechPortal</h1>
    <nav>...</nav>
</header>
```

### 2. `<nav>`
Navigation links ka group (Main navbar, footer sitemap links).

### 3. `<main>`
Page ka **primary unique content container**.
> ⚠️ **CRITICAL RULE**: Ek page par **sirf EK `<main>` element** ho sakta hai. `<main>` kabhi bhi `<header>`, `<nav>`, ya `<footer>` ke andar nahi aana chahiye.

### 4. `<article>`
Independent, self-contained content unit jise standalone copy/share kiya ja sakta hai (Blog post, News article, Forum post, Product card).

```html
<article>
    <h2>Understanding React Hooks</h2>
    <p>React hooks state manage karte hain...</p>
</article>
```

### 5. `<section>`
Document ka thematic grouping / chapter (e.g. Hero Section, Features Section, Pricing Section). Generally contains a heading.

### 6. `<aside>`
Main content se tangentially related side content (Sidebar, related posts, ads, author bio widget).

### 7. `<footer>`
Document ya section ka footer area (Copyright, terms, social links).

### 8. `<time datetime="...">`
Human-readable date/time ko machine-readable ISO format me convert karta hai.

```html
<!-- Machine-readable datetime attribute helps search engines -->
<p>Published on <time datetime="2026-08-28T18:00">August 28th, 2026</time></p>
```

---

## 4. Concept Comparisons & Decision Tree 🎯

### `<article>` vs `<section>` vs `<div>` (CRITICAL INTERVIEW COMPARISON)

| Element | Semantic Meaning | Standalone Reusable? | Should Have Heading? | Best Use Case |
|---|---|---|---|---|
| **`<article>`** | Independent self-contained piece | ✅ YES | ✅ YES | Blog post, news item, tweet, product card |
| **`<section>`** | Thematic section of a larger page | ❌ NO | ✅ YES | Features section, pricing table, contact section |
| **`<div>`** | **NO Meaning** (Generic styling box) | ❌ NO | ❌ Not required | Wrapper for CSS Flexbox/Grid layout styling only |

---

## 5. MERN Stack & React Component Mapping ⚛️

React me Semantic HTML elements JSX Component Structure se 1-to-1 map hote hain:

```
HTML5 Semantic Layout Architecture         React JSX Component Mental Model
──────────────────────────────────         ────────────────────────────────
<header><nav>...</nav></header>    ───►    <NavbarComponent />
<main>                             ───►    <MainLayout>
   <section>                       ───►        <HeroSection />
   <article>                       ───►        <BlogPostCard />
</main>                            ───►    </MainLayout>
<footer>...</footer>               ───►    <FooterComponent />
```

---

## 6. Quick Revision Table ⚡

| Element | Role | Key Rule |
|---|---|---|
| `<header>` | Intro / Logo area | Can be page header or section header |
| `<nav>` | Navigation link block | Wrap key link groups |
| `<main>` | Unique primary page content | Exactly ONE per document |
| `<article>` | Independent standalone content | Self-contained (Blog post/Card) |
| `<section>` | Theme section grouping | Should contain a heading |
| `<aside>` | Sidebar / Tangential info | Related links, ads, author bio |
| `<footer>` | Page bottom summary | Copyright, legal links |
| `<time>` | Machine readable date | Use `datetime="YYYY-MM-DD"` |

---

## 7. Placement Must Know 🎯

1. Page me generic `<div>` soup ki bajae semantic landmarks use karne se Web Accessibility (a11y) score boost hota hai.
2. `<main>` element document me duplicate nahi ho sakta (Only 1 `<main>` per page).
3. `<article>` and `<section>` in standard HTML5 should almost always contain a Heading tag (`<h2>`-`<h6>`).
4. `<time datetime="2026-08-28">` search engines ko search results me exact published dates index karne me madad karta hai.
5. Interviewers frequently ask: *"When should you use `<article>` vs `<section>`?"*  
   **Answer**: Use `<article>` if the content can be taken out of the website and published independently elsewhere (e.g. blog post). Use `<section>` if it is a thematic chapter/part of the page.
