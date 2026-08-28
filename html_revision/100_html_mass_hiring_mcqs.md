# 💯 100 HTML Mass-Hiring Placement MCQs

This document contains **exactly 100 placement-focused HTML MCQs** designed for mass-hiring placement exams and technical interview rounds (TCS, Infosys, Wipro, Accenture, Cognizant, Capgemini, L&T, Tech Mahindra).

---

## 📌 Topic Distribution Index
- **Q1–Q25**: HTML Basics & Core Architecture (Unit 01)
- **Q26–Q40**: Text, Links, Images & Lists (Units 02, 03, 04, 05)
- **Q41–Q55**: Data Tables & Form Controls (Units 06, 07)
- **Q56–Q70**: Advanced Forms, Semantics & Global Attributes (Units 08, 09, 10, 11)
- **Q71–Q80**: Multimedia, Accessibility & SEO Meta (Units 12, 13)
- **Q81–Q90**: HTML + CSS + JavaScript + DOM + React JSX Connection (Unit 14)
- **Q91–Q100**: Tricky Placement-Level HTML Questions (Units 15, 16)

---

## 🟢 Part 1: HTML Basics & Core Architecture (Q1–Q25)

### Q1. What is the full form of HTML?
A. HyperText Markup Language  
B. High Text Machine Language  
C. Hyper Transfer Mark Language  
D. Home Tool Markup Language  

**Answer:** A  
**Explanation:** HTML stands for HyperText Markup Language, the standard markup language for creating web pages.

---

### Q2. What is the purpose of `<!DOCTYPE html>` at the beginning of an HTML document?
A. It is a mandatory closing tag  
B. It informs the browser to render the document in modern W3C Standards Mode  
C. It imports CSS styles  
D. It connects JavaScript files  

**Answer:** B  
**Explanation:** `<!DOCTYPE html>` is a declaration that instructs the browser rendering engine to use modern HTML5 Standards Mode instead of legacy Quirks Mode.

---

### Q3. What is the root element of an HTML page?
A. `<head>`  
B. `<body>`  
C. `<html>`  
D. `<!DOCTYPE>`  

**Answer:** C  
**Explanation:** The `<html>` element is the root container for all other HTML tags on a webpage.

---

### Q4. Which HTML element contains behind-the-scenes metadata, page titles, and external resource links?
A. `<body>`  
B. `<head>`  
C. `<main>`  
D. `<section>`  

**Answer:** B  
**Explanation:** The `<head>` tag holds metadata, `<title>`, character set declarations, and CSS/JS links that are not directly visible in the viewport.

---

### Q5. Which HTML element encloses all content displayed visually to the user in the browser viewport?
A. `<head>`  
B. `<body>`  
C. `<html>`  
D. `<meta>`  

**Answer:** B  
**Explanation:** `<body>` contains all visible webpage content such as headings, paragraphs, images, tables, and forms.

---

### Q6. What is the difference between an HTML Tag and an HTML Element?
A. They are identical  
B. A Tag is the markup syntax inside `< >`; an Element is Opening Tag + Content + Closing Tag  
C. Tags are in JavaScript; Elements are in CSS  
D. Elements cannot contain text  

**Answer:** B  
**Explanation:** A tag is syntax markup (e.g. `<h1>`), whereas an element includes the start tag, inner content, and end tag (e.g. `<h1>Hello</h1>`).

---

### Q7. What is a Void Element in HTML?
A. An element with an empty string value  
B. An element that cannot contain inner text or child nodes and lacks a closing tag  
C. A deleted element  
D. A custom JavaScript tag  

**Answer:** B  
**Explanation:** Void elements (self-closing tags like `<img>`, `<br>`, `<hr>`, `<meta>`, `<input>`) have no closing tags or inner content.

---

### Q8. Which element specifies the text displayed on the browser tab bar?
A. `<meta>`  
B. `<title>`  
C. `<header>`  
D. `<label>`  

**Answer:** B  
**Explanation:** `<title>` sets the title string shown on the browser tab bar and search engine results.

---

### Q9. What meta tag ensures character support for international scripts and emojis?
A. `<meta name="viewport">`  
B. `<meta charset="UTF-8">`  
C. `<meta name="language">`  
D. `<meta http-equiv="X-UA-Compatible">`  

**Answer:** B  
**Explanation:** `<meta charset="UTF-8">` configures UTF-8 character encoding supporting Unicode characters, emojis, and non-English scripts.

---

