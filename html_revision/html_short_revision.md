# 🚀 HTML Short Revision Notes (Master Exam & Interview Guide)

This document contains high-density, topic-by-topic HTML revision notes covering **Units 01 through 16**. It is designed for fast 15-minute review before technical placement interviews and online coding assessments.

---

## 📌 1. Master Concept Comparison Tables

### Comparison 1: HTML vs CSS vs JavaScript ⭐⭐⭐
| Technology | Primary Role | Real-Life Analogy (Human Body) | Real-Life Analogy (Car) |
|---|---|---|---|
| **HTML** | Structure & Content | **Skeleton (Haddiyan)** | Metal Chassis Frame |
| **CSS** | Styling & Appearance | **Skin, Hair, Clothes** | Car Paint & Leather Seats |
| **JavaScript** | Behavior & Logic | **Brain, Muscles, Action** | Engine & Steering System |

### Comparison 2: Tag vs Element ⭐⭐⭐
| Feature | HTML Tag | HTML Element |
|---|---|---|
| **Definition** | Markup code enclosed in `< >` | Complete unit: Opening Tag + Content + Closing Tag |
| **Example** | `<h1>` or `</h1>` | `<h1>Welcome to HTML Course</h1>` |

### Comparison 3: Block vs Inline vs Inline-Block ⭐⭐⭐
| Display Level | New Line? | Width Occupied | Accepts Width/Height CSS? | Examples |
|---|---|---|---|---|
| **Block** | ✅ Yes (Starts on new line) | 100% of parent width | ✅ Yes | `<div>`, `<p>`, `<h1>`, `<ul>`, `<form>`, `<section>` |
| **Inline** | ❌ No (Sits on same line) | Content width only | ❌ No (Ignored) | `<span>`, `<a>`, `<strong>`, `<em>`, `<code>`, `<mark>` |
| **Inline-Block** | ❌ No (Sits on same line) | Content width default | ✅ Yes (Custom sizing) | `<img>`, `<input>`, `<button>`, `<select>`, `<textarea>` |

### Comparison 4: `<div>` vs `<span>` ⭐⭐⭐
| Container | Default Display | Semantic Meaning | Primary Purpose |
|---|---|---|---|
| **`<div>`** | `block` | **None** (Generic Block Container) | Wrapping layout sections for Flexbox/Grid |
| **`<span>`** | `inline` | **None** (Generic Inline Container) | Styling individual words inside a paragraph |

### Comparison 5: `id` vs `class` Attributes ⭐⭐⭐
| Property | `id` Attribute | `class` Attribute |
|---|---|---|
| **Uniqueness** | **Must be strictly UNIQUE** per page | Reusable across multiple elements |
| **Multiple Values?** | ❌ No | ✅ Yes (`class="btn active primary"`) |
| **CSS Selector** | `#my-id` | `.my-class` |
| **JS Selection** | `document.getElementById("id")` | `document.getElementsByClassName("class")` |

### Comparison 6: `<ul>` vs `<ol>` vs `<dl>` ⭐⭐
| List Type | Full Name | Marker Icon | Main Child Tags | Primary Use Case |
|---|---|---|---|---|
| **`<ul>`** | Unordered List | Bullet dots (•) | `<li>` | Navbars, bullet features |
| **`<ol>`** | Ordered List | Numbers (1, 2, 3...) | `<li>` | Step-by-step tutorials |
| **`<dl>`** | Description List | No marker (Indented) | `<dt>`, `<dd>` | Glossaries, FAQs, Metadata |

### Comparison 7: `<th>` vs `<td>` ⭐⭐
| Cell Type | Name | Default Font Weight | Alignment | Semantic Role |
|---|---|---|---|---|
| **`<th>`** | Table Header | **Bold** | **Center** | Column or Row header label |
| **`<td>`** | Table Data | Normal | Left | Data cell value |

