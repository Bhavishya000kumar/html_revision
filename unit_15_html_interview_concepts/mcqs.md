# Unit 15 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your knowledge of HTML placement interview concepts, browser rendering internals, Standards vs Quirks mode, Critical Rendering Path (CRP), and HTML security.

---

### Q1. What is the correct chronological sequence of the Browser Rendering Pipeline?

A. Paint $\rightarrow$ Layout $\rightarrow$ DOM $\rightarrow$ CSSOM  
B. HTML Parsing (DOM/CSSOM) $\rightarrow$ Render Tree $\rightarrow$ Layout (Reflow) $\rightarrow$ Painting  
C. Layout $\rightarrow$ Render Tree $\rightarrow$ Paint $\rightarrow$ DOM  
D. CSSOM $\rightarrow$ Paint $\rightarrow$ Reflow $\rightarrow$ DOM  

**Answer:** B

**Explanation:** Browsers construct DOM/CSSOM trees, combine them into a Render Tree, calculate layout geometry (Reflow), and paint pixels onto screen.

---

### Q2. What triggers Quirks Mode in modern web browsers?

A. Missing or invalid `<!DOCTYPE html>` declaration  
B. Using CSS flexbox  
C. Using JavaScript `fetch()`  
D. Missing `alt` tags  

**Answer:** A

**Explanation:** Omitting `<!DOCTYPE html>` causes browsers to render in legacy Quirks Mode for backward compatibility.

---

### Q3. What nodes are EXCLUDED from the browser Render Tree?

A. `<p>` elements  
B. Hidden elements (like `<head>`, `<script>`, and elements with `display: none`)  
C. `<h1>` tags  
D. `<img>` tags  

**Answer:** B

**Explanation:** The Render Tree contains only nodes that require visual rendering. `<head>`, `<script>`, and `display: none` elements are excluded.

---

### Q4. What is the browser process of recalculating the exact visual positions and dimensions of elements on screen?

A. Painting  
B. Reflow (Layout)  
C. Parsing  
D. Compiling  

**Answer:** B

**Explanation:** Reflow (Layout) calculates the geometry (size and position) of all nodes in the Render Tree.

---

### Q5. What is the primary difference between `display: none` and `visibility: hidden`?

A. `display: none` turns text red  
B. `display: none` removes the node from render layout (0px space); `visibility: hidden` hides text visually but preserves layout space  
C. `visibility: hidden` is faster  
D. They are identical  

**Answer:** B

**Explanation:** `display: none` releases layout space, whereas `visibility: hidden` retains reserved layout space.

---

### Q6. Which Core Web Vital metric measures unexpected layout shifts during page load?

A. LCP  
B. FID  
C. CLS (Cumulative Layout Shift)  
D. FCP  

**Answer:** C

**Explanation:** CLS measures visual layout stability during page loading.

---

### Q7. What attack occurs when a malicious user injects unescaped `<script>` tags into a web input field?

A. SQL Injection  
B. Cross-Site Scripting (XSS)  
C. Denial of Service (DoS)  
D. Buffer Overflow  

**Answer:** B

**Explanation:** XSS (Cross-Site Scripting) involves executing untrusted malicious scripts in a victim's browser via unescaped inputs.

---

### Q8. How does React JSX natively protect web applications against Cross-Site Scripting (XSS)?

A. By disabling JavaScript  
B. By automatically escaping all string values embedded in JSX variables before rendering  
C. By deleting input fields  
D. By requiring C++ compilation  

**Answer:** B

**Explanation:** React automatically escapes all string variables in JSX to prevent untrusted HTML/script execution.

---

### Q9. What performance optimization attribute preloads critical high-priority assets before the parser encounters them?

A. `<link rel="preload">`  
B. `<meta name="fast">`  
C. `<script speed="high">`  

**Answer:** A

**Explanation:** `<link rel="preload" href="..." as="...">` instructs the browser to fetch critical assets early in the Critical Rendering Path.

---

### Q10. What is the target ideal score threshold for Google's Cumulative Layout Shift (CLS) metric?

A. Under 0.1  
B. Under 10.0  
C. Exactly 5.0  
D. Over 100  

**Answer:** A

**Explanation:** Google recommends maintaining a CLS score of less than 0.1 for optimal user experience.

---

### Q11. Which browser operation is more computationally expensive?

A. Repaint (changing text color)  
B. Reflow (changing element dimensions/positions causing layout recalculation)  
C. Reading a variable  
D. Hovering mouse  

**Answer:** B

**Explanation:** Reflow requires geometry calculations across affected layout trees, making it much more expensive than Repaint.

---

### Q12. What does LCP stand for in Google Web Vitals?

A. Light Content Performance  
B. Largest Contentful Paint  
C. Local Code Parsing  
D. Layout Component Process  

**Answer:** B

**Explanation:** LCP (Largest Contentful Paint) measures how quickly the main content block loads on screen (ideal: < 2.5s).

---

### Q13. What is the legacy Internet Explorer Box Model issue present in Quirks Mode?

A. `width` includes content + padding + border  
B. `width` includes margin  
C. `width` is ignored  
D. Border is always red  

**Answer:** A

**Explanation:** The legacy IE box model calculated specified `width` to include inner padding and borders, unlike the W3C standard.

---

### Q14. What security feature on `<iframe>` prevents third-party embedded pages from running unauthorized scripts or navigating top frames?

A. `sandbox`  
B. `secure`  
C. `protect`  

**Answer:** A

**Explanation:** `sandbox` restricts scripts, forms, popups, and same-origin access for `<iframe>` embeds.

---

### Q15. What character string replaces `<` in HTML escaping to prevent XSS script tag injection?

A. `&lt;`  
B. `&lower;`  
C. `&bracket;`  

**Answer:** A

**Explanation:** `&lt;` escapes `<` into plain text entity format.

---

### Q16. Which CSS changes trigger ONLY a Repaint (and NOT a Reflow)?

A. Changing `width` from 100px to 200px  
B. Changing `color` or `background-color`  
C. Changing `font-size`  
D. Changing `margin`  

**Answer:** B

**Explanation:** Color changes alter pixel appearances (Repaint) without altering structural layout dimensions (Reflow).

---

### Q17. What HTTP header or meta tag specifies Content Security Policy rules restricting inline scripts?

A. Content-Security-Policy (CSP)  
B. X-Frame-Options  
C. CORS  

**Answer:** A

**Explanation:** Content Security Policy (CSP) restricts allowed script execution sources to prevent XSS attacks.

---

### Q18. What is the purpose of `rel="noopener"` on external links?

A. Improves font size  
B. Prevents newly opened tabs from accessing `window.opener` on the originating page (tabnabbing protection)  
C. Speeds up internet connection  

**Answer:** B

**Explanation:** `rel="noopener"` severs the `window.opener` JavaScript reference link for newly opened tabs.

---

### Q19. How does browser caching benefit Critical Rendering Path performance?

A. By eliminating network fetch latency for previously downloaded static assets  
B. By shortening JavaScript code  
C. By deleting images  

**Answer:** A

**Explanation:** Cached static assets load instantly from local memory/disk cache without waiting for network HTTP roundtrips.

---

### Q20. In placement interviews, what is the ultimate goal of optimizing the Critical Rendering Path (CRP)?

A. To reduce the time it takes for the browser to render the First Contentful Paint (FCP) and display meaningful content to the user  
B. To write less HTML  
C. To replace CSS with JS  

**Answer:** A

**Explanation:** CRP optimization aims to minimize initial load blocking, enabling fast First Contentful Paint and interactive page rendering.

---

*End of Unit 15 MCQs! All 20 questions completed.* 🚀
