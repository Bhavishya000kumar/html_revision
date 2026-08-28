# Unit 02 — Text & Headings (Master Study Notes)

Welcome to **Unit 02: Text & Headings**! Is unit me hum web page par text content ko structure karna, headings hierarchy follow karna, formatting tags, preformatted code, aur HTML entities ko detail me samjhenge.

---

## 1. Introduction to Text in HTML

HTML me text sirf words dikhane ke liye nahi hota, balki browser, search engines (Google), aur screen readers ko text ka **meaning (semantics)** samjhane ke liye use hota hai.

- **Content vs Presentation**: HTML ka kaam content ka **meaning** define karna hai (jaise ye main heading hai, ye important warning text hai). Styling (font size, font family, color) hamesha **CSS** se di jaati hai.
- **Whitespace Collapsing**: Browser HTML code me kitne bhi extra spaces ya line breaks ko **single space** me convert kar deta hai. Line breaks ke liye `<p>` ya `<br>` tag ki zaroorat padti hai.

---

## 2. Headings Hierarchy (`<h1>` to `<h6>`)

HTML text hierarchy ke liye **6 heading elements** provide karta hai: `<h1>` (sabse bada/sabse important) se lekar `<h6>` (sabse chota/sabse kam important).

```html
<h1>Heading Level 1 - Main Page Title</h1>
<h2>Heading Level 2 - Major Section</h2>
<h3>Heading Level 3 - Sub Section</h3>
<h4>Heading Level 4 - Sub-sub Section</h4>
<h5>Heading Level 5 - Minor Heading</h5>
<h6>Heading Level 6 - Smallest Heading</h6>
```

### 🚨 Crucial Rules for Headings:

1. **Single `<h1>` Rule**: Hard page par generally **sirf EK `<h1>` tag** hona chahiye. Ye page ka main title hota hai. Multiple `<h1>` tags SEO ranking ko hurt karte hain.
2. **Logical Sequence**: Heading levels ko **sequence** me use karein (`<h1>` → `<h2>` → `<h3>`). Never skip levels (jaise `<h1>` ke turant baad `<h4>` mat use karein).
3. **DO NOT Use Headings for Font Size**: Headings text ko bada dikhane ke liye nahi, balki **document outline** structure karne ke liye hoti hain. Text bada karna CSS ka kaam hai (`font-size`).

### Headings Comparison Table

| Tag | Level | Purpose | Default Browser Style | SEO Weight |
|---|---|---|---|---|
| `<h1>` | Main Title | Document/Page ka main heading | 2em (32px), Bold | 🔥 Highest |
| `<h2>` | Major Section | Sub-topic / Chapter heading | 1.5em (24px), Bold | High |
| `<h3>` | Subsection | Major section ke andar ka sub-heading | 1.17em (18.72px), Bold | Medium |
| `<h4>` | Minor Section | Detail subsection | 1em (16px), Bold | Normal |
| `<h5>` | Small Heading | Rare usage / Minor label | 0.83em (13.28px), Bold | Low |
| `<h6>` | Smallest Heading | Footer labels / Fine print header | 0.67em (10.72px), Bold | Lowest |

---

## 3. Paragraphs (`<p>`)

Paragraph text blocks ko represent karta hai.

```html
<p>This is a standard paragraph in HTML. Browsers automatically add top and bottom margins to paragraphs.</p>
```

### Key Behaviors of `<p>`:
1. **Block-Level Element**: Paragraph naye line se start hota hai aur poori available width occupy karta hai.
2. **Automatic Margin**: Browser default CSS me `<p>` element ke upar aur niche spacing (margin) add karta hai.
3. **Whitespace Collapsing**:
   ```html
   <!-- Browser output me extra spaces Ignore ho jayenge -->
   <p>Hello          World!</p> <!-- Rendered as: "Hello World!" -->
   ```

---

## 4. Line Breaks (`<br>`) and Horizontal Rules (`<hr>`)

Dono **Void Elements** hain (no closing tag).

### 1. Line Break (`<br>`)
`<br>` naye paragraph ke bina **single line break** create karta hai.

```html
<p>Bhavishya Kumar<br>Full Stack Developer<br>New Delhi, India</p>
```
> ⚠️ **Best Practice**: Line gap create karne ke liye repeated `<br><br><br>` mat use karein! Line spacing ke liye CSS margins use karein. `<br>` sirf address, poetry, ya line-sensitive text me use hota hai.

### 2. Horizontal Rule (`<hr>`)
`<hr>` semantic section break (theme change / divider line) draw karta hai.

```html
<h2>Section 1: Basics</h2>
<p>Content of section 1...</p>
<hr>
<h2>Section 2: Advanced</h2>
<p>Content of section 2...</p>
```

---

## 5. Text Formatting & Semantic Weight