### Comparison 8: `GET` vs `POST` Submission Methods ⭐⭐⭐
| Feature | `GET` Method | `POST` Method |
|---|---|---|
| **Data Payload Location** | Appended to URL query string (`?key=val`) | Hidden inside HTTP Request Body |
| **Security** | ❌ Insecure (Exposes passwords in URL) | ✅ Secure for sensitive credentials |
| **Data Size Limit** | Limited (~2048 chars) | Unlimited |
| **Bookmarkable?** | Yes | No |

### Comparison 9: Checkbox vs Radio Buttons ⭐⭐
| Input Type | Selection Mode | Grouping Requirement | Visual Shape |
|---|---|---|---|
| `type="checkbox"` | Multi-choice independent selection | Independent `name` attributes | Square box |
| `type="radio"` | Single-choice exclusive selection | Must share **exact SAME `name` attribute** | Circular dot |

### Comparison 10: `required` vs `readonly` vs `disabled` ⭐⭐⭐
| State Attribute | User Can Edit? | Submitted to Server Payload? | Focusable via Tab? |
|---|---|---|---|
| `required` | ✅ Yes | ✅ Yes (If non-empty) | ✅ Yes |
| `readonly` | ❌ No | ✅ **YES (Included in POST data)** | ✅ Yes |
| `disabled` | ❌ No | ❌ **NO (Excluded from POST data)** | ❌ No |

### Comparison 11: `<article>` vs `<section>` vs `<div>` ⭐⭐⭐
| Element | Semantic Meaning | Standalone Reusable Elsewhere? | Typical Best Use Case |
|---|---|---|---|
| **`<article>`** | Independent self-contained unit | ✅ YES | Blog post, news item, tweet card |
| **`<section>`** | Thematic chapter of a page | ❌ NO | Features section, pricing section |
| **`<div>`** | **NO Meaning** | ❌ NO | Wrapper for CSS layout styling only |

### Comparison 12: Semantic vs Non-Semantic HTML ⭐⭐⭐
| Approach | Syntax Example | SEO Value | Screen Reader Accessibility |
|---|---|---|---|
| **Non-Semantic** | `<div id="nav">` | ❌ Poor | ❌ Cannot identify landmarks |
| **Semantic** | `<nav>` | 🔥 Excellent | ✅ High (Landmark shortcut keys) |

### Comparison 13: `<button>` vs `<input type="submit">` ⭐⭐
| Button Type | Can Enclose Icons / HTML Markup? | Styling Flexibility |
|---|---|---|
| **`<button type="submit">`** | ✅ YES (`<button><svg> Login</button>`) | High |
| **`<input type="submit">`** | ❌ NO (Only plain text in `value`) | Low |

### Comparison 14: HTML Attribute vs DOM Property ⭐⭐⭐
| Aspect | HTML Attribute | DOM Property |
|---|---|---|
| **Location** | Written in static HTML markup | Live object property in browser memory |
| **Value State** | Initial default value | Current live state (updates when user types) |
| **Access Method** | `el.getAttribute("value")` | `el.value` |

### Comparison 15: Standard HTML vs React JSX Syntax ⭐⭐⭐
| Standard HTML | React JSX Equivalent | Reason |
|---|---|---|
| `class="card"` | `className="card"` | `class` is a reserved JavaScript keyword |
| `for="email"` | `htmlFor="email"` | `for` is a reserved JS loop keyword |
| `<img>`, `<br>` | `<img />`, `<br />` | **All JSX elements MUST be explicitly closed** |
| `onclick="fn()"` | `onClick={fn}` | CamelCase props accepting function references |

### Comparison 16: `<script>` vs `<script async>` vs `<script defer>` ⭐⭐⭐
| Script Attribute | Download Timeline | Execution Timeline | Render Blocking? |
|---|---|---|---|
| **Standard `<script>`** | Synchronous | Immediately upon download | ❌ **YES (Pauses HTML Parser)** |
| **`<script async>`** | Asynchronous | Immediately upon download completion | ❌ **YES (Pauses HTML to run)** |
| **`<script defer>`** | Asynchronous | **ONLY after HTML parsing finishes** | ✅ **NO (Non-blocking)** |