### Q10. What meta tag configuration enables mobile responsive viewport scaling?
A. `<meta name="mobile" content="true">`  
B. `<meta name="viewport" content="width=device-width, initial-scale=1.0">`  
C. `<meta name="responsive" content="yes">`  
D. `<meta name="screen" content="auto">`  

**Answer:** B  
**Explanation:** The viewport meta tag sets page width to device screen width and establishes initial 1.0 zoom scaling.

---

### Q11. What is the correct syntax for an HTML single-line comment?
A. `// This is a comment`  
B. `/* This is a comment */`  
C. `<!-- This is a comment -->`  
D. `' This is a comment`  

**Answer:** C  
**Explanation:** HTML comments begin with `<!--` and end with `-->`.

---

### Q12. How does the browser parser handle multiple consecutive spaces typed in HTML text?
A. Preserves all spaces  
B. Performs whitespace collapsing, reducing consecutive spaces to a single space  
C. Throws a syntax error  
D. Converts spaces into hyphens  

**Answer:** B  
**Explanation:** Browsers automatically collapse consecutive spaces, tabs, and line breaks inside standard elements into a single space.

---

### Q13. Which of the following is NOT a void element in HTML5?

A. `<img>`  
B. `<br>`  
C. `<p>`  
D. `<input>`  

**Answer:** C  
**Explanation:** `<p>` (Paragraph) is a paired element requiring a closing tag `</p>`.

---

### Q14. What tree structure does the browser build in memory after parsing an HTML file?
A. JSON Object  
B. Document Object Model (DOM) Tree  
C. Binary Search Tree  
D. CSSOM Tree  

**Answer:** B  
**Explanation:** The browser HTML parser converts HTML tags into a hierarchical tree of DOM node objects.

---

### Q15. What attribute specifies the primary natural language of an HTML document?
A. `lang="en"` on `<html>`  
B. `language="english"` on `<head>`  
C. `dict="en"` on `<body>`  
D. `locale="US"`  

**Answer:** A  
**Explanation:** The `lang` attribute on `<html>` informs screen readers and search engines of the document's primary language.

---

### Q16. Can HTML tags be written in uppercase like `<H1>` in HTML5?
A. No, it causes a syntax error  
B. Yes, HTML5 is case-insensitive, but lowercase is the universal W3C industry standard  
C. Only in Internet Explorer  
D. Uppercase is required  

**Answer:** B  
**Explanation:** HTML is case-insensitive, but W3C guidelines recommend lowercase tags for consistency and XML/JSX compatibility.

---

### Q17. Where should the `<script>` tag be placed if the `defer` attribute is NOT used?
A. Before `<!DOCTYPE html>`  
B. Inside `<title>`  
C. Right before the closing `</body>` tag to prevent render-blocking  
D. Inside `<meta>`  

**Answer:** C  
**Explanation:** Placing un-deferred scripts at the bottom of `<body>` ensures DOM elements parse before script execution.

---

### Q18. What happens if an HTML opening tag is missing its closing tag (e.g. `<p>Text`)?
A. The browser crashes  
B. The browser's error-recovery parser attempts to auto-close or infer the element boundary  
C. The page turns black  
D. The file is deleted  

**Answer:** B  
**Explanation:** Modern browser HTML parsers use forgiving error-recovery algorithms to infer missing closing tags.

---

### Q19. What element provides metadata instructions for search engine crawlers regarding indexing?

A. `<meta name="robots" content="index, follow">`  
B. `<meta name="crawler">`  
C. `<meta name="google">`  
D. `<link rel="search">`  

**Answer:** A  
**Explanation:** The robots meta tag instructs search crawlers whether to index and follow page links.

---

### Q20. Is HTML a programming language?
A. Yes, it has loops and functions  
B. No, HTML is a Markup Language used for content structuring without programming logic  
C. Yes, it compiles to C++  
D. Only when combined with CSS  

**Answer:** B  
**Explanation:** HTML is a declarative markup language for structuring content, lacking computational programming logic like loops or variables.

---

### Q21. Which global attribute specifies an element's unique identifier?
A. `class`  
B. `id`  
C. `key`  
D. `name`  

**Answer:** B  
**Explanation:** `id` assigns a strictly unique identifier to an HTML element.

---

### Q22. What tag connects a browser tab Favicon graphic in `<head>`?
A. `<link rel="icon" href="favicon.ico">`  
B. `<meta name="icon" content="favicon.ico">`  
C. `<img src="favicon.ico">`  
D. `<icon href="favicon.ico">`  

**Answer:** A  
**Explanation:** `<link rel="icon" href="...">` connects the tab icon graphic in the document `<head>`.

