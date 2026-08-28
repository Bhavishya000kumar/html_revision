# Unit 13 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your knowledge of Web Accessibility (a11y), WCAG principles, ARIA attributes, `<button>` vs `<div onClick>`, SEO meta tags, and Open Graph protocols.

---

### Q1. What does the acronym "a11y" stand for in web development?

A. HTML5 Year 11  
B. Accessibility (a + 11 letters + y)  
C. Algorithm 11 Y  
D. Array 11 Yield  

**Answer:** B

**Explanation:** "a11y" is a numeronym for Accessibility, representing the 11 letters between 'a' and 'y'.

---

### Q2. What attribute provides an accessible label for screen readers on icon-only buttons?

A. `alt`  
B. `title`  
C. `aria-label`  
D. `description`  

**Answer:** C

**Explanation:** `aria-label` supplies an accessible text string for interactive elements that lack visible text content.

---

### Q3. What attribute hides decorative visual icons from screen readers?

A. `aria-hidden="true"`  
B. `hidden="true"`  
C. `display="none"`  
D. `screen-reader="false"`  

**Answer:** A

**Explanation:** `aria-hidden="true"` removes an element from the accessibility tree so screen readers ignore decorative icons.

---

### Q4. What key advantage does `<button>` have over `<div onClick="...">` regarding accessibility?

A. `<button>` changes background color automatically  
B. `<button>` is natively keyboard focusable (`Tab`) and triggers on `Enter` and `Space` keys  
C. `<div onClick>` is deprecated  
D. `<button>` loads faster  

**Answer:** B

**Explanation:** Native `<button>` elements built into browsers handle keyboard focus and keypress activation out-of-the-box.

---

### Q5. What is the First Rule of ARIA in Web Accessibility guidelines?

A. Always use ARIA on every element  
B. Do not use ARIA if a native HTML element with the required semantics already exists  
C. ARIA replaces CSS  
D. ARIA requires JavaScript  

**Answer:** B

**Explanation:** The First Rule of ARIA states: *"If you can use a native HTML element instead of adding ARIA, do so."*

---

### Q6. Which meta tag controls responsive scaling on mobile device viewports?

A. `<meta name="mobile">`  
B. `<meta name="viewport" content="width=device-width, initial-scale=1.0">`  
C. `<meta name="screen">`  
D. `<meta name="responsive">`  

**Answer:** B

**Explanation:** The viewport meta tag instructs mobile browsers to render the page width matching the screen device width.

---

### Q7. Where is the snippet text displayed under a search result title in Google generated from?

A. `<meta name="keywords">`  
B. `<meta name="description">`  
C. `<title>`  
D. `<h1>`  

**Answer:** B

**Explanation:** Google frequently displays the `<meta name="description">` content as the search result summary snippet.

---

### Q8. What meta tag prefix protocol is used to control preview card titles, images, and descriptions shared on WhatsApp, Facebook, or LinkedIn?

A. `twitter:`  
B. `og:` (Open Graph)  
C. `seo:`  
D. `card:`  

**Answer:** B

**Explanation:** Open Graph (`og:title`, `og:image`, `og:description`) protocol tags format social media link sharing preview cards.

---

### Q9. What attribute indicates whether a collapsible dropdown menu is currently expanded or collapsed?

A. `aria-expanded`  
B. `aria-open`  
C. `aria-visible`  
D. `aria-active`  

**Answer:** A

**Explanation:** `aria-expanded="true"` or `false` informs assistive technology whether a collapsible section is open or closed.

---

### Q10. What tag prevents Google SEO search crawlers from penalizing a website for duplicate content across multiple URLs?

A. `<link rel="canonical" href="...">`  
B. `<meta name="duplicate">`  
C. `<meta name="copy">`  
D. `<link rel="same">`  

**Answer:** A

**Explanation:** Canonical link tags (`<link rel="canonical">`) specify the primary authoritative URL for indexing.

---

### Q11. Which attribute specifies explicit landmark roles like `role="navigation"` or `role="banner"`?

A. `aria-role`  
B. `role`  
C. `type`  
D. `landmark`  

**Answer:** B

**Explanation:** The `role` attribute specifies an element's landmark or widget role in the accessibility tree.

---

### Q12. What attribute on `<meta name="robots">` instructs search crawlers NOT to index a webpage?

A. `content="noindex"`  
B. `content="nofollow"`  
C. `content="hide"`  
D. `content="block"`  

**Answer:** A

**Explanation:** `content="noindex"` instructs search engine crawlers to exclude the document from search result indexes.

---

### Q13. What is the recommended character count range for SEO `<meta name="description">` tags?

A. 10–20 characters  
B. 150–160 characters  
C. 500–1000 characters  
D. Unlimited  

**Answer:** B

**Explanation:** Keeping meta descriptions between 150-160 characters ensures complete rendering without truncation in search engine snippets.

---

### Q14. What key triggers click events on native `<button>` elements when focused via keyboard navigation?

A. `Tab` key  
B. `Enter` and `Space` keys  
C. `Shift` key  
D. `Escape` key  

**Answer:** B

**Explanation:** Native `<button>` controls execute click handlers when either `Enter` or `Space` is pressed while focused.

---

### Q15. How do screen readers announce an element with `aria-label="Delete Account"` containing text "❌"?

A. "Cross icon"  
B. "Delete Account"  
C. "X"  
D. "Blank"  

**Answer:** B

**Explanation:** `aria-label` overrides inner element text, instructing the screen reader to vocalize "Delete Account".

---

### Q16. What is WCAG in web accessibility?

A. Web Code Acceleration Group  
B. Web Content Accessibility Guidelines (Global W3C standard)  
C. Web Compiler Algorithm Group  
D. Web Component Action Guide  

**Answer:** B

**Explanation:** WCAG (Web Content Accessibility Guidelines) provides international standards for web accessibility compliance.

---

### Q17. What tag connects a website's shortcut icon (Favicon) in the browser tab?

A. `<meta name="icon">`  
B. `<link rel="icon" href="favicon.ico">`  
C. `<img src="favicon.ico">`  
D. `<icon src="favicon.ico">`  

**Answer:** B

**Explanation:** `<link rel="icon" href="...">` connects the tab icon graphic in the document `<head>`.

---

### Q18. What ARIA attribute connects an input to its error message container ID?

A. `aria-errormessage` or `aria-describedby`  
B. `aria-fail`  
C. `aria-bad`  
D. `aria-alert`  

**Answer:** A

**Explanation:** `aria-describedby` or `aria-errormessage` links inputs to descriptive error text containers for screen readers.

---

### Q19. What open graph tag specifies the preview image URL shown on social media sharing cards?

A. `<meta property="og:picture">`  
B. `<meta property="og:image" content="...">`  
C. `<meta property="og:thumb">`  

**Answer:** B

**Explanation:** `og:image` specifies the image URL displayed on social link preview cards.

---

### Q20. In React Single Page Applications (SPAs), what library is commonly used to dynamically manage head metadata tags?

A. `react-router`  
B. `react-helmet` (or Next.js `<Head>`)  
C. `axios`  
D. `redux`  

**Answer:** B

**Explanation:** `react-helmet` (and Next.js `<Head>`) injects dynamic head title and meta tags into SPA pages.

---

*End of Unit 13 MCQs! All 20 questions completed.* 🚀