### Comparison 17: Accessibility (a11y) vs SEO ⭐⭐
| Area | Target Audience | Primary HTML Strategy |
|---|---|---|
| **Web Accessibility (a11y)** | Human users with disabilities / Screen readers | Semantic tags, `alt` text, ARIA attributes |
| **Search Engine Optimization (SEO)** | Search engine crawlers (Googlebot) | Meta tags, heading hierarchy, semantic structure |

### Comparison 18: `<button>` vs `<div onClick>` (Accessibility Debate) ⭐⭐⭐
| Clickable Element | Natively Focusable via `Tab`? | Triggers on `Enter` & `Space` keys? | Screen Reader Announcement |
|---|---|---|---|
| **`<button>`** | ✅ YES | ✅ YES | *"Button"* |
| **`<div onClick>`** | ❌ NO (Requires `tabindex="0"`) | ❌ NO (Requires manual JS key handlers) | *"Group"* (Unclear role) |

---

## 📌 2. Topic-by-Topic Revision Guide

### 1. HTML Foundations & Skeleton (Unit 01) ⭐⭐⭐
- **`<!DOCTYPE html>`**: Informs the browser to render the page in modern W3C **Standards Mode** (preventing legacy Quirks Mode).
- **`<html>`**: Root element. Always set language attribute: `<html lang="en">`.
- **`<head>`**: Contains metadata (`charset`, `viewport`, `title`), scripts, and styles. NOT rendered in viewport.
- **`<body>`**: Contains 100% of visible page elements.
- **Metadata**: `<meta charset="UTF-8">` supports all Unicode characters/emojis; `<meta name="viewport" content="width=device-width, initial-scale=1.0">` ensures mobile scaling.
- **Void Elements**: Elements without closing tags or inner content (`<img>`, `<br>`, `<hr>`, `<meta>`, `<input>`, `<link>`).

### 2. Text Formatting & Structure (Unit 02) ⭐⭐
- **Headings (`<h1>`-`<h6>`)**: Use logically. Only **ONE `<h1>` per page** for SEO. Never skip heading levels (`H1` $\rightarrow$ `H3`).
- **Formatting Tags**:
  - `<strong>` (Semantic high importance) vs `<b>` (Visual bold only).
  - `<em>` (Semantic stress emphasis) vs `<i>` (Alternate tone / foreign words).
  - `<sub>` (Subscript: $H_2O$) and `<sup>` (Superscript: $a^2$).
  - `<mark>` (Highlighted text match) and `<small>` (Fine print/copyright).
- **Preformatted Code**: `<pre>` preserves whitespace and line breaks; `<code>` formats monospace code text. Use `<pre><code>...</code></pre>` for code blocks.
- **HTML Entities**: Reserved characters must be escaped: `<` = `&lt;`, `>` = `&gt;`, `&` = `&amp;`, `"` = `&quot;`, `©` = `&copy;`, `₹` = `&#8377;`.

### 3. Links & Navigation (Unit 03) ⭐⭐⭐
- **Anchor Tag (`<a>`)**: Inline link element.
- **Absolute URLs**: Full web address (`https://google.com`).
- **Relative Paths**: Local directory navigation (`./page.html`, `pages/about.html`, `../index.html`). `../` moves UP one folder.
- **Target & Security**: `target="_blank"` opens a new tab. **Security Rule**: ALWAYS add `rel="noopener noreferrer"` to prevent Tabnabbing phishing attacks.
- **Page Anchors**: Jump to specific section using `#id` (e.g. `<a href="#contact">` $\rightarrow$ `<section id="contact">`).
- **Special Schemes**: `mailto:user@site.com` (Email), `tel:+919876543210` (Phone dialer), `sms:+919876543210` (SMS), `download="name.pdf"` (Forces file download).

### 4. Images & Media Basics (Unit 04) ⭐⭐⭐
- **Image Tag (`<img>`)**: Void element.
- **`alt` Attribute**: Essential for Screen Readers (a11y), broken image fallback, and Google Image Search (SEO). Use `alt=""` for decorative graphics.
- **Cumulative Layout Shift (CLS) Prevention**: ALWAYS set explicit `width` and `height` attributes (without `px`) on `<img>` tags to reserve aspect ratio layout space before loading.
- **Semantic Figure**: `<figure>` encapsulates image/media; `<figcaption>` provides semantic caption text.
- **Performance**: `loading="lazy"` defers off-screen image loading until user scrolls near.
- **Image Formats**: **WebP** (modern high-compression web format), **SVG** (infinite resolution vector code), **PNG** (transparency), **JPG** (realistic photos).