---

### Q23. What global attribute provides a native browser mouse hover tooltip?
A. `alt`  
B. `title`  
C. `tooltip`  
D. `hover`  

**Answer:** B  
**Explanation:** The global `title` attribute displays a native browser tooltip pop-up box upon hovering.

---

### Q24. Which element is used to include inline CSS styles inside an HTML document?
A. `<script>`  
B. `<style>`  
C. `<css>`  
D. `<link>`  

**Answer:** B  
**Explanation:** The `<style>` tag holds internal CSS rules within the document.

---

### Q25. What is the default display behavior of `<h1>` through `<h6>` headings?
A. `inline`  
B. `block`  
C. `inline-block`  
D. `none`  

**Answer:** B  
**Explanation:** All heading elements (`<h1>`-`<h6>`) are block-level elements that start on a new line.

---

## 🟡 Part 2: Text, Links, Images & Lists (Q26–Q40)

### Q26. According to SEO best practices, how many `<h1>` elements should a single HTML page contain?
A. Exactly 1  
B. As many as possible  
C. 5  
D. None  

**Answer:** A  
**Explanation:** Having a single `<h1>` per page establishes a clear primary topic outline for search engines.

---

### Q27. What is the semantic difference between `<strong>` and `<b>`?
A. `<strong>` is visual bold; `<b>` is semantic  
B. `<strong>` indicates high semantic importance; `<b>` applies bold styling without added importance  
C. `<b>` is deprecated  
D. They render differently in color  

**Answer:** B  
**Explanation:** `<strong>` conveys strong importance/urgency to screen readers and search crawlers, whereas `<b>` is purely stylistic.

---

### Q28. Which tag represents subscript text (e.g. $H_2O$)?
A. `<sup>`  
B. `<sub>`  
C. `<subscript>`  
D. `<under>`  

**Answer:** B  
**Explanation:** `<sub>` lowers character alignment below the baseline.

---

### Q29. Which tag represents superscript text (e.g. $E=mc^2$)?
A. `<sub>`  
B. `<sup>`  
C. `<super>`  
D. `<up>`  

**Answer:** B  
**Explanation:** `<sup>` raises character alignment above the baseline.

---

### Q30. Which tag preserves whitespace, tabs, and line breaks in a monospace font?
A. `<p>`  
B. `<pre>`  
C. `<code>`  
D. `<span>`  

**Answer:** B  
**Explanation:** `<pre>` (preformatted text) preserves all whitespace and line breaks as typed.

---

### Q31. What HTML entity code represents the less-than symbol (`<`)?
A. `&lt;`  
B. `&gt;`  
C. `&amp;`  
D. `&less;`  

**Answer:** A  
**Explanation:** `&lt;` stands for "Less Than" (`<`), preventing the browser from interpreting text as an HTML tag.

---

### Q32. What security attribute combination MUST be added to external links opening in a new tab (`target="_blank"`)?
A. `rel="security"`  
B. `rel="noopener noreferrer"`  
C. `type="external"`  
D. `secure="true"`  

**Answer:** B  
**Explanation:** `rel="noopener noreferrer"` prevents tabnabbing phishing attacks by severing `window.opener` access in newly opened tabs.

---

### Q33. What relative file path symbol navigates UP one directory level?
A. `./`  
B. `../`  
C. `//`  
D. `~/`  

**Answer:** B  
**Explanation:** `../` instructs the browser parser to ascend one directory level up into the parent folder.

---

### Q34. How do you create an internal page jump link to `<section id="pricing">`?
A. `<a href="pricing">`  
B. `<a href="#pricing">`  
C. `<a href="?pricing">`  
D. `<a href="@pricing">`  

**Answer:** B  
**Explanation:** Internal page anchor links use `#` followed by the target element's `id`.

---

### Q35. What special URL scheme opens the device phone dialer?
A. `phone:`  
B. `call:`  
C. `tel:`  
D. `dial:`  

**Answer:** C  
**Explanation:** `tel:+919876543210` opens the native phone dialer on mobile devices.

---

### Q36. Why is setting explicit `width` and `height` attributes on `<img>` tags recommended?
A. To make images load faster  
B. To allocate aspect ratio space and prevent Cumulative Layout Shift (CLS)  
C. To change image colors  
D. To disable right-click  

**Answer:** B  
**Explanation:** Setting explicit dimensions allows the layout engine to reserve space before image download, preventing layout shifts.

---

