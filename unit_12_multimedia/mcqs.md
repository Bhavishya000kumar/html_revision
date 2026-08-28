# Unit 12 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your knowledge of HTML5 native video/audio, iframes, native accordions (`<details>`), `<dialog>`, and status widgets.

---

### Q1. Which element is used to specify multiple media source fallbacks inside `<video>` or `<audio>`?

A. `<media>`  
B. `<source>`  
C. `<url>`  
D. `<src>`  

**Answer:** B

**Explanation:** `<source>` allows specifying multiple file formats (e.g. MP4, WebM) so the browser can choose the first compatible format.

---

### Q2. What attribute renders native play, pause, volume, and fullscreen controls on `<video>`?

A. `buttons`  
B. `controls`  
C. `toolbar`  
D. `player`  

**Answer:** B

**Explanation:** The `controls` boolean attribute displays default browser media playback controls.

---

### Q3. Why do modern browsers block un-muted `autoplay` video execution on page load?

A. HTML5 specification bug  
B. User experience protection against intrusive loud background audio  
C. Video files are too large  
D. Operating system limits  

**Answer:** B

**Explanation:** Browsers enforce autoplay policies preventing videos from auto-playing with sound unless the `muted` attribute is also present.

---

### Q4. Which attribute specifies a preview thumbnail image displayed before a `<video>` starts playing?

A. `thumbnail`  
B. `preview`  
C. `poster`  
D. `cover`  

**Answer:** C

**Explanation:** `poster="image.jpg"` displays a preview frame image until the user plays the video.

---

### Q5. What element embeds an external HTML webpage or third-party widget (like Google Maps or YouTube) into current page?

A. `<embed-page>`  
B. `<iframe>`  
C. `<frame>`  
D. `<object>`  

**Answer:** B

**Explanation:** `<iframe>` (Inline Frame) embeds an external HTML document inside the current page.

---

### Q6. What security attribute on `<iframe>` restricts scripts, forms, and same-origin access for third-party embeds?

A. `security`  
B. `sandbox`  
C. `protect`  
D. `strict`  

**Answer:** B

**Explanation:** The `sandbox` attribute applies extra security restrictions to content embedded inside an `<iframe>`.

---

### Q7. Which pair of elements creates a native collapsible disclosure accordion without any JavaScript?

A. `<accordion>` and `<item>`  
B. `<details>` and `<summary>`  
C. `<collapse>` and `<header>`  
D. `<toggle>` and `<title>`  

**Answer:** B

**Explanation:** `<details>` wraps the collapsible section, and `<summary>` provides the visible clickable heading.

---

### Q8. What boolean attribute on `<details>` renders the accordion expanded (open) by default?

A. `active`  
B. `expanded`  
C. `open`  
D. `visible`  

**Answer:** C

**Explanation:** `<details open>` displays the inner content expanded upon page load.

---

### Q9. What HTML5 element defines a native browser popup modal dialog window?

A. `<modal>`  
B. `<popup>`  
C. `<dialog>`  
D. `<window>`  

**Answer:** C

**Explanation:** `<dialog>` represents a native modal or non-modal dialog box.

---

### Q10. What JavaScript method opens a `<dialog>` element as a backdrop-blocked modal window?

A. `dialog.open()`  
B. `dialog.showModal()`  
C. `dialog.popup()`  
D. `dialog.visible = true`  

**Answer:** B

**Explanation:** `element.showModal()` opens the `<dialog>` as a modal window with a backdrop layer.

---

### Q11. Which element represents the completion progress of a task (e.g., file upload percentage)?

A. `<meter>`  
B. `<progress>`  
C. `<bar>`  
D. `<loader>`  

**Answer:** B

**Explanation:** `<progress>` represents task completion progress (0% to 100%).

---

### Q12. Which element represents a scalar measurement within a known range (e.g., disk usage, battery level)?

A. `<progress>`  
B. `<meter>`  
C. `<level>`  
D. `<scale>`  

**Answer:** B

**Explanation:** `<meter>` represents a scalar fractional or gauge measurement within a known range.

---

### Q13. What attribute on `<iframe>` is MANDATORY for web accessibility compliance?

A. `title`  
B. `alt`  
C. `name`  
D. `id`  

**Answer:** A

**Explanation:** `<iframe>` elements must have a descriptive `title` attribute so screen readers can explain the embedded frame content.

---

### Q14. What does the `loop` attribute do on `<audio>` or `<video>` elements?

A. Plays video in reverse  
B. Automatically restarts media playback from the beginning when it reaches the end  
C. Slows down video speed  
D. Mutes audio  

**Answer:** B

**Explanation:** The boolean `loop` attribute causes media playback to restart automatically when finished.

---

### Q15. How do you close an open HTML `<dialog>` element programmatically in JavaScript?

A. `dialog.close()`  
B. `dialog.hide()`  
C. `dialog.destroy()`  
D. `dialog.remove()`  

**Answer:** A

**Explanation:** Calling `.close()` on a `<dialog>` DOM node closes the dialog window.

---

### Q16. Which attribute configures video preload behavior (e.g. loading metadata only)?

A. `download`  
B. `preload`  
C. `buffer`  
D. `strategy`  

**Answer:** B

**Explanation:** `preload="metadata"` instructs the browser to load only media duration and dimension metadata initially.

---

### Q17. What tag provides subtitle or caption tracks for `<video>` elements?

A. `<subtitles>`  
B. `<caption`  
C. `<track>`  
D. `<text>`  

**Answer:** C

**Explanation:** `<track>` specifies timed text tracks (subtitles, captions) for media elements.

---

### Q18. What happens if a browser does not support the `<video>` element?

A. Browser crashes  
B. Browser renders the fallback text/content placed inside the opening and closing `<video>` tags  
C. Screen turns black  
D. Code deletes itself  

**Answer:** B

**Explanation:** Fallback text inside `<video>Fallback text</video>` is displayed only in browsers lacking HTML5 video support.

---

### Q19. What attribute value on `<iframe>` defers loading until the iframe scrolls near the viewport?

A. `loading="lazy"`  
B. `defer="true"`  
C. `async="true"`  
D. `wait="scroll"`  

**Answer:** A

**Explanation:** `loading="lazy"` applies native lazy loading to `<iframe>` elements.

---

### Q20. In `<dialog>`, what CSS pseudo-element targets the darkened overlay background behind a modal opened with `.showModal()`?

A. `::modal-bg`  
B. `::backdrop`  
C. `::overlay`  
D. `::shadow`  

**Answer:** B

**Explanation:** `::backdrop` is the CSS pseudo-element used to style the background overlay behind an active `<dialog>`.

---

*End of Unit 12 MCQs! All 20 questions completed.* 🚀