### 5. Lists (Unit 05) ⭐⭐
- **`<ul>`**: Unordered list (bullet dots). Used for navbars and link groups.
- **`<ol>`**: Ordered list (numbers/letters). Attributes: `type` ("1","A","a","I"), `start="5"`, `reversed` (counts down).
- **`<dl>`**: Description List. `<dt>` = Term (Key), `<dd>` = Description (Value). Used for glossaries, metadata sidebars, FAQs.
- **Nesting Rule**: Inner `<ul>` or `<ol>` MUST be placed directly inside an `<li>` element.

### 6. Tables (Unit 06) ⭐⭐
- **Core Elements**: `<table>`, `<tr>` (Row), `<th>` (Header cell - bold/centered), `<td>` (Data cell).
- **Semantic Sections**: `<thead>` (Header group), `<tbody>` (Body rows), `<tfoot>` (Summary/Totals), `<caption>` (Table title - must be first child of `<table>`).
- **Cell Spanning**: `colspan="2"` (Merges horizontal columns), `rowspan="2"` (Merges vertical rows).

### 7. Forms Basics & Input Controls (Unit 07) ⭐⭐⭐
- **`<form>` Attributes**: `action="URL"`, `method="GET"` (data in URL) or `POST` (data in request body).
- **Labeling (`<label for="id">`)**: Clicking label focuses corresponding input. Essential for screen readers and user experience.
- **`name` Attribute**: CRITICAL! Inputs without `name` attributes are skipped during form submission payload creation.
- **Input Types**: `text`, `password`, `email`, `number`, `checkbox` (multi-select), `radio` (single choice - must share exact same `name`), `submit`, `reset`, `button`.
- **Textarea & Select**: `<textarea>` (multi-line text, needs `</textarea>`), `<select>` & `<option>` (dropdown menu).

### 8. Advanced Forms & Validations (Unit 08) ⭐⭐⭐
- **File Uploads**: `<input type="file" accept="image/*" multiple>`. `<form>` MUST have `enctype="multipart/form-data"`.
- **Hidden Input**: `<input type="hidden" name="token" value="123">`. Invisible to user, submits value with form payload (used for CSRF tokens & IDs).
- **HTML5 Native Validations**: `required`, `minlength`/`maxlength`, `min`/`max`, `step`, `pattern` (Regular Expression validation).
- **Widgets**: `<datalist>` (input autocomplete suggestions), `<fieldset>` & `<legend>` (form field visual/semantic grouping).

### 9. Semantic HTML Layouts (Unit 09) ⭐⭐⭐
- **Semantic Tags**: `<header>`, `<nav>`, `<main>` (Exactly 1 per page), `<section>` (thematic chapter with heading), `<article>` (independent standalone content), `<aside>` (sidebar), `<footer>`, `<time datetime="YYYY-MM-DD">`.
- **Div Soup Elimination**: Avoid replacing semantic HTML with pure `<div>` elements.

### 10. Layout Mechanics & Containers (Unit 10) ⭐⭐⭐
- **Block Display**: Starts on new line, 100% parent width (`<div>`, `<p>`, `<h1>`, `<section>`).
- **Inline Display**: Stays on same line, content width only, ignores CSS width/height (`<span>`, `<a>`, `<strong>`).
- **Inline-Block**: Stays on same line, respects CSS width/height (`<img>`, `<input>`, `<button>`).

### 11. Global Attributes & Custom Data (Unit 11) ⭐⭐⭐
- **Global Attributes**: `id` (strictly unique per page), `class` (reusable classifier), `title` (tooltip), `hidden` (boolean invisible state), `tabindex` (keyboard navigation: `tabindex="0"` makes element focusable; `tabindex="-1"` removes from tab order).
- **Custom Data Attributes (`data-*`)**: Store custom data in HTML markup. Accessible in JavaScript via `element.dataset` (e.g. `data-user-id="101"` $\rightarrow$ `element.dataset.userId`).