### Q37. What should be placed in the `alt` attribute of a purely decorative graphic?
A. `alt="decorative"`  
B. `alt=""` (Empty string)  
C. Omit `alt` attribute  
D. `alt="image"`  

**Answer:** B  
**Explanation:** `alt=""` instructs screen readers to silently skip decorative images.

---

### Q38. Which HTML5 elements encapsulate media alongside a semantic text caption?
A. `<div>` and `<p>`  
B. `<figure>` and `<figcaption>`  
C. `<section>` and `<caption>`  
D. `<media>` and `<title>`  

**Answer:** B  
**Explanation:** `<figure>` encapsulates self-contained media, and `<figcaption>` provides its semantic caption.

---

### Q39. What attribute enables native image lazy loading?
A. `lazy="true"`  
B. `loading="lazy"`  
C. `defer="image"`  
D. `async="true"`  

**Answer:** B  
**Explanation:** `loading="lazy"` defers off-screen image loading until the user scrolls near it.

---

### Q40. Which list tag creates an ordered numerical list?
A. `<ul>`  
B. `<ol>`  
C. `<dl>`  
D. `<list>`  

**Answer:** B  
**Explanation:** `<ol>` defines an ordered sequential list (1, 2, 3...).

---

## 🟠 Part 3: Tables & Forms (Q41–Q55)

### Q41. Which tag defines a table header cell with default bold text and centered alignment?
A. `<td>`  
B. `<th>`  
C. `<tr>`  
D. `<thead>`  

**Answer:** B  
**Explanation:** `<th>` represents a table header cell, rendered bold and centered by default.

---

### Q42. Which tag must be the VERY FIRST child inside a `<table>` to define its title?
A. `<title>`  
B. `<caption>`  
C. `<thead>`  
D. `<header>`  

**Answer:** B  
**Explanation:** `<caption>` defines the title of a table and must be the first child inside `<table>`.

---

### Q43. What attribute merges a table cell across 3 horizontal columns?
A. `rowspan="3"`  
B. `colspan="3"`  
C. `span="3"`  
D. `merge="3"`  

**Answer:** B  
**Explanation:** `colspan="3"` merges 3 horizontal columns into a single cell.

---

### Q44. What attribute merges a table cell across 2 vertical rows?
A. `colspan="2"`  
B. `rowspan="2"`  
C. `vspan="2"`  
D. `height="2"`  

**Answer:** B  
**Explanation:** `rowspan="2"` merges 2 vertical rows in the same column.

---

### Q45. What are the three semantic section elements of an HTML table?
A. `<thead>`, `<tbody>`, `<tfoot>`  
B. `<top>`, `<middle>`, `<bottom>`  
C. `<head>`, `<body>`, `<footer>`  
D. `<header>`, `<content>`, `<footer`  

**Answer:** A  
**Explanation:** `<thead>` (header), `<tbody>` (body), and `<tfoot>` (footer) group semantic table sections.

---

### Q46. What form HTTP submission method appends input values into the browser URL bar?
A. `POST`  
B. `GET`  
C. `PUT`  
D. `DELETE`  

**Answer:** B  
**Explanation:** `GET` appends form input key-value pairs to the URL query string (`?key=val`).

---

### Q47. What form submission method hides data inside the HTTP Request Body?
A. `GET`  
B. `POST`  
C. `FETCH`  
D. `QUERY`  

**Answer:** B  
**Explanation:** `POST` sends form payload data inside the HTTP Request Body, keeping sensitive data out of the URL bar.

---

### Q48. What attribute explicitly links a `<label>` element to an input's `id`?
A. `for`  
B. `link`  
C. `target`  
D. `id`  

**Answer:** A  
**Explanation:** `<label for="input-id">` links the label to the input with `id="input-id"`.

---

### Q49. What happens to inputs missing a `name` attribute during form submission?
A. HTML syntax error  
B. Their values are completely excluded from the submitted form payload  
C. Input text turns red  
D. The button disables  

**Answer:** B  
**Explanation:** Browsers construct form payloads using `name=value` pairs. Without a `name` attribute, inputs are skipped.

---

### Q50. How do you group radio buttons so only ONE option can be selected at a time?
A. Give them unique `id` values  
B. Give all radio buttons in the group the exact SAME `name` attribute value  
C. Wrap them in `<div>`  
D. Set `type="single"`  

**Answer:** B  
**Explanation:** Radio buttons sharing the same `name` attribute form a single-choice exclusive selection group.

---

### Q51. What input attribute displays light gray hint text inside an empty input box?
A. `value`  
B. `placeholder`  
C. `hint`  
D. `title`  

