# Unit 04 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your knowledge of HTML image embedding (`<img>`), accessibility (`alt`), Cumulative Layout Shift (CLS) prevention, semantic `<figure>` elements, image formats (SVG, WebP), and native lazy loading.

---

### Q1. What type of element is `<img>` in HTML5?

A. Container element  
B. Void (Self-closing) element  
C. Block-level container  
D. Head metadata element  

**Answer:** B

**Explanation:** `<img>` is a void element that cannot contain inner text or child elements, so it does not have a closing tag (`</img>`).

---

### Q2. Which attribute specifies the file location or URL of an image in HTML?

A. `href`  
B. `url`  
C. `src`  
D. `path`  

**Answer:** C

**Explanation:** `src` (Source) specifies the absolute URL or relative file path location of the image asset.

---

### Q3. What is the main purpose of the `alt` attribute on an `<img>` tag?

A. To add border styling  
B. To provide descriptive alternative text for screen readers, broken image fallbacks, and SEO  
C. To change image background color  
D. To auto-resize the image file size  

**Answer:** B

**Explanation:** `alt` (Alternative text) provides accessibility descriptions for screen readers, fallback text when network requests fail, and indexation data for search engines.

---

### Q4. What is Cumulative Layout Shift (CLS) in web development?

A. A server error code  
B. Unexpected layout jumps on a page caused when late-loading assets (like images) shift existing content  
C. Slow database query speed  
D. CSS color animation effect  

**Answer:** B

**Explanation:** CLS measures visual stability. When images without width/height attributes load late, they suddenly push text down, causing layout shifts.

---

### Q5. How do you prevent Cumulative Layout Shift (CLS) caused by HTML images?

A. By omitting `alt` attributes  
B. By adding explicit `width` and `height` pixel attributes to the `<img>` tag  
C. By using `target="_blank"`  
D. By wrapping images in `<p>` tags  

**Answer:** B

**Explanation:** Explicit `width` and `height` attributes allow the browser layout engine to calculate aspect ratios and reserve space before image files finish downloading.

---

### Q6. Which HTML5 elements are designed to semantically group an image with its text caption?

A. `<div>` and `<p>`  
B. `<figure>` and `<figcaption>`  
C. `<section>` and `<label>`  
D. `<header>` and `<caption>`  

**Answer:** B

**Explanation:** `<figure>` encapsulates self-contained media content, and `<figcaption>` defines its semantic caption.

---

### Q7. What should be set in the `alt` attribute for a purely decorative background pattern image?

A. `alt="decorative image"`  
B. `alt="picture"`  
C. `alt=""` (Empty string)  
D. Omit the `alt` attribute completely  

**Answer:** C

**Explanation:** An empty string `alt=""` explicitly instructs screen readers to skip announcing decorative graphics to visually impaired users.

---

### Q8. Which modern web image format developed by Google offers 25%–35% smaller file sizes than JPG/PNG while supporting transparency?

A. BMP  
B. WebP  
C. TIFF  
D. SVG  

**Answer:** B

**Explanation:** WebP is a modern high-compression image format supporting lossy, lossless, transparency, and animation with smaller file sizes.

---

### Q9. What makes Scalable Vector Graphics (SVG) unique compared to PNG or JPG?

A. SVG contains audio files  
B. SVG is XML-based vector code that scales infinitely without losing resolution or pixelating  
C. SVG only works on mobile screens  
D. SVG file size increases exponentially when zoomed  

**Answer:** B

**Explanation:** SVGs are vector graphics defined in XML code, making them resolution-independent and crisp at any scale or zoom level.

---

### Q10. What does the performance attribute `loading="lazy"` do?

A. Slows down browser execution  
B. Defers fetching an off-screen image until the user scrolls near its position in the viewport  
C. Compresses image quality automatically  
D. Automatically rotates images  

**Answer:** B

**Explanation:** `loading="lazy"` implements native lazy loading, deferring network fetch requests for off-screen images to improve initial page load speed.

---

### Q11. Which image format is best suited for complex realistic photographs with millions of colors?

A. SVG  
B. GIF  
C. JPG / JPEG  
D. ICO  

**Answer:** C

**Explanation:** JPG (JPEG) uses lossy compression optimized for complex real-world photographic imagery.

---

### Q12. Which image format supports transparent background channels (alpha channel) without vector scaling?

A. JPG  
B. PNG  
C. BMP  
D. MP4  

**Answer:** B

**Explanation:** PNG supports alpha channel transparency, making it ideal for UI icons, logos, and overlays.

---

### Q13. How do you turn an HTML image into a clickable link?

A. Add `href` directly to the `<img>` tag  
B. Wrap the `<img>` element inside an `<a>` anchor tag  
C. Add `click="true"` to `<img>`  
D. Use `<figcaption>` as a link  

**Answer:** B

**Explanation:** Wrapping `<img src="...">` inside `<a href="...">` makes the graphic an interactive hyperlink.

---

### Q14. What attribute displays a native hover tooltip pop-up when hovering a mouse over an image?

A. `alt`  
B. `title`  
C. `tooltip`  
D. `hover`  

**Answer:** B

**Explanation:** The global `title` attribute displays a native browser tooltip box when hovering over the image element.

---

### Q15. Where should `<figcaption>` be placed relative to its `<figure>` container?

A. Outside the `<html>` document  
B. Inside `<head>`  
C. As a direct child inside `<figure>`, either at the beginning or end of the figure container  
D. Inside `<title>`  

**Answer:** C

**Explanation:** `<figcaption>` must be a direct child inside `<figure>`, positioned before or after the figure content.

---

### Q16. Which value for the `loading` attribute should be used for critical above-the-fold Hero banner images?

A. `loading="lazy"`  
B. `loading="eager"`  
C. `loading="slow"`  
D. `loading="wait"`  

**Answer:** B

**Explanation:** `loading="eager"` (the default) fetches critical above-the-fold hero images immediately for fast First Contentful Paint.

---

### Q17. Why is `alt="image"` considered bad practice?

A. It causes browser errors  
B. It provides no meaningful context to screen reader users or search engines  
C. It forces the image to reload  
D. It disables CSS styling  

**Answer:** B

**Explanation:** Generic terms like "image" or "photo" fail accessibility guidelines because they fail to convey what the image depicts.

---

### Q18. Can a `<figure>` element contain code snippets (`<pre><code>`) instead of images?

A. No, `<figure>` is strictly for images  
B. Yes, `<figure>` is a semantic container for any self-contained content including charts, images, and code snippets  
C. Only if the code is written in C++  
D. Only inside the `<head>` tag  

**Answer:** B

**Explanation:** HTML5 defines `<figure>` for any self-contained unit of content (diagrams, photos, listings, code blocks) referenced with a caption.

---

### Q19. What happens if `src` points to a relative path `images/logo.png` that does not exist?

A. The browser crashes  
B. The browser displays a broken image icon and renders the `alt` text  
C. The page redirects to Google  
D. CSS is automatically disabled  

**Answer:** B

**Explanation:** When an image request returns a 404 error, the browser renders the broken image icon alongside the `alt` attribute text.

---

### Q20. What unit should be used inside HTML `width="600"` and `height="300"` attributes on an `<img>` tag?

A. `px` (e.g., `width="600px"`)  
B. Plain integers without unit names (e.g., `width="600"`)  
C. `em` (e.g., `width="60em"`)  
D. `%` (e.g., `width="100%"`)  

**Answer:** B

**Explanation:** HTML dimension attributes on `<img>` expect raw integer pixel values without suffix units like `px`.

---

*End of Unit 04 MCQs! All 20 questions completed.* 🚀
