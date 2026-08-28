# Unit 03 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your knowledge of HTML hyperlinks, relative/absolute file paths, window targets, security best practices, internal page anchors, and special link protocols.

---

### Q1. Which HTML tag is used to create a hyperlink?

A. `<link>`  
B. `<a>`  
C. `<href>`  
D. `<url>`  

**Answer:** B

**Explanation:** The `<a>` (Anchor) tag is used to define hyperlinks in HTML. `<link>` is used in `<head>` to attach external stylesheets.

---

### Q2. What does the `href` attribute stand for in an anchor tag?

A. HTML Reference  
B. Hypertext Reference  
C. Header Resource Finder  
D. Home Reference File  

**Answer:** B

**Explanation:** `href` stands for Hypertext Reference, specifying the destination URL or file path.

---

### Q3. Which attribute value opens a link in a new browser tab?

A. `target="_self"`  
B. `target="_parent"`  
C. `target="_blank"`  
D. `target="_newtab"`  

**Answer:** C

**Explanation:** `target="_blank"` tells the browser to open the linked document in a new window or tab.

---

### Q4. What security attribute should ALWAYS be added when using `target="_blank"` on external links?

A. `rel="security"`  
B. `rel="noopener noreferrer"`  
C. `type="secure"`  
D. `secure="true"`  

**Answer:** B

**Explanation:** `rel="noopener noreferrer"` prevents the newly opened tab from exploiting the `window.opener` JavaScript object (Tabnabbing vulnerability).

---

### Q5. What relative path symbol represents moving UP one directory level to the parent folder?

A. `./`  
B. `../`  
C. `//`  
D. `~/`  

**Answer:** B

**Explanation:** `../` tells the browser parser to ascend one directory level up into the parent folder.

---

### Q6. If `index.html` and `about.html` are in the exact same directory, how should the relative link be written?

A. `<a href="../about.html">`  
B. `<a href="/about.html">`  
C. `<a href="about.html">` or `<a href="./about.html">`  
D. `<a href="same/about.html">`  

**Answer:** C

**Explanation:** `about.html` or `./about.html` references a file residing in the same current folder.

---

### Q7. How do you link to an internal page section with `id="contact-section"` on the same page?

A. `<a href="contact-section">`  
B. `<a href="?contact-section">`  
C. `<a href="#contact-section">`  
D. `<a href="@contact-section">`  

**Answer:** C

**Explanation:** Internal page anchors use the hash symbol `#` followed by the matching element `id`.

---

### Q8. Which protocol scheme opens the user's default email client when clicked?

A. `email:`  
B. `mailto:`  
C. `mail:`  
D. `sendmail:`  

**Answer:** B

**Explanation:** The `mailto:` protocol scheme launches the default email application with specified recipient addresses.

---

### Q9. Which protocol scheme triggers the phone dialer on mobile devices?

A. `phone:`  
B. `call:`  
C. `tel:`  
D. `dial:`  

**Answer:** C

**Explanation:** The `tel:` scheme opens the device phone dialer pre-filled with the specified phone number.

---

### Q10. What does the `download` attribute do when added to an `<a>` tag?

A. Downloads the webpage source code  
B. Prompts the browser to download the target file rather than navigating to or previewing it  
C. Installs an application  
D. Closes the browser tab  

**Answer:** B

**Explanation:** The `download` attribute forces a browser file save/download action for the target resource.

---

### Q11. Why is using "Click Here" as anchor text considered bad practice?

A. The browser throws a syntax error  
B. It hurts accessibility for screen readers and reduces SEO relevance for search engines  
C. It slows down page load speed  
D. It disables link clicks on mobile  

**Answer:** B

**Explanation:** Out-of-context link lists read by screen readers lack meaning with "Click Here". Search engines also require descriptive anchor text for page topic indexing.

---

### Q12. What does `href="#"` do when clicked on a web page?

A. Opens a blank page  
B. Scrolls the window back to the top of the current page  
C. Reloads the server  
D. Deletes browser cookies  

**Answer:** B

**Explanation:** An anchor link with `href="#"` targets the top of the current document viewport.

---

### Q13. How do you pre-fill a subject line in a `mailto:` link?

A. `<a href="mailto:info@site.com?subject=Help">`  
B. `<a href="mailto:info@site.com&subject=Help">`  
C. `<a href="mailto:info@site.com#subject=Help">`  
D. `<a href="mailto:info@site.com/subject=Help">`  

**Answer:** A

**Explanation:** URL parameters in `mailto:` begin with `?` (e.g. `mailto:info@site.com?subject=Help`).

---

### Q14. What is an Absolute URL?

A. A file path relative to current folder  
B. A complete web address specifying protocol, domain, and file path (e.g., `https://example.com/page.html`)  
C. A link inside a database  
D. A CSS selector  

**Answer:** B

**Explanation:** Absolute URLs contain full web addresses including protocol (`https://`) and domain name.

---

### Q15. In relative path notation, what does `../../page.html` mean?

A. Move down 2 subfolders  
B. Move UP 2 parent directory levels to locate `page.html`  
C. Duplicate `page.html` twice  
D. Search root domain  

**Answer:** B

**Explanation:** Each `../` ascends one directory level. `../../` ascends two levels up.

---

### Q16. Which `target` value is the default behavior if the `target` attribute is omitted?

A. `_blank`  
B. `_self`  
C. `_top`  
D. `_parent`  

**Answer:** B

**Explanation:** The default target behavior is `_self`, which opens the link in the current tab/window.

---

### Q17. How do you display a tooltip when a user hovers their mouse over a hyperlink?

A. Use the `hover` attribute  
B. Use the `tooltip` attribute  
C. Use the `title` attribute on the `<a>` tag  
D. Use the `alt` attribute  

**Answer:** C

**Explanation:** The global `title` attribute displays a native browser hover tooltip box.

---

### Q18. What protocol scheme triggers SMS text messaging on mobile devices?

A. `message:`  
B. `txt:`  
C. `sms:`  
D. `text:`  

**Answer:** C

**Explanation:** The `sms:` scheme opens the native text messaging app on mobile devices.

---

### Q19. What happens if an anchor tag `<a>` is left unclosed in HTML?

A. Only the first word becomes clickable  
B. All subsequent content on the page becomes part of the clickable hyperlink  
C. The browser displays a blank white screen  
D. The link automatically closes at line end  

**Answer:** B

**Explanation:** Because `<a>` is an inline paired element, omitting `</a>` causes the browser parser to treat all following elements as link content.

---

### Q20. What SEO attribute tells search engines NOT to pass ranking weight to an untrusted external link?

A. `rel="nofollow"`  
B. `rel="noindex"`  
C. `rel="hidden"`  
D. `rel="stop"`  

**Answer:** A

**Explanation:** `rel="nofollow"` signals to search engine crawlers that the link is not endorsed or should not pass PageRank.

---

*End of Unit 03 MCQs! All 20 questions completed.* 🚀