**Answer:** B  
**Explanation:** `placeholder` displays temporary hint text inside an empty input field.

---

### Q52. What is the default `type` behavior of a `<button>` element placed inside a `<form>`?
A. `type="button"`  
B. `type="submit"`  
C. `type="reset"`  
D. `type="none"`  

**Answer:** B  
**Explanation:** Inside a `<form>`, buttons default to `type="submit"`, triggering form submission when clicked.

---

### Q53. Which element creates a multi-line text input field?
A. `<input type="text">`  
B. `<textarea>`  
C. `<textbox>`  
D. `<multiline>`  

**Answer:** B  
**Explanation:** `<textarea>` provides a multi-line plain text editing control.

---

### Q54. Which element creates a dropdown selection menu?
A. `<dropdown>`  
B. `<select>`  
C. `<option>`  
D. `<menu>`  

**Answer:** B  
**Explanation:** `<select>` creates a drop-down selection menu containing `<option>` items.

---

### Q55. Which boolean attribute forces native browser validation to block submission if an input is left blank?
A. `validate`  
B. `required`  
C. `mandatory`  
D. `check`  

**Answer:** B  
**Explanation:** `required` specifies that an input field must be filled before submitting.

---

## 🔵 Part 4: Advanced Forms, Semantics & Attributes (Q56–Q70)

### Q56. Which `enctype` value MUST be set on a `<form>` tag to support binary file uploads (`<input type="file">`)?
A. `application/x-www-form-urlencoded`  
B. `multipart/form-data`  
C. `text/plain`  
D. `application/json`  

**Answer:** B  
**Explanation:** `enctype="multipart/form-data"` is required when uploading files so data is sent in multi-part binary streams.

---

### Q57. What input type is rendered invisibly on screen but submits its value to the server payload?
A. `type="hidden"`  
B. `type="invisible"`  
C. `type="secret"`  
D. `type="none"`  

**Answer:** A  
**Explanation:** `<input type="hidden">` is invisible to users and passes tokens/IDs silently in form payloads.

---

### Q58. Which HTML5 attribute validates text inputs using Regular Expressions (Regex)?
A. `regex`  
B. `pattern`  
C. `rule`  
D. `validate`  

**Answer:** B  
**Explanation:** `pattern="[0-9]{10}"` applies Regex pattern validation natively in browsers.

---

### Q59. Which HTML5 element provides autocomplete search suggestions while allowing custom text entry?
A. `<select>`  
B. `<datalist>`  
C. `<optgroup>`  
D. `<list>`  

**Answer:** B  
**Explanation:** `<datalist>` connects to `<input list="id">` to offer dropdown suggestions while leaving the input editable.

---

### Q60. What element visually and semantically groups related form fields together with a border box?
A. `<group>`  
B. `<fieldset>`  
C. `<container>`  
D. `<section>`  

**Answer:** B  
**Explanation:** `<fieldset>` groups form controls visually, and `<legend>` supplies a border caption.

---

### Q61. Which input attribute is excluded from form submission data when set?
A. `readonly`  
B. `disabled`  
C. `required`  
D. `placeholder`  

**Answer:** B  
**Explanation:** `disabled` inputs are grayed out and omitted from submission payloads. `readonly` inputs ARE submitted.

---

### Q62. What element represents the unique primary content of a webpage (only 1 per document)?
A. `<header>`  
B. `<main>`  
C. `<section>`  
D. `<body>`  

**Answer:** B  
**Explanation:** `<main>` represents the unique primary content of a page; specifications restrict it to one per document.

---

### Q63. What is the key distinction between `<article>` and `<section>`?
A. `<article>` is larger than `<section>`  
B. `<article>` represents independent, self-contained reusable content; `<section>` is a thematic part of a page  
C. `<section>` is non-semantic  
D. `<article>` cannot contain headings  

**Answer:** B  
**Explanation:** `<article>` content stands alone independently (e.g. blog post card); `<section>` groups thematic content.

---

### Q64. What semantic element represents sidebars or tangentially related callout widgets?
A. `<aside>`  
B. `<nav>`  
C. `<header>`  
D. `<footer>`  

**Answer:** A  
**Explanation:** `<aside>` represents secondary or tangentially related content like sidebars.

---

### Q65. What attribute on `<time>` specifies machine-readable ISO date strings for search engines?
A. `datetime`  
B. `date`  
C. `value`  
D. `time`  

**Answer:** A  
**Explanation:** `<time datetime="2026-08-28">` provides standardized ISO date formatting for search crawlers.

---

