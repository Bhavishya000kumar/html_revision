# Unit 14 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your knowledge of connecting CSS/JS to HTML, `defer` vs `async` script loading timelines, DOM element selection, and React JSX translation rules.

---

### Q1. Which tag is used in `<head>` to connect an external CSS stylesheet to an HTML document?

A. `<style src="styles.css">`  
B. `<link rel="stylesheet" href="styles.css">`  
C. `<script href="styles.css">`  
D. `<css file="styles.css">`  

**Answer:** B

**Explanation:** `<link rel="stylesheet" href="...">` connects external CSS files to HTML documents.

---

### Q2. How does `<script src="app.js" defer>` behave during HTML page parsing?

A. It blocks HTML parsing while downloading  
B. It downloads in parallel with HTML parsing and executes ONLY after HTML parsing is complete  
C. It deletes the DOM  
D. It executes before the `<head>` tag opens  

**Answer:** B

**Explanation:** `defer` downloads the script asynchronously without pausing HTML parsing and executes after the DOM tree is ready.

---

### Q3. What is the execution behavior of `<script src="app.js" async>`?

A. Executes after page unload  
B. Downloads in parallel with HTML parsing and executes IMMEDIATELY when download finishes (pausing HTML parsing)  
C. Never executes  
D. Executes only on mobile  

**Answer:** B

**Explanation:** `async` scripts execute immediately upon finishing download, which can pause HTML parsing and execute out of document order.

---

### Q4. Why is placing un-deferred `<script>` tags in the `<head>` without `defer` or `async` bad practice?

A. The script will be deleted  
B. It causes render-blocking, pausing HTML parsing and delaying page display until the script downloads and runs  
C. Browsers ignore scripts in head  
D. It breaks CSS colors  

**Answer:** B

**Explanation:** Un-deferred scripts in `<head>` block the HTML parser, causing render-blocking delays.

---

### Q5. What HTML attribute is replaced by `className` in React JSX?

A. `id`  
B. `class`  
C. `style`  
D. `name`  

**Answer:** B

**Explanation:** In React JSX, `className` replaces `class` because `class` is a reserved keyword in JavaScript.

---

### Q6. What attribute replaces HTML `for` on `<label>` elements in React JSX?

A. `htmlFor`  
B. `labelFor`  
C. `forTarget`  
D. `targetFor`  

**Answer:** A

**Explanation:** `htmlFor` replaces `for` in JSX because `for` is a reserved JavaScript loop keyword.

---

### Q7. What is a strict syntax rule for void elements (like `<img>` or `<br>`) in React JSX compared to standard HTML5?

A. Void elements cannot be used in JSX  
B. All void elements MUST be explicitly self-closed (e.g. `<img />`, `<br />`)  
C. Void elements must be wrapped in `<div>`  
D. Void elements must contain text  

**Answer:** B

**Explanation:** Unlike standard HTML5 where closing slashes are optional on void tags, React JSX requires all elements to be explicitly closed (`<img />`).

---

### Q8. Which DOM method selects the first element matching a CSS selector (e.g. `#main-btn`)?

A. `document.getElementByIdName()`  
B. `document.querySelector("#main-btn")`  
C. `document.findCSS()`  
D. `document.getElement()`  

**Answer:** B

**Explanation:** `document.querySelector()` selects the first DOM element matching a CSS selector string.

---

### Q9. How are inline CSS styles written in React JSX?

A. `style="color: red;"`  
B. `style={{ color: "red" }}`  
C. `style="color = red"`  
D. `style={color: red}`  

**Answer:** B

**Explanation:** In JSX, inline styles are passed as JavaScript objects wrapped in double curly braces `style={{ color: "red" }}`.

---

### Q10. What JavaScript DOM property accesses the CSS class string of a selected element `el`?

A. `el.class`  
B. `el.className`  
C. `el.cssClass`  
D. `el.styleClass`  