HTML me text formatting tags do categories me hote hain:
1. **Semantic Formatting Tags**: Text ko meaning & importance dete hain.
2. **Visual Formatting Tags**: Text ko sirf visually change karte hain.

### 1. `<strong>` vs `<b>`

- `<strong>`: Represents **High Importance / Serious Warning**. Screen readers ise **strong vocal stress** ke sath read karte hain. Search engines ise heavy weightage dete hain.
- `<b>`: Represents **Stylistically Bold Text** without any extra importance (e.g. key terms in an introduction).

```html
<!-- Semantic High Importance -->
<p><strong>DANGER:</strong> Do not cross the high voltage line!</p>

<!-- Visual Bold only -->
<p>The course covers <b>HTML</b>, <b>CSS</b>, and <b>JavaScript</b>.</p>
```

### 2. `<em>` vs `<i>`

- `<em>`: Represents **Stress Emphasis** (changing the sentence meaning). Screen readers pitch change karke pronounce karte hain.
- `<i>`: Represents text in an **alternate tone or voice** (technical terms, idiomatic phrases, foreign language words, thoughts).

```html
<!-- Emphasis -->
<p>You <em>must</em> complete the assignment today.</p>

<!-- Alternate Voice / Foreign Word -->
<p>The term <i>carpe diem</i> means seize the day.</p>
```

### 3. Other Essential Formatting Tags

| Tag | Full Name | Semantic Purpose | Visual Rendering |
|---|---|---|---|
| `<mark>` | Mark / Highlight | Relevance / Highlighted text (search results match) | Yellow background highlight |
| `<small>` | Small Text | Side comments, legal disclaimers, copyright fine print | Smaller font size (approx 80%) |
| `<sub>` | Subscript | Chemical formulas (H₂O), subscript numbers | Lowered baseline, smaller font |
| `<sup>` | Superscript | Mathematical exponents ($E=mc^2$), ordinal numbers ($1^{st}$) | Raised baseline, smaller font |
| `<u>` | Underline | Unarticulated annotation (spelling mistake, proper name in Chinese) | Underlined text |

#### Code Examples:
```html
<!-- Subscript & Superscript -->
<p>Water formula: H<sub>2</sub>O</p>
<p>Einstein equation: E = mc<sup>2</sup></p>
<p>Date: August 28<sup>th</sup>, 2026</p>

<!-- Mark & Small -->
<p>Search result for <mark>HTML</mark> course.</p>
<p><small>&copy; 2026 Bhavishya. All rights reserved.</small></p>
```

---

## 6. Preserved Text (`<pre>`) & Inline Code (`<code>`)

### 1. Preserved Text (`<pre>`)
`<pre>` (Preformatted Text) tag HTML me **spaces, tabs, aur line breaks** ko EXACTLY waise hi preserve karta hai jaise aap code editor me likhte hain. Ye monospace font me display hota hai.

```html
<pre>
    Line 1
        Line 2 (indented)
    Line 3
</pre>
```

### 2. Inline Code (`<code>`)
`<code>` inline computer code snippet ko represent karta hai.

```html
<p>Use the <code>console.log()</code> method in JavaScript.</p>
```

### 3. Combining `<pre>` and `<code>` for Code Blocks
Multilines code snippet dikhane ke liye `<pre>` aur `<code>` ko mix karke use kiya jata hai:

```html
<pre><code>function greet() {
    console.log("Hello World!");
}</code></pre>
```

---

## 7. HTML Special Entities

HTML me kuch characters **Reserved Characters** hote hain kyunki browser unhe HTML tags samajhta hai (jaise `<` and `>`). Agar aapko text me literal `<` dikhana hai, to aapko **HTML Entity** use karni hogi.

### Why do we need Entities?
Agar aap HTML file me aise likhenge:
```html
<!-- ❌ Browser treats <p> as HTML tag! -->
<p>The syntax for paragraph is <p></p>
```
Browser confuse ho jayega! Correct way:
```html
<!-- ✅ Using HTML Entity for < and > -->
<p>The syntax for paragraph is &lt;p&gt;</p>
```

### Common HTML Entities Reference Table

| Character | Description | Entity Name | Entity Number | Example Usage |
|---|---|---|---|---|
| `<` | Less than | `&lt;` | `&#60;` | `&lt;div&gt;` |
| `>` | Greater than | `&gt;` | `&#62;` | `5 &gt; 3` |
| `&` | Ampersand | `&amp;` | `&#38;` | `Tom &amp; Jerry` |
| `"` | Double Quotation | `&quot;` | `&#34;` | `&quot;Hello&quot;` |
| `'` | Single Quote / Apostrophe | `&apos;` | `&#39;` | `It&apos;s clean` |
|   | Non-breaking space | `&nbsp;` | `&#160;` | `Word1&nbsp;Word2` |
| `©` | Copyright Symbol | `&copy;` | `&#169;` | `&copy; 2026` |
| `®` | Registered Trademark | `&reg;` | `&#174;` | `Brand&reg;` |
| `™` | Trademark Symbol | `&trade;` | `&#8482;` | `Product&trade;` |
| `₹` | Indian Rupee Symbol | `&#8377;` | `&#8377;` | `&#8377; 500` |
| `€` | Euro Symbol | `&euro;` | `&#8364;` | `&euro; 50` |