### Q66. What is the default CSS display property of a `<div>` element?
A. `inline`  
B. `block`  
C. `inline-block`  
D. `none`  

**Answer:** B  
**Explanation:** `<div>` is a generic block-level container (`display: block`).

---

### Q67. What is the default CSS display property of a `<span>` element?
A. `block`  
B. `inline`  
C. `flex`  
D. `grid`  

**Answer:** B  
**Explanation:** `<span>` is a generic inline-level text container (`display: inline`).

---

### Q68. How much width does a block-level element occupy by default?
A. Only its text content width  
B. 100% of its parent container's available width  
C. 50% width  
D. 0px  

**Answer:** B  
**Explanation:** Block elements stretch to fill 100% of their parent container's available width.

---

### Q69. What happens when you apply CSS `width` and `height` to a pure inline element (`<span>`)?
A. The element resizes  
B. Browsers ignore width and height properties on pure inline elements  
C. Syntax error  
D. Text deletes  

**Answer:** B  
**Explanation:** Pure inline elements (`display: inline`) ignore CSS `width` and `height` properties.

---

### Q70. How is custom data attribute `data-user-id="101"` accessed in JavaScript?
A. `element.dataUserId`  
B. `element.dataset.userId`  
C. `element.dataset['data-user-id']`  
D. `element.getData("user-id")`  

**Answer:** B  
**Explanation:** Custom data attributes map to `element.dataset`, converting hyphenated names into CamelCase (`userId`).

---

## 🟣 Part 5: Multimedia, Accessibility & SEO (Q71–Q80)

### Q71. Which tag specifies format fallbacks inside `<video>` or `<audio>` elements?
A. `<source>`  
B. `<media>`  
C. `<url>`  
D. `<file>`  

**Answer:** A  
**Explanation:** `<source src="..." type="...">` specifies fallback media files.

---

### Q72. Why do modern browsers block video `autoplay` on page load unless `muted` is also set?
A. Specification bug  
B. User experience protection against intrusive background audio playback  
C. Saves CPU  
D. Muted is compulsory  

**Answer:** B  
**Explanation:** Autoplay policies require `muted` alongside `autoplay` to prevent unrequested audio.

---

### Q73. What security attribute restricts script execution and same-origin access on `<iframe>` embeds?
A. `protect`  
B. `sandbox`  
C. `strict`  
D. `security`  

**Answer:** B  
**Explanation:** `sandbox` applies security restrictions to content inside an `<iframe>`.

---

### Q74. Which tag pair creates a native collapsible disclosure accordion without JavaScript?
A. `<details>` and `<summary>`  
B. `<accordion>` and `<item>`  
C. `<collapse>` and `<title>`  
D. `<toggle>` and `<header>`  

**Answer:** A  
**Explanation:** `<details>` wraps the container, and `<summary>` provides the clickable heading tag.

---

### Q75. What JS method opens a native `<dialog>` element as a modal window with a backdrop layer?
A. `dialog.open()`  
B. `dialog.showModal()`  
C. `dialog.popup()`  

**Answer:** B  
**Explanation:** `.showModal()` opens a `<dialog>` element as a backdrop-blocked modal.

---

### Q76. What ARIA attribute provides accessible labels for icon-only buttons?
A. `alt`  
B. `aria-label`  
C. `title`  
D. `description`  

**Answer:** B  
**Explanation:** `aria-label` supplies an accessible text string for interactive controls without visible text.

---

### Q77. What ARIA attribute hides decorative graphics from screen readers?
A. `aria-hidden="true"`  
B. `hidden="true"`  
C. `display="none"`  

**Answer:** A  
**Explanation:** `aria-hidden="true"` removes elements from the accessibility tree so screen readers skip them.

---

### Q78. Why is `<button>` preferred over `<div onClick>` for interactive buttons?
A. `<button>` changes color  
B. `<button>` is natively focusable via `Tab` key and triggers on `Enter` and `Space` keypresses  
C. `<div onClick>` is forbidden  

**Answer:** B  
**Explanation:** Native `<button>` elements handle keyboard focus and keypress activation out-of-the-box.

---

### Q79. What meta property prefix controls link preview cards shared on WhatsApp, Facebook, or LinkedIn?
A. `og:` (Open Graph)  
B. `seo:`  
C. `card:`  

**Answer:** A  
**Explanation:** Open Graph (`og:title`, `og:image`, `og:description`) specifies social media link sharing preview cards.

---

### Q80. What tag specifies the authoritative URL to prevent SEO duplicate content penalties?
A. `<link rel="canonical" href="...">`  
B. `<meta name="duplicate">`  
C. `<meta name="original">`  