### 12. Multimedia & HTML5 Widgets (Unit 12) ⭐⭐
- **Media**: `<video controls poster="thumb.jpg">` and `<audio controls>`. Use `<source src="..." type="...">` for format fallbacks. `autoplay` requires `muted`.
- **`<iframe>`**: Embeds external pages/maps. ALWAYS include `title` attribute for a11y, and `sandbox` attribute for security.
- **Accordion & Dialog**: `<details>` & `<summary>` create native collapsible accordions without JS. `<dialog>` creates native modals operated via JS `.showModal()` and `.close()`.

### 13. Accessibility & SEO (Unit 13) ⭐⭐⭐
- **a11y & ARIA**: Use native HTML tags first (First Rule of ARIA). Use `aria-label="text"` for icon buttons, `aria-hidden="true"` for decorative icons, `aria-expanded="false"` for collapsible menus.
- **SEO & Social**: Meta description (150–160 chars for Google search snippet). Open Graph tags (`og:title`, `og:image`, `og:description`) for WhatsApp/LinkedIn preview cards.

### 14. HTML to CSS, JS & React (Unit 14) ⭐⭐⭐
- **Connecting Files**: `<link rel="stylesheet" href="style.css">`. `<script src="app.js" defer>` downloads in parallel and executes after DOM parsing completes (non-blocking).
- **React JSX Rules**: `class` $\rightarrow$ `className`, `for` $\rightarrow$ `htmlFor`, all elements MUST be self-closed (`<img />`, `<br />`), `style={{ color: "red" }}` accepts JS objects.

### 15. Placement Interview Concepts (Unit 15) ⭐⭐⭐
- **Browser Pipeline**: HTML parsing $\rightarrow$ DOM Tree $\rightarrow$ CSSOM Tree $\rightarrow$ Render Tree (visible nodes only) $\rightarrow$ Layout / Reflow (geometry) $\rightarrow$ Painting (pixels).
- **Reflow vs Repaint**: Reflow recalculates element sizes/positions (expensive). Repaint redraws pixel styles (color).
- **Quirks vs Standards Mode**: `<!DOCTYPE html>` triggers Standards Mode. Missing DOCTYPE causes legacy Quirks Mode.
- **Security**: XSS (Cross-Site Scripting) is prevented by HTML text escaping. Tabnabbing is prevented by `rel="noopener noreferrer"`.

---

## 📌 3. HTML Most Important Syntax Cheat Sheet

```html
<!-- 1. Document Boilerplate -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="150-160 char SEO page summary">
    <title>Page Title</title>
    <link rel="stylesheet" href="styles.css">
    <script src="app.js" defer></script>
</head>
<body>

    <!-- 2. Semantic Page Skeleton -->
    <header>
        <h1>Logo / Title</h1>
        <nav>
            <a href="index.html">Home</a> | 
            <a href="pages/about.html">About</a>
        </nav>
    </header>

    <main>
        <!-- 3. Form with File Upload & Validations -->
        <form action="/api/register" method="POST" enctype="multipart/form-data">
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required placeholder="user@site.com">

            <label for="avatar">Photo:</label>
            <input type="file" id="avatar" name="avatar" accept="image/*">

            <button type="submit">Submit</button>
        </form>

        <!-- 4. Image with CLS Prevention & Lazy Loading -->
        <figure>
            <img src="banner.webp" alt="Descriptive text" width="800" height="400" loading="lazy">
            <figcaption>Figure 1: Banner Caption</figcaption>
        </figure>

        <!-- 5. Accessible External Link -->
        <a href="https://external.com" target="_blank" rel="noopener noreferrer" title="External Site">
            External Secure Link
        </a>
    </main>

    <footer>
        <p><small>&copy; 2026 Developer Inc. All rights reserved.</small></p>
    </footer>

</body>
</html>
```