**Answer:** B

**Explanation:** In DOM node objects, the HTML `class` attribute is exposed via the `className` property.

---

### Q11. Which script attribute guarantees that multiple scripts execute in the exact order they appear in the HTML document?

A. `async`  
B. `defer`  
C. `random`  
D. `order`  

**Answer:** B

**Explanation:** `defer` preserves script execution order based on document appearance, whereas `async` scripts execute in order of download completion.

---

### Q12. What event listener is attached to an HTML `<form>` DOM node to handle form submission in JavaScript?

A. `button.addEventListener("click")`  
B. `form.addEventListener("submit", handler)`  
C. `form.addEventListener("post")`  
D. `window.addEventListener("load")`  

**Answer:** B

**Explanation:** Form submissions trigger the `submit` event on the `<form>` DOM element.

---

### Q13. What is the CSS specificity hierarchy order from HIGHEST to LOWEST?

A. Tag Selector $\rightarrow$ Class Selector $\rightarrow$ ID Selector $\rightarrow$ Inline Style  
B. Inline Style $\rightarrow$ ID Selector (`#id`) $\rightarrow$ Class Selector (`.class`) $\rightarrow$ Tag Selector (`h1`)  
C. Class Selector $\rightarrow$ Inline Style $\rightarrow$ Tag Selector  
D. All selectors have equal specificity  

**Answer:** B

**Explanation:** Inline styles override ID selectors, which override class selectors, which override tag selectors.

---

### Q14. What event handler prop name is used in React JSX for button click events?

A. `onclick`  
B. `onClick`  
C. `on-click`  
D. `click`  

**Answer:** B

**Explanation:** React JSX uses CamelCase for event handler prop names (`onClick={handleClick}`).

---

### Q15. How does JavaScript attach a click event listener to a button element `btn`?

A. `btn.click = function`  
B. `btn.addEventListener("click", function)`  
C. `btn.attach("click")`  
D. `btn.listen("click")`  

**Answer:** B

**Explanation:** `element.addEventListener("click", callback)` is the standard W3C DOM method for attaching event listeners.

---

### Q16. Where should independent third-party scripts (like Google Analytics) typically use the `async` attribute?

A. On `<style>` tags  
B. On `<script src="..." async>` tags so they download and run independently without waiting for DOM completion  
C. On `<img>` tags  
D. On `<a>` tags  

**Answer:** B

**Explanation:** `async` is ideal for independent analytics scripts that do not depend on DOM completion or other scripts.

---

### Q17. What DOM method converts an HTML collection into a true JavaScript Array?

A. `Array.from(htmlCollection)`  
B. `htmlCollection.toArray()`  
C. `JSON.stringify()`  

**Answer:** A

**Explanation:** `Array.from()` creates a true JavaScript Array instance from an array-like HTMLCollection or NodeList.

---

### Q18. What happens if a JavaScript file attempts to select `document.querySelector("#btn")` before the HTML parser reaches line `<button id="btn">`?

A. It selects all buttons  
B. It returns `null` because the DOM node does not exist in memory yet  
C. It pauses HTML parsing  
D. It creates the button  

**Answer:** B

**Explanation:** If a script runs before the HTML parser encounters the element, `querySelector` returns `null`.

---

### Q19. In React JSX, what attribute replaces `readonly` for input fields?

A. `readonly`  
B. `readOnly`  
C. `noEdit`  

**Answer:** B

**Explanation:** JSX uses CamelCase property names (`readOnly`).

---

### Q20. What HTML element is created when a browser parses `<div class="card">`?

A. An `HTMLDivElement` object in the browser DOM tree  
B. A text file  
C. A C++ pointer  
D. A server process  

**Answer:** A

**Explanation:** The browser HTML parser instantiates an `HTMLDivElement` node object in the DOM tree memory.

---

*End of Unit 14 MCQs! All 20 questions completed.* 🚀