**Answer:** A  
**Explanation:** Canonical link tags (`<link rel="canonical">`) define the primary authoritative URL for search indexing.

---

## 🔴 Part 6: HTML + CSS + JS + DOM + React/JSX Connection (Q81–Q90)

### Q81. How does `<script src="app.js" defer>` execute relative to HTML parsing?
A. Blocks parsing while downloading  
B. Downloads in parallel with HTML parsing and executes ONLY after DOM parsing completes  
C. Never executes  

**Answer:** B  
**Explanation:** `defer` downloads non-blockingly and executes after DOM parsing completes.

---

### Q82. How does `<script src="app.js" async>` execute?
A. Executes after page unload  
B. Downloads in parallel and executes IMMEDIATELY when finished, pausing HTML parsing  
C. Executes only on mobile  

**Answer:** B  
**Explanation:** `async` scripts execute immediately upon finishing download, which can pause HTML parsing.

---

### Q83. What HTML attribute is replaced by `className` in React JSX?
A. `class`  
B. `id`  
C. `style`  

**Answer:** A  
**Explanation:** `className` replaces `class` in JSX because `class` is a reserved JavaScript keyword.

---

### Q84. What attribute replaces HTML `for` on `<label>` elements in React JSX?
A. `htmlFor`  
B. `labelFor`  
C. `targetFor`  

**Answer:** A  
**Explanation:** `htmlFor` replaces `for` in JSX because `for` is a reserved JS loop keyword.

---

### Q85. How must void elements (like `<img>` or `<br>`) be written in React JSX?
A. Unclosed tags  
B. Explicitly self-closed tags (`<img />`, `<br />`)  
C. Inside `<div>`  

**Answer:** B  
**Explanation:** React JSX requires all void elements to be explicitly self-closed (`<img />`).

---

### Q86. Which JS method selects the first DOM element matching CSS selector `#btn`?
A. `document.querySelector("#btn")`  
B. `document.getElementByIdName("#btn")`  
C. `document.find("#btn")`  

**Answer:** A  
**Explanation:** `document.querySelector("#btn")` selects the first DOM element matching the CSS selector.

---

### Q87. How are inline CSS styles passed to elements in React JSX?
A. `style="color: red;"`  
B. `style={{ color: "red" }}`  
C. `style={color: red}`  

**Answer:** B  
**Explanation:** In JSX, inline styles accept a JavaScript object wrapped in double curly braces (`style={{ color: "red" }}`).

---

### Q88. What JS DOM property exposes an HTML element's `class` attribute string?
A. `el.class`  
B. `el.className`  
C. `el.cssClass`  

**Answer:** B  
**Explanation:** In DOM objects, the `class` attribute is accessed via `el.className`.

---

### Q89. What JS method attaches a click event listener to a DOM node `el`?
A. `el.addEventListener("click", callback)`  
B. `el.click(callback)`  
C. `el.attach("click")`  

**Answer:** A  
**Explanation:** `addEventListener("click", callback)` is the standard W3C DOM method for binding event handlers.

---

### Q90. What feature in React JSX groups multiple children without adding extra DOM node wrappers?
A. `<React.Fragment>` (or `<>...</>`)  
B. `<React.Div>`  
C. `<React.Container>`  

**Answer:** A  
**Explanation:** React Fragments (`<>...</>`) group JSX children without injecting extra `<div>` wrapper nodes into the DOM tree.

---

## ⚡ Part 7: Tricky Placement-Level HTML Questions (Q91–Q100)

### Q91. What is the browser pipeline sequence from HTML parsing to pixel output?
A. HTML Parsing $\rightarrow$ DOM/CSSOM $\rightarrow$ Render Tree $\rightarrow$ Layout (Reflow) $\rightarrow$ Painting  
B. Paint $\rightarrow$ Layout $\rightarrow$ DOM  
C. Layout $\rightarrow$ Render Tree $\rightarrow$ Paint  

**Answer:** A  
**Explanation:** The browser builds DOM/CSSOM, constructs the Render Tree, calculates Layout geometry (Reflow), and Paints pixels.

---

### Q92. What is the difference between Reflow and Repaint in browser rendering?
A. They are identical  
B. Reflow recalculates element geometry/layout (expensive); Repaint redraws pixel styles like color without changing layout  
C. Repaint is slower  

**Answer:** B  
**Explanation:** Reflow recalculates element dimensions and positions, making it much more computationally expensive than Repaint.

