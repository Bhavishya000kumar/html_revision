# Unit 11 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your understanding of HTML Global Attributes, Custom Data Attributes (`data-*`), `tabindex`, and HTML Attributes vs DOM Properties.

---

### Q1. What is the defining characteristic of HTML Global Attributes?

A. They can only be used on forms  
B. They are valid on every HTML element in the document  
C. They only work in Internet Explorer  
D. They require JavaScript to function  

**Answer:** B

**Explanation:** Global attributes (e.g. `id`, `class`, `title`, `hidden`) can be applied to all HTML elements.

---

### Q2. What is the specification rule regarding the `id` attribute on a webpage?

A. Multiple elements can share the same `id`  
B. An `id` value must be strictly unique across the entire HTML document  
C. An `id` can only contain numbers  
D. `id` is deprecated in HTML5  

**Answer:** B

**Explanation:** `id` values must be unique per document to prevent identifier collisions in CSS and JavaScript selection.

---

### Q3. How do multiple class names be specified on a single element's `class` attribute?

A. Separated by commas (`class="c1, c2"`)  
B. Separated by spaces (`class="c1 c2"`)  
C. Separated by semicolons (`class="c1; c2"`)  
D. Using multiple `class` attributes  

**Answer:** B

**Explanation:** Multiple classes are written inside a single `class` attribute separated by whitespace (e.g., `class="btn primary active"`).

---

### Q4. What prefix MUST be used to define custom data attributes in HTML5?

A. `custom-`  
B. `js-`  
C. `data-`  
D. `attr-`  

**Answer:** C

**Explanation:** Custom data attributes in HTML5 must begin with the `data-` prefix (e.g. `data-user-id`).

---

### Q5. How does JavaScript access custom `data-user-role="admin"` attribute values on a DOM element `el`?

A. `el.dataUserRole`  
B. `el.dataset.userRole`  
C. `el.getData("user-role")`  
D. `el.custom.userRole`  

**Answer:** B

**Explanation:** Custom data attributes map to the `dataset` property on DOM objects, converting hyphenated names into CamelCase (`data-user-role` $\rightarrow$ `dataset.userRole`).

---

### Q6. What does the boolean `hidden` attribute do when present on an HTML element?

A. Hides the element from viewport rendering  
B. Deletes the element from DOM  
C. Disables mouse clicks  
D. Changes text to transparent  

**Answer:** A

**Explanation:** The `hidden` attribute indicates that the element is not currently relevant and browser default styles hide it from rendering (`display: none`).

---

### Q7. What effect does `tabindex="0"` have on a `<div>` element?

A. It hides the div  
B. It makes the `<div>` keyboard focusable in sequential tab navigation order  
C. It moves the div to page top  
D. It disables keyboard input  

**Answer:** B

**Explanation:** `tabindex="0"` inserts non-interactive elements into the natural keyboard tab navigation flow.

---

### Q8. What effect does `tabindex="-1"` have on an element?

A. Makes it the first tab item  
B. Removes it from sequential keyboard tab order while allowing programmatic focus via JavaScript  
C. Disables the browser tab  
D. Throws a syntax error  

**Answer:** B

**Explanation:** `tabindex="-1"` removes an element from keyboard Tab navigation while permitting JS `element.focus()`.

---

### Q9. What is the fundamental difference between an HTML Attribute and a DOM Property?

A. Attributes are in JavaScript; Properties are in CSS  
B. HTML Attributes represent static initial values in markup source code; DOM Properties represent live dynamic state in browser memory  
C. They are identical  
D. Attributes cannot be read  

**Answer:** B

**Explanation:** HTML attributes initialize DOM properties in source code, but DOM properties reflect current live state (e.g., user-typed input text).

---

### Q10. What does `element.getAttribute("value")` return after a user types new text into `<input value="Default">`?

A. The new user-typed text  
B. The initial static HTML attribute value ("Default")  
C. `null`  
D. `undefined`  

**Answer:** B

**Explanation:** `getAttribute("value")` returns the static initial attribute string from markup, whereas `element.value` returns the live typed string.

---

### Q11. Which attribute displays a native browser hover tooltip when the mouse hovers over an element?

A. `alt`  
B. `tooltip`  
C. `title`  
D. `hover`  

**Answer:** C

**Explanation:** The global `title` attribute shows a native browser tooltip pop-up box.

---

### Q12. What JS method selects an element by its unique `id="submit-btn"`?

A. `document.querySelector(".submit-btn")`  
B. `document.getElementById("submit-btn")`  
C. `document.getElementsByName("submit-btn")`  

**Answer:** B

**Explanation:** `document.getElementById("submit-btn")` selects the element matching the specified ID.

---

### Q13. Which CSS selector targets elements with `data-status="active"`?

A. `[data-status="active"]`  
B. `.data-status-active`  
C. `#data-status=active`  
D. `data(status=active)`  

**Answer:** A

**Explanation:** CSS attribute selectors use square brackets `[attr="value"]`.

---

### Q14. What attribute name in React JSX replaces the HTML `class` attribute?

A. `class`  
B. `className`  
C. `classList`  
D. `cssClass`  

**Answer:** B

**Explanation:** In React JSX, `className` is used instead of `class` because `class` is a reserved keyword in JavaScript.

---

### Q15. Is `data-123="value"` a valid custom data attribute name?

A. Yes  
B. No, data attribute names after prefix must contain only lowercase letters/hyphens and no numbers immediately after dash  
C. Only in Chrome  
D. Custom attributes are forbidden  

**Answer:** A

**Explanation:** Custom data attribute names must start with `data-` and follow XML-compatible name rules.

---

### Q16. What is a Boolean Attribute in HTML?

A. An attribute requiring `true` or `false` string values  
B. An attribute whose presence represents `true` and absence represents `false` (e.g. `required`, `disabled`, `hidden`)  
C. An attribute used only in C++  
D. An attribute with numeric values  

**Answer:** B

**Explanation:** Boolean attributes (like `disabled` or `required`) are enabled simply by being present on an element tag.

---

### Q17. How is `data-user-first-name` accessed in JavaScript `dataset`?

A. `element.dataset.user-first-name`  
B. `element.dataset.userFirstName`  
C. `element.dataset.UserFirstName`  
D. `element.dataset["user-first-name"]`  

**Answer:** B

**Explanation:** Hyphenated data attributes convert to CamelCase properties on the `dataset` object.

---

### Q18. What global attribute specifies text direction (Left-to-Right or Right-to-Left)?

A. `lang`  
B. `dir`  
C. `align`  
D. `orient`  

**Answer:** B

**Explanation:** `dir="ltr"` (Left-to-Right) or `dir="rtl"` (Right-to-Left) sets text directionality.

---

### Q19. What global attribute enables inline editing of text content directly on a rendered webpage?

A. `editable="true"`  
B. `contenteditable="true"`  
C. `edit="yes"`  
D. `modify="true"`  

**Answer:** B

**Explanation:** `contenteditable="true"` allows users to edit an element's text content live in the browser viewport.

---

### Q20. What is the CSS ID selector symbol used to target `<div id="app">`?

A. `.app`  
B. `#app`  
C. `@app`  
D. `$app`  

**Answer:** B

**Explanation:** In CSS, `#` denotes an ID selector (`#app`).

---

*End of Unit 11 MCQs! All 20 questions completed.* 🚀
