# Unit 10 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your knowledge of Block vs Inline display mechanics, `<div>` vs `<span>`, layout skeletons, and CSS document flow.

---

### Q1. What is the default display behavior of a `<div>` element in browser stylesheets?

A. `inline`  
B. `block`  
C. `inline-block`  
D. `flex`  

**Answer:** B

**Explanation:** `<div>` is a generic block-level container (`display: block`).

---

### Q2. What is the default display behavior of a `<span>` element?

A. `block`  
B. `inline`  
C. `grid`  
D. `table`  

**Answer:** B

**Explanation:** `<span>` is a generic inline-level container (`display: inline`).

---

### Q3. How much width does a block-level element occupy by default?

A. Only the width of its text content  
B. 100% of its parent container's available width  
C. 50% width  
D. 0px width  

**Answer:** B

**Explanation:** Block elements stretch to fill 100% of their parent container's width.

---

### Q4. Which of the following describes line behavior for inline elements?

A. They always start on a new line  
B. They sit on the same line alongside adjacent inline content  
C. They clear floats  
D. They hide text  

**Answer:** B

**Explanation:** Inline elements stay on the same line as surrounding text and inline elements.

---

### Q5. What happens when you attempt to set explicit `width` and `height` properties in CSS on a pure inline element like `<span>`?

A. The element expands  
B. Browsers ignore width and height properties on pure inline elements  
C. Browser throws a syntax error  
D. The element turns red  

**Answer:** B

**Explanation:** Pure inline elements (`display: inline`) ignore `width` and `height` CSS properties.

---

### Q6. Which of the following is a Block-level element?

A. `<a>`  
B. `<strong>`  
C. `<h2>`  
D. `<span>`  

**Answer:** C

**Explanation:** Heading elements (`<h1>`-`<h6>`) are block-level elements.

---

### Q7. Which of the following is an Inline-level element?

A. `<p>`  
B. `<div>`  
C. `<em>`  
D. `<section>`  

**Answer:** C

**Explanation:** `<em>` (emphasis) is an inline-level text element.

---

### Q8. What element type is `<img>` categorized as by default in CSS layout flow?

A. Pure block  
B. Inline-block (sits inline but respects width/height dimensions)  
C. Fixed  
D. Absolute  

**Answer:** B

**Explanation:** `<img>` behaves as an inline-block element (replaces content inline while preserving width/height box dimensions).

---

### Q9. What is the primary difference between `<div>` and `<span>`?

A. `<div>` is semantic, `<span>` is not  
B. `<div>` is a generic block container; `<span>` is a generic inline text container  
C. `<span>` is deprecated  
D. `<div>` cannot hold text  

**Answer:** B

**Explanation:** `<div>` groups block-level sections; `<span>` groups inline words/phrases. Neither carries semantic meaning.

---

### Q10. Is placing a block-level `<div>` element inside a paragraph `<p>` tag valid HTML5 syntax?

A. Yes, perfectly valid  
B. No, W3C specifications state `<p>` tags cannot contain block-level elements  
C. Only if styled with CSS  
D. Only inside forms  

**Answer:** B

**Explanation:** HTML5 syntax rules prohibit nesting block-level elements inside paragraph `<p>` tags.

---

### Q11. Which element should be used to apply CSS styling to a single specific word inside a paragraph?

A. `<div>`  
B. `<span>`  
C. `<section>`  
D. `<main>`  

**Answer:** B

**Explanation:** `<span>` wraps inline words without disrupting the sentence line flow.

---

### Q12. What feature in React JSX allows grouping multiple elements without creating extra DOM `<div>` nodes?

A. `<React.Fragment>` (or `<>...</>`)  
B. `<React.Div>`  
C. `<React.Container>`  
D. `<React.Block>`  

**Answer:** A

**Explanation:** React Fragments group JSX children without adding extra wrapper nodes to the DOM tree.

---

### Q13. Which of the following lists contains ONLY block-level elements?

A. `<a>`, `<span>`, `<b>`  
B. `<p>`, `<div>`, `<section>`  
C. `<img>`, `<sub>`, `<sup>`  
D. `<label>`, `<code>`, `<mark>`  

**Answer:** B

**Explanation:** `<p>`, `<div>`, and `<section>` are all block-level elements.

---

### Q14. Which of the following lists contains ONLY inline-level elements?

A. `<h1>`, `<h2>`, `<h3>`  
B. `<strong>`, `<em>`, `<span>`  
C. `<ul>`, `<ol>`, `<li>`  
D. `<form>`, `<table>`, `<footer>`  

**Answer:** B

**Explanation:** `<strong>`, `<em>`, and `<span>` are all inline-level elements.

---

### Q15. Can an anchor tag `<a>` enclose block-level elements (like a `<div>` or `<h2>`) in modern HTML5?

A. No, invalid  
B. Yes, HTML5 explicitly permits `<a>` to wrap block-level elements to make entire cards clickable  
C. Only in Internet Explorer  
D. Only inside `<table>`  

**Answer:** B

**Explanation:** HTML5 updated the spec to allow `<a>` to wrap block-level containers to make entire UI cards clickable.

---

### Q16. What is the default margin behavior on `<div>` elements in browser stylesheets?

A. 20px top and bottom margin  
B. 0px default margin  
C. 50px left margin  
D. Auto margin  

**Answer:** B

**Explanation:** Unlike `<p>` or `<h1>` tags, generic `<div>` elements have 0px default margin/padding in User Agent stylesheets.

---

### Q17. How does a browser handle consecutive `<div>` elements written one after another in HTML?

A. It places them side by side horizontally  
B. It stacks them vertically on new lines  
C. It overlaps them  
D. It hides the second div  

**Answer:** B

**Explanation:** Because `<div>` is block-level, consecutive divs stack vertically down the page in normal document flow.

---

### Q18. What happens to consecutive `<span>` elements written one after another in HTML?

A. They stack vertically on new lines  
B. They sit side by side horizontally on the same line  
C. The second span is deleted  
D. They convert to buttons  

**Answer:** B

**Explanation:** Because `<span>` is inline-level, consecutive spans sit next to each other on the same line.

---

### Q19. What CSS property can transform an inline `<span>` into an element that accepts `width` and `height` dimensions while remaining on the same line?

A. `display: inline-block;`  
B. `display: flex;`  
C. `display: block;`  
D. `position: absolute;`  

**Answer:** A

**Explanation:** `display: inline-block;` combines inline line flow with block box-model dimension properties.

---

### Q20. In web layout design, what is the recommended approach for creating a multi-column page container?

A. Use multiple `<p>` tags  
B. Use a parent `<div>` or `<main>` container configured with CSS Flexbox or Grid  
C. Use 10 `<br>` tags  
D. Use `<title>` tags  

**Answer:** B

**Explanation:** Multi-column layouts should be constructed by wrapping items in structural containers (`<main>`, `<div>`, `<section>`) and styling them with CSS Flexbox or Grid.

---

*End of Unit 10 MCQs! All 20 questions completed.* 🚀