---

## 📌 4. HTML Top 50 Must-Remember Points

1. `<!DOCTYPE html>` is not an HTML tag; it is an instruction that triggers W3C Standards Mode.
2. An HTML Tag is `<tag>`; an HTML Element is `<tag>Content</tag>`.
3. Every webpage should have exactly one `<h1>` tag for optimal SEO outline structure.
4. `<strong>` represents semantic high importance; `<b>` represents visual bolding without weight.
5. `<em>` represents semantic stress emphasis; `<i>` represents foreign words/alternate tone.
6. `<sub>` lowers baseline (H₂O); `<sup>` raises baseline (E=mc²).
7. `<pre>` preserves whitespace and line breaks in monospace font.
8. Reserved characters must be escaped: `<` = `&lt;`, `>` = `&gt;`, `&` = `&amp;`.
9. `target="_blank"` links MUST include `rel="noopener noreferrer"` to prevent Tabnabbing security attacks.
10. `../` in a relative file path navigates UP one directory level.
11. `mailto:` opens email client; `tel:` opens phone dialer; `sms:` opens messaging app.
12. `download="file.pdf"` forces browser file download instead of inline preview.
13. `alt` attribute is mandatory on `<img>` for screen reader accessibility (a11y) and SEO.
14. Purely decorative images must use an empty string `alt=""` so screen readers skip them.
15. Setting explicit `width` and `height` on `<img>` prevents Cumulative Layout Shift (CLS).
16. `loading="lazy"` defers loading off-screen images until the user scrolls near them.
17. WebP is a modern web format offering 30% smaller file sizes than JPG/PNG.
18. SVG is XML-based vector code that scales infinitely without resolution loss.
19. `<figure>` wraps media content; `<figcaption>` provides its semantic caption.
20. Inner `<ul>` or `<ol>` lists MUST be nested directly inside an `<li>` element.
21. `<dl>` contains `<dt>` (Description Term/Key) and `<dd>` (Description Detail/Value).
22. `<table>` caption must be the first child tag: `<caption>Table Title</caption>`.
23. `colspan="2"` merges columns horizontally; `rowspan="2"` merges rows vertically.
24. `<thead>`, `<tbody>`, and `<tfoot>` group semantic table sections and repeat on printouts.
25. Forms submitting passwords or sensitive data MUST use `method="POST"`.
26. Inputs missing a `name` attribute are completely excluded from form submission data.
27. Radio buttons must share the exact SAME `name` attribute value to enforce single-choice grouping.
28. Form buttons default to `type="submit"`; use `type="button"` for generic JS action buttons.
29. `<label for="id">` links to an input's `id`, expanding click target area and helping screen readers.
30. `<textarea>` requires a closing tag `</textarea>` and is not self-closing.
31. Forms uploading files (`<input type="file">`) MUST set `enctype="multipart/form-data"`.
32. `<input type="hidden">` transmits invisible data payload (like CSRF security tokens).
33. `disabled` inputs are excluded from form submission; `readonly` inputs are included.
34. `<datalist>` provides search autocomplete suggestions while allowing custom user typing.
35. `pattern="[0-9]{10}"` enforces HTML5 Regular Expression native browser validation.
36. `<main>` element must be unique per document (only ONE `<main>` per page).
37. `<article>` represents standalone independent content (blog post); `<section>` is a thematic chapter.
38. `<div>` is a generic block container; `<span>` is a generic inline container.
39. Block elements take 100% width and start on a new line; Inline elements take content width and sit on the same line.
40. Pure inline elements (`<span>`, `<a>`) ignore CSS `width` and `height` properties.
41. `id` attributes must be strictly UNIQUE per HTML page.
42. Custom data attributes (`data-user-id="101"`) are accessed in JS via `element.dataset.userId`.
43. `tabindex="0"` makes non-interactive elements focusable via keyboard Tab key navigation.
44. `<iframe>` embeds MUST include a `title` attribute and `sandbox` attribute for security.
45. `<details>` and `<summary>` create native collapsible disclosure accordions without JavaScript.
46. `<dialog>` elements are operated natively in JS using `.showModal()` and `.close()`.
47. First Rule of ARIA: Do NOT use ARIA if a native HTML semantic tag already exists.
48. `<script defer>` downloads scripts in parallel and executes after DOM parsing finishes (non-blocking).
49. In React JSX, HTML `class` becomes `className` and `for` becomes `htmlFor`.
50. Reflow (Layout geometry calculation) is significantly more performance-intensive than Repaint.

