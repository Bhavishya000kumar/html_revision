# Unit 05 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your understanding of HTML lists (`<ul>`, `<ol>`, `<dl>`), list attributes, nesting rules, accessibility, and DOM/React connections.

---

### Q1. What type of list should be used when the sequence of list items is NOT important?

A. `<ol>`  
B. `<dl>`  
C. `<ul>`  
D. `<list>`  

**Answer:** C

**Explanation:** `<ul>` (Unordered List) is designed for bulleted items where sequential order is irrelevant.

---

### Q2. Which tag defines an individual list item inside an unordered or ordered list?

A. `<item>`  
B. `<li>`  
C. `<point>`  
D. `<dt>`  

**Answer:** B

**Explanation:** `<li>` stands for List Item and must be a child of `<ul>` or `<ol>`.

---

### Q3. What is the default list marker visual style for an `<ul>` element in modern browsers?

A. Numbers (1, 2, 3)  
B. Filled disc bullet points (•)  
C. Letters (A, B, C)  
D. Roman numerals  

**Answer:** B

**Explanation:** Unordered lists default to rendering filled disc bullet icons.

---

### Q4. Which attribute of `<ol>` reverses the list numbering natively?

A. `reverse="true"`  
B. `dir="down"`  
C. `reversed`  
D. `order="desc"`  

**Answer:** C

**Explanation:** The boolean `reversed` attribute on `<ol>` counts list numbers downwards natively.

---

### Q5. What attribute changes the starting numerical value of an `<ol>` element?

A. `begin`  
B. `start`  
C. `offset`  
D. `from`  

**Answer:** B

**Explanation:** The `start` attribute (e.g. `<ol start="5">`) sets the numeric starting value of the list.

---

### Q6. Which tag pair represents a Description Term and Description Detail inside a `<dl>`?

A. `<li>` and `<item>`  
B. `<dt>` and `<dd>`  
C. `<key>` and `<value>`  
D. `<th>` and `<td>`  

**Answer:** B

**Explanation:** `<dl>` uses `<dt>` (Description Term) for keys and `<dd>` (Description Details) for values.

---

### Q7. What is the correct syntax rule for nesting an inner `<ul>` inside a parent `<ul>`?

A. Place the inner `<ul>` directly inside the parent `<ul>`  
B. Place the inner `<ul>` inside an `<li>` element of the parent list  
C. Use `<nested-ul>` tag  
D. Nesting lists is invalid in HTML5  

**Answer:** B

**Explanation:** W3C HTML5 standards require that nested child lists must sit inside an `<li>` element.

---

### Q8. Which `type` attribute value on `<ol>` produces uppercase Roman numerals (I, II, III)?

A. `type="1"`  
B. `type="a"`  
C. `type="I"`  
D. `type="r"`  

**Answer:** C

**Explanation:** `type="I"` formats ordered list numbers into uppercase Roman numerals.

---

### Q9. Why are navigation menus almost universally built using `<ul>` and `<li>` elements?

A. CSS only works on `<ul>`  
B. It provides screen readers with semantic structure announcing the item count to visually impaired users  
C. Browsers fail to render links without `<ul>`  
D. `<ul>` automatically centers text  

**Answer:** B

**Explanation:** Screen readers leverage `<ul><li>` semantics to inform users of the list length and navigation structure.

---

### Q10. What default browser CSS margin/padding behavior is applied to `<dd>` elements?

A. Right alignment  
B. Left indentation (margin-left)  
C. Underline styling  
D. Bold font weight  

**Answer:** B

**Explanation:** Browsers automatically apply a left margin (indentation) to `<dd>` elements to visually offset them from `<dt>`.

---

### Q11. Can a single `<dt>` term have multiple `<dd>` description elements inside a `<dl>`?

A. No, only 1-to-1 matching is allowed  
B. Yes, a term can have multiple description definitions  
C. Only if written in uppercase  
D. `<dl>` is deprecated  

**Answer:** B

**Explanation:** In HTML `<dl>`, a single term (`<dt>`) can be followed by multiple definitions (`<dd>`).

---

### Q12. What JavaScript DOM method selects all `<li>` elements inside an element with `id="nav-menu"`?

A. `document.getElementByName("li")`  
B. `document.querySelectorAll("#nav-menu li")`  
C. `document.selectItems("li")`  
D. `document.getLiElements()`  

**Answer:** B

**Explanation:** `querySelectorAll("#nav-menu li")` uses CSS selector syntax to retrieve a NodeList of list items.

---

### Q13. How does React JSX dynamically render an array of items into an HTML list?

A. Using `<for-each>` HTML tag  
B. Using the JavaScript `.map()` method returning `<li>` elements with unique `key` props  
C. Using `<ul>` loop attribute  
D. Using `document.write()`  

**Answer:** B

**Explanation:** React maps JavaScript data arrays into `<li>` JSX elements.

---

### Q14. What are the ONLY direct allowed child elements inside a `<ul>` or `<ol>` container?

A. `<div>` and `<p>`  
B. `<li>` elements (and `<script>` / `<template>`)  
C. `<a>` tags  
D. `<span>` elements  

**Answer:** B

**Explanation:** The W3C specification restricts direct structural children of `<ul>` and `<ol>` to `<li>` elements.

---

### Q15. What happens if you hardcode numbers inside `<li>` tags within an `<ol>` (e.g. `<ol><li>1. Step</li></ol>`)?

A. HTML syntax error  
B. Double numbering appears on screen (e.g. "1. 1. Step")  
C. The list turns into bullet points  
D. The text vanishes  

**Answer:** B

**Explanation:** Browsers automatically generate sequential list markers on `<ol><li>`, so hardcoding numbers creates duplicate text.

---

### Q16. Which list type is best suited for an online Glossary or Dictionary page?

A. `<ol>`  
B. `<ul>`  
C. `<dl>`  
D. `<menu>`  

**Answer:** C

**Explanation:** `<dl>` (Description List) is specifically designed for term-definition structures like glossaries.

---

### Q17. How do you remove bullet points from a `<ul>` using CSS?

A. `list-style-type: none;`  
B. `bullets: false;`  
C. `text-decoration: none;`  
D. `remove-dots: true;`  

**Answer:** A

**Explanation:** `list-style-type: none;` in CSS removes default bullet markers from `<ul>` or `<ol>`.

---

### Q18. What is the display level of an `<li>` element by default in CSS browser stylesheets?

A. `display: inline`  
B. `display: list-item`  
C. `display: flex`  
D. `display: grid`  

**Answer:** B

**Explanation:** Browsers style `<li>` elements with `display: list-item`, which behaves like block display with a marker box.

---

### Q19. What attribute value for `type` on an `<ol>` displays lowercase letters (a, b, c)?

A. `type="L"`  
B. `type="a"`  
C. `type="alpha"`  
D. `type="small"`  

**Answer:** B

**Explanation:** `type="a"` sets ordered list markers to lowercase Latin letters.

---

### Q20. Can an `<li>` element contain headings, paragraphs, images, and anchors?

A. No, `<li>` can only contain plain text  
B. Yes, `<li>` is a block container that can hold any flow content  
C. Only if wrapped in a `<div>`  
D. Only images are allowed  

**Answer:** B

**Explanation:** `<li>` list items accept any flow content, including text, headings, paragraphs, images, links, forms, and nested lists.

---

*End of Unit 05 MCQs! All 20 questions completed.* 🚀