---

## 8. Text Accessibility & Screen Reader Mechanics

Screen readers visually impaired users ke liye web page text ko bol kar sunaate hain.

- **`<strong>` vs `<b>`**: Screen readers `<strong>` par thoda rukaav aur strong voice pitch use karte hain. `<b>` par normal reading tone hoti hai.
- **`<em>` vs `<i>`**: Screen readers `<em>` wale word par stress dete hain.
- **Heading Order**: Screen reader users keyboard shortcut (press `H`) daba kar heading-by-heading jump karte hain. Agar heading structure disorganized hai (`<h1>` → `<h4>`), to navigation kharab ho jata hai.

---

## 9. Common Beginner Mistakes to Avoid 🛑

1. ❌ **Using Multiple `<h1>` Tags**: Single page par 3-4 `<h1>` tags daalna (SEO rule violation).
2. ❌ **Skipping Heading Levels**: `<h1>` ke baad seedha `<h3>` ya `<h4>` par jump karna.
3. ❌ **Using `<br>` for Vertical Margins**: Paragraphs ke beech space ke liye `<br><br><br>` daalna.
4. ❌ **Using `<b>` and `<i>` everywhere**: Modern semantic HTML me `<strong>` aur `<em>` ko priority di jaati hai.
5. ❌ **Writing Raw Reserved Characters**: HTML code me direct `<script>` likhna instead of `&lt;script&gt;`.
6. ❌ **Underlining text with `<u>` for emphasis**: Users `<u>` (underline) text ko **clickable hyperlink** samajh kar click karne ki koshish karte hain.

---

## 10. Placement Interview Questions & Answers 🎯

### Q1: What is the difference between `<strong>` and `<b>` tags?
**Answer**: `<strong>` is a semantic tag that indicates that the text has high importance or seriousness; screen readers pronounce it with vocal emphasis and search engines weigh it heavily. `<b>` is a stylistic tag that bolds text for visual presentation without adding any semantic importance.

### Q2: What is the difference between `<em>` and `<i>` tags?
**Answer**: `<em>` represents semantic stress emphasis, altering the tone/meaning of the sentence. `<i>` represents text in an alternate tone, such as technical terms, foreign words, or idiomatic phrases, without stress emphasis.

### Q3: Why should a web page contain only one `<h1>` element?
**Answer**: Search engines use the single `<h1>` tag as the primary topic title of the page outline. Multiple `<h1>` tags confuse web crawlers and screen readers about the main document subject.

### Q4: What are HTML Entities and why are they needed?
**Answer**: HTML Entities are special character codes (e.g. `&lt;`, `&gt;`, `&amp;`) used to display reserved HTML characters or non-keyboard symbols. They prevent the browser from misinterpreting text like `<script>` as actual executable HTML code.

### Q5: What is the `<pre>` tag used for and how does it differ from `<p>`?
**Answer**: The `<pre>` (preformatted text) tag preserves all whitespace, tabs, and line breaks exactly as typed in code, rendering in monospace font. The `<p>` tag collapses multiple spaces/linebreaks into a single space.

---

## 11. Quick Revision Table ⚡

| Element | Category | Purpose | Example |
|---|---|---|---|
| `<h1>`-`<h6>` | Block / Semantic | Headings structure (H1 highest) | `<h1>Title</h1>` |
| `<p>` | Block / Content | Paragraph text block | `<p>Text...</p>` |
| `<br>` | Inline / Void | Single line break | `Text<br>More text` |
| `<hr>` | Block / Void | Horizontal section break line | `<hr>` |
| `<strong>` | Inline / Semantic | High importance text (bold) | `<strong>Important</strong>` |
| `<em>` | Inline / Semantic | Stress emphasis text (italic) | `<em>Must do</em>` |
| `<mark>` | Inline / Semantic | Highlighted text | `<mark>Match</mark>` |
| `<sub>` / `<sup>` | Inline / Format | Subscript / Superscript | `H<sub>2</sub>O`, `x<sup>2</sup>` |
| `<pre>` | Block / Format | Preserved whitespace & text | `<pre>Formatted</pre>` |
| `<code>` | Inline / Format | Computer code snippet | `<code>console.log()</code>` |
| `&lt;` / `&gt;` | Entity | Reserved `<` and `>` symbols | `&lt;html&gt;` |

---

*End of Unit 02 Notes. Open `example_01_headings_paragraphs.html` to run code!* 🚀