---

## 📌 5. HTML Interview Traps ⚠️

1. ⚠️ **TRAP**: *"Can a page have multiple `<h1>` tags?"*  
   **TRUTH**: HTML5 permits it, but SEO best practices strictly require **only ONE `<h1>` tag per page** for document outline clarity.
2. ⚠️ **TRAP**: *"What is the difference between `alt` and `title` on images?"*  
   **TRUTH**: `alt` is alternative text for screen readers/broken images; `title` is a mouse hover tooltip.
3. ⚠️ **TRAP**: *"Why doesn't `width: 200px;` work on my `<span>` tag in CSS?"*  
   **TRUTH**: `<span>` is a pure inline element (`display: inline`), which ignores CSS `width` and `height`. You must set `display: inline-block` or `block`.
4. ⚠️ **TRAP**: *"Will an input with `disabled` submit its value to the backend server?"*  
   **TRUTH**: NO! `disabled` inputs are omitted from submission payloads. Use `readonly` or `<input type="hidden">` if the value must be submitted.
5. ⚠️ **TRAP**: *"What happens if a button inside `<form>` has no `type` attribute?"*  
   **TRUTH**: It defaults to `type="submit"` and will submit the form when clicked! Set `type="button"` for custom JS triggers.
6. ⚠️ **TRAP**: *"Can you put a `<div>` inside a `<p>` tag?"*  
   **TRUTH**: NO! HTML5 specifications prohibit block-level elements inside `<p>` elements.
7. ⚠️ **TRAP**: *"Is `data-user-role` accessed as `element.dataset['data-user-role']` in JavaScript?"*  
   **TRUTH**: NO! `data-` is stripped and hyphenated names convert to CamelCase: `element.dataset.userRole`.
8. ⚠️ **TRAP**: *"Does `display: none` keep an element in the browser Render Tree?"*  
   **TRUTH**: NO! `display: none` removes the node from the Render Tree (0px space). `visibility: hidden` keeps the node in the Render Tree (retaining space).

---

## 📌 6. HTML Final 10-Minute Pre-Interview Revision

- **DOCTYPE**: `<!DOCTYPE html>` $\rightarrow$ W3C Standards Mode.
- **Title / Meta**: Page tab title, `<meta name="description">` (150-160 chars), `<meta name="viewport">` (Mobile responsive).
- **Semantics**: `<header>`, `<nav>`, `<main>` (1 per page), `<section>` (chapter), `<article>` (standalone card), `<aside>` (sidebar), `<footer>`.
- **Block vs Inline**: Block = 100% width + New line (`div`, `p`, `h1`). Inline = Content width + Same line (`span`, `a`, `strong`).
- **Links**: `target="_blank"` $\rightarrow$ ALWAYS add `rel="noopener noreferrer"`.
- **Images**: `alt` required. Set `width` and `height` to prevent Cumulative Layout Shift (CLS). Use `loading="lazy"` for below-the-fold assets.
- **Forms**: `<form action="..." method="POST">`. Set `name` attribute on ALL inputs. Use `enctype="multipart/form-data"` for file uploads.
- **Validations**: `required`, `pattern="[0-9]{10}"`, `min`/`max`, `minlength`/`maxlength`.
- **Scripts**: `<script src="..." defer>` in `<head>` for non-blocking execution after DOM parsing.
- **React JSX**: `class` $\rightarrow$ `className`, `for` $\rightarrow$ `htmlFor`, self-close all tags (`<img />`, `<br />`).

---

*Revision complete! Proceed to [100_html_mass_hiring_mcqs.md](100_html_mass_hiring_mcqs.md) for 100 practice MCQs.* 🚀