---

### Q93. What is the difference between `element.getAttribute("value")` and `element.value` in JavaScript?
A. They return the same thing  
B. `getAttribute("value")` returns static initial markup text; `element.value` returns live user-typed DOM property state  
C. `element.value` is static  

**Answer:** B  
**Explanation:** Attributes reflect initial HTML source values, whereas DOM properties reflect live user-input state.

---

### Q94. What CSS specificity level does an inline `style="..."` attribute possess?
A. Lowest specificity  
B. Highest specificity (overrides class and ID stylesheet rules)  
C. Equal to tag selectors  

**Answer:** B  
**Explanation:** Inline styles carry the highest specificity, overriding class and ID selectors in external stylesheets.

---

### Q95. What happens if `<script src="app.js">` in `<head>` has NO `defer` or `async` attribute?
A. Script is ignored  
B. Render-blocking occurs, pausing HTML parsing until the script finishes downloading and running  
C. Page loads faster  

**Answer:** B  
**Explanation:** Standard scripts in `<head>` block the HTML parser until download and execution complete.

---

### Q96. Is putting a `<div>` inside a `<p>` tag valid HTML5 syntax?
A. Yes  
B. No, HTML5 specifications prohibit block-level elements inside `<p>` tags  
C. Only in forms  

**Answer:** B  
**Explanation:** W3C specifications state that `<p>` tags cannot contain block-level elements like `<div>`.

---

### Q97. What does `tabindex="0"` do on a non-interactive `<div>`?
A. Hides the div  
B. Inserts the `<div>` into natural keyboard Tab navigation order  
C. Moves div to page top  

**Answer:** B  
**Explanation:** `tabindex="0"` makes non-interactive elements focusable via keyboard Tab navigation.

---

### Q98. What open graph meta tag specifies the social media share preview image URL?
A. `<meta property="og:image" content="...">`  
B. `<meta property="og:picture">`  
C. `<meta property="og:thumb">`  

**Answer:** A  
**Explanation:** `og:image` sets the preview image URL displayed on social link cards.

---

### Q99. How does `loading="lazy"` on `<img>` tags improve page performance metrics?
A. Compresses image files  
B. Defers network fetching of off-screen images, improving initial load speed and reducing bandwidth  
C. Rotates images  

**Answer:** B  
**Explanation:** Lazy loading defers off-screen image network requests until scrolled near the viewport.

---

### Q100. In mass-hiring placement interviews, what is the First Rule of ARIA?
A. Always use ARIA  
B. Do NOT use ARIA if a native HTML semantic element already exists  
C. ARIA replaces CSS  

**Answer:** B  
**Explanation:** The First Rule of ARIA states: *"If you can use a native HTML element with the required semantics, do so instead of adding ARIA."*

---

## 📌 FINAL 25 MUST-KNOW HTML QUESTIONS INDEX

If you have limited time, master these 25 essential questions first:
`Q2`, `Q7`, `Q10`, `Q17`, `Q26`, `Q27`, `Q32`, `Q33`, `Q36`, `Q43`, `Q46`, `Q47`, `Q49`, `Q50`, `Q56`, `Q62`, `Q63`, `Q70`, `Q74`, `Q78`, `Q81`, `Q83`, `Q91`, `Q92`, `Q93`.

---

## 📌 HTML MASS-HIRING LAST-MINUTE CHECKLIST

Before entering your placement assessment or technical interview, verify you can answer these 10 core checks:

1. [ ] Do you know why `<!DOCTYPE html>` is compulsory for Standards Mode?
2. [ ] Can you explain the difference between `<strong>` vs `<b>` and `<em>` vs `<i>`?
3. [ ] Do you know why `target="_blank"` requires `rel="noopener noreferrer"`?
4. [ ] Can you explain how explicit `width` and `height` attributes prevent Cumulative Layout Shift (CLS)?
5. [ ] Do you know why forms that upload files require `enctype="multipart/form-data"`?
6. [ ] Can you explain why inputs MUST have a `name` attribute to be submitted to backend servers?
7. [ ] Do you know the difference between `<article>`, `<section>`, and `<div>`?
8. [ ] Can you explain Block vs Inline display rules (`<div>` vs `<span>`)?
9. [ ] Do you know the difference between `<script defer>` and `<script async>`?
10. [ ] Can you list 3 differences between HTML syntax and React JSX (`className`, `htmlFor`, self-closing tags)?

---

*100 MCQs Complete! You are fully prepared for your HTML Mass-Hiring Assessments & Technical Interviews.* 🚀
