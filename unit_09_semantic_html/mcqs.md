# Unit 09 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your knowledge of HTML5 Semantic tags (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<time>`), accessibility landmarks, and SEO layout structure.

---

### Q1. What is the primary definition of Semantic HTML?

A. HTML code that contains JavaScript  
B. Using HTML elements that convey their structural meaning and role to both the browser and assistive technologies  
C. Using CSS for styling  
D. Writing code in uppercase  

**Answer:** B

**Explanation:** Semantic HTML uses tags whose names clearly describe their structural role and meaning in the document.

---

### Q2. How many `<main>` elements are permitted per HTML document?

A. Unlimited  
B. Exactly 1  
C. At least 5  
D. Zero  

**Answer:** B

**Explanation:** W3C specifications state that a document must contain only one `<main>` element representing unique primary content.

---

### Q3. Which semantic tag represents a self-contained, independent piece of content that could be republished on another site?

A. `<section>`  
B. `<div>`  
C. `<article>`  
D. `<aside>`  

**Answer:** C

**Explanation:** `<article>` represents independent, self-contained content (like blog posts, news stories, or forum posts).

---

### Q4. Which semantic element is designed for secondary, tangentially related content like sidebars or author bio widgets?

A. `<header>`  
B. `<aside>`  
C. `<nav>`  
D. `<main>`  

**Answer:** B

**Explanation:** `<aside>` represents content tangentially related to the main content, such as sidebars or callout boxes.

---

### Q5. What is the term for bad code practice where web pages rely almost exclusively on generic `<div>` tags?

A. Div Soup  
B. Tag Nesting  
C. DOM Explosion  
D. CSS Bloat  

**Answer:** A

**Explanation:** "Div Soup" refers to overusing non-semantic `<div>` elements instead of meaningful HTML5 structural tags.

---

### Q6. Which tag is used to wrap primary navigation link groups?

A. `<header>`  
B. `<links>`  
C. `<nav>`  
D. `<menu>`  

**Answer:** C

**Explanation:** `<nav>` represents a section of a page intended for primary navigation links.

---

### Q7. What attribute on the `<time>` tag provides machine-readable date/time strings for search crawlers?

A. `date`  
B. `value`  
C. `datetime`  
D. `time-str`  

**Answer:** C

**Explanation:** `<time datetime="2026-08-28">` provides standardized ISO date format for search engine indexation.

---

### Q8. What is the main difference between `<section>` and `<div>`?

A. `<div>` has SEO value, `<section>` does not  
B. `<section>` is a semantic thematic container typically containing a heading, whereas `<div>` has zero semantic meaning used solely for CSS styling  
C. `<section>` is inline  
D. `<div>` is deprecated  

**Answer:** B

**Explanation:** `<section>` denotes a meaningful thematic grouping of content, whereas `<div>` carries no semantic meaning.

---

### Q9. Can a webpage contain multiple `<header>` elements?

A. No, only 1 per document  
B. Yes, `<header>` can be used as a document header and as structural headers inside `<article>` or `<section>` tags  
C. Only if written in JavaScript  
D. Only inside `<footer>`  

**Answer:** B

**Explanation:** `<header>` can represent the overall page header or introductory headers for individual `<article>` and `<section>` components.

---

### Q10. How do screen readers benefit from HTML5 semantic elements like `<main>` and `<nav>`?

A. They change text color to black  
B. They treat them as landmark regions, allowing visually impaired users to jump directly to primary sections  
C. They turn off audio  
D. They hide images  

**Answer:** B

**Explanation:** Screen readers use semantic landmarks to provide shortcut hotkeys for jumping between major page regions.

---

### Q11. Which semantic tag represents the thematic footer of a document or section containing copyright and legal links?

A. `<bottom>`  
B. `<footer>`  
C. `<end>`  
D. `<summary>`  

**Answer:** B

**Explanation:** `<footer>` defines the footer section containing copyright notes, sitemaps, or contact info.

---

### Q12. What element should be used to wrap a blog post item in a news feed layout?

A. `<div>`  
B. `<article>`  
C. `<aside>`  
D. `<span>`  

**Answer:** B

**Explanation:** Each blog post or news feed item is a self-contained unit best represented by `<article>`.

---

### Q13. Which element should wrap a website's top navigation bar containing site logo and links?

A. `<header>` containing a `<nav>`  
B. `<main>` containing a `<footer>`  
C. `<aside>` containing a `<time>`  
D. `<div>` containing a `<section>`  

**Answer:** A

**Explanation:** The standard top navigation layout encapsulates `<nav>` within the site `<header>`.

---

### Q14. What semantic tag represents contact information for the author of a document or article?

A. `<contact>`  
B. `<address>`  
C. `<mail>`  
D. `<info>`  

**Answer:** B

**Explanation:** `<address>` is an HTML5 semantic element used to supply contact info for its nearest `<article>` or `<body>` ancestor.

---

### Q15. Why should a `<section>` generally contain a heading tag (`<h2>`-`<h6>`)?

A. HTML parser will crash without it  
B. Headings define the thematic topic outline of the section for accessibility and SEO  
C. CSS grid requires headings  
D. Headings change background color  

**Answer:** B

**Explanation:** A `<section>` represents a thematic group of content, so providing a heading clarifies the theme outline.

---

### Q16. How do HTML5 semantic elements map to React component architecture?

A. They do not map at all  
B. Semantic elements directly mirror top-level React JSX components (e.g. `<Navbar />` renders `<nav>`, `<Footer />` renders `<footer>`)  
C. React converts all tags into `<div>`  
D. React requires XML tags  

**Answer:** B

**Explanation:** React component trees assemble semantic HTML tags into modular UI components.

---

### Q17. What element is best suited for displaying a highlighted search result match?

A. `<mark>`  
B. `<strong>`  
C. `<em>`  
D. `<b>`  

**Answer:** A

**Explanation:** `<mark>` represents text marked or highlighted for reference or relevance in search results.

---

### Q18. Does `<aside>` always have to sit visually on the left or right side of a webpage?

A. Yes, visual position is fixed  
B. No, `<aside>` defines semantic relationship (tangential content), while visual position is controlled by CSS  
C. Only in Chrome  
D. It must sit in the footer  

**Answer:** B

**Explanation:** Semantic HTML defines meaning; visual layout positioning is handled independently by CSS.

---

### Q19. What machine-readable format is expected in `<time datetime="...">` attributes?

A. `MM/DD/YY`  
B. ISO 8601 standard format (e.g. `YYYY-MM-DD` or `YYYY-MM-DDTHH:MM`)  
C. Plain English text  
D. Roman numerals  

**Answer:** B

**Explanation:** ISO 8601 standard date/time formatting ensures machine parsability.

---

### Q20. In web placement interviews, what is the key distinction between `<article>` and `<section>`?

A. `<article>` is larger than `<section>`  
B. `<article>` is independent and reusable outside the page context; `<section>` is a thematic part of the page  
C. `<section>` is obsolete  
D. `<article>` cannot contain text  

**Answer:** B

**Explanation:** Content inside `<article>` stands alone independently; `<section>` groups related thematic content within a page context.

---

*End of Unit 09 MCQs! All 20 questions completed.* 🚀
