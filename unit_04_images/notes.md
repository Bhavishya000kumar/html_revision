# Unit 04 — Images & Media Basics (Master Study Notes)

Welcome to **Unit 04: Images & Media Basics**! Visuals web application ke user experience (UI/UX) ka ek major part hote hain. Is unit me hum `<img>` element, `src`, `alt`, image performance, Cumulative Layout Shift (CLS) prevention, modern image formats (SVG, WebP), aur semantic `<figure>` & `<figcaption>` elements ko detail me samjhenge.

---

## 1. Introduction to Images in HTML

HTML me images render karne ke liye `<img>` element use hota hai. 

- **Void Element**: `<img>` ek **void element (self-closing)** hai. Iska koi closing tag (`</img>`) nahi hota aur na hi iske andar koi text content hota hai.
- **Inline-Block Element**: Default display level par `<img>` ek inline-block element hai. Ye text line me sit karta hai lekin height aur width inspectable hoti hai.
- **External Asset Fetching**: Image content HTML file ke andar embed nahi rehta, balki browser `src` attribute se image file ko asynchronously fetch karta hai.

```html
<img src="logo.png" alt="Company Logo" width="200" height="50">
```

---

## 2. Essential Attributes of `<img>`

### 1. `src` (Source Path)
`src` (Source) image file ka URL ya relative file path specify karta hai.
- **Relative Path**: `src="images/banner.jpg"` or `src="../assets/logo.png"`
- **Absolute URL**: `src="https://example.com/photo.jpg"`
- **Data URI (Base64)**: `src="data:image/svg+xml;utf8,..."`

### 2. `alt` (Alternative Text)
`alt` text tab display hota hai jab image load nahi ho paati, aur screen readers ise padhte hain.

```html
<!-- Example with all core attributes -->
<img src="profile.jpg" alt="Bhavishya Kumar - Full Stack Developer Profile Photo" width="150" height="150">
```

---

## 3. Mastering the `alt` Attribute 🎯 (CRITICAL A11Y & SEO)

`alt` attribute sirf ek optional text nahi hai, ye web accessibility aur SEO ka core pilllar hai.

### Why is `alt` Text Crucial?
1. **Screen Reader Accessibility (a11y)**: Visually impaired users jab screen reader use karte hain, to screen reader `src` path nahi padhta, balki `alt` text padh kar image ka meaning batata hai.
2. **Broken Image Fallback**: Agar network slow ho, file delete ho gayi ho, ya path galat ho (404), to browser image placeholder ke sath `alt` text dikhata hai.
3. **Google Image Search (SEO)**: Search engine crawlers (Googlebot) images ko dekh nahi sakte. Wo `alt` text se image content aur page topic relevance samajhte hain.

### Decorative vs Informational Images:

| Image Type | Meaning | How to write `alt`? | Example |
|---|---|---|---|
| **Informational** | Content ka meaning clarify kar rahi hai (Profile photo, chart, product image) | Descriptive, concise sentence | `alt="Quarterly Sales Bar Chart 2026"` |
| **Decorative** | Purely visual decoration (background pattern, divider icon, decorative border) | Empty `alt=""` string | `alt=""` (Screen readers skipped silently) |

> 🛑 **Mistake to Avoid**: `alt="image"` ya `alt="photo"` likhna bilkul useless hai! `alt` text hamesha specific aur descriptive hona chahiye.

---

## 4. Image Dimensions & Layout Stability (Preventing CLS)

### What is Cumulative Layout Shift (CLS)?
Jab aap browser me webpage kholte hain aur page content upar-niche jump karta hai kyunki images late load ho kar jagah gherati hain, is layout jump ko **Cumulative Layout Shift (CLS)** kehte hain. Google PageSpeed insights me CLS ek major ranking metric hai.

```
WITHOUT width/height attributes:
[ Header Text ]
[ Text Paragraph ] 
  ↓ (Image loads late, pushes paragraph down violently!)
[ Image Renders ]
[ Text Paragraph ]
```

### How to Prevent CLS in HTML?
Always specify `width` and `height` attributes (in pixels, without `px` unit) on the `<img>` tag:

```html
<!-- ✅ CLS Prevention Best Practice -->
<img src="hero-banner.jpg" alt="Web Development Course Banner" width="800" height="400">
```

- Jab aap `width="800" height="400"` dete hain, to browser image load hone se pehle hi page par 800x400 aspect ratio ki **space reserve (allocate)** kar leta hai. Isse layout jump nahi hota!

---

## 5. Semantic Image Containers (`<figure>` & `<figcaption>`)

Legacy HTML me images aur captions ko `<div>` aur `<p>` me dala jata tha:

```html
<!-- ❌ Non-semantic legacy code -->
<div class="image-box">
    <img src="chart.png" alt="Sales Chart">
    <p>Figure 1: Sales Growth</p>
</div>
```

Modern HTML5 me semantic `<figure>` aur `<figcaption>` elements provide kiye gaye hain:

```html
<!-- ✅ Semantic HTML5 Figure Container -->
<figure>
    <img src="chart.png" alt="Bar chart showing 40 percent revenue growth in 2026" width="600" height="300">
    <figcaption>Figure 1: Revenue Growth Analysis for Q1 2026.</figcaption>
</figure>
```

### Why use `<figure>` and `<figcaption>`?
1. **Semantic Connection**: Browser aur screen readers ko pata chalta hai ki `<figcaption>` ka text seedhe usi image se related hai.
2. **Self-Contained Content**: Image + Caption ek single independent unit ki tarah behave karte hain jise document me kahin bhi move kiya ja sakta hai.

---

## 6. Web Image Formats Comparison & Selection Guide

Web development me right image format choose karna file size reduce karne ke liye zaroori hai.

### Formats Comparison Matrix

| Format | Full Name | Compression | Transparency (Alpha)? | Animation? | Scalable Vector? | Best Use Case |
|---|---|---|---|---|---|---|
| **JPG / JPEG** | Joint Photographic Experts Group | Lossy | ❌ No | ❌ No | ❌ No | Realistic photos, complex nature images |
| **PNG** | Portable Network Graphics | Lossless | ✅ Yes | ❌ No | ❌ No | Logos, icons with transparent background, screenshots |
| **WebP** | Web Picture Format (Google) | Lossy & Lossless | ✅ Yes | ✅ Yes | ❌ No | **Modern Web Standard**: Replaces JPG & PNG with 30% smaller file size |
| **SVG** | Scalable Vector Graphics | XML-based Vector | ✅ Yes | ✅ Yes | ✅ **Infinite** | Logos, icons, UI graphics (never gets pixelated!) |
| **GIF** | Graphics Interchange Format | Lossy | ✅ Yes | ✅ Yes | ❌ No | Short animated memes / simple low-color animations |

### SVG Code Example (XML-based Vector):
SVG images resolution-independent hoti hain (kisi bhi display resolution ya zoom par blurred nahi hoti).

```html
<!-- Inline SVG Code Example -->
<svg width="100" height="100">
    <circle cx="50" cy="50" r="40" fill="skyblue" stroke="navy" stroke-width="4" />
</svg>
```

---

## 7. Image Performance Optimization & Lazy Loading

### Native Lazy Loading (`loading="lazy"`)
Large web pages me 10-20 images ho sakti hain. Agar sabhi images ek sath load hongi to initial page load slow ho jayega.

HTML5 me **Native Lazy Loading** attribute introduce hua hai:

```html
<!-- Eager loading (Default): Loads image immediately -->
<img src="header-logo.png" alt="Logo" width="200" height="50" loading="eager">

<!-- Lazy loading: Loads image ONLY when user scrolls near it! -->
<img src="footer-photo.jpg" alt="Team Photo" width="600" height="400" loading="lazy">
```

### Best Practice Rules for `loading`:
1. **Above-the-Fold Images** (Hero banner, Navbar logo): Use `loading="eager"` (or omit `loading` attribute).
2. **Below-the-Fold Images** (Footer images, gallery items further down the page): Use `loading="lazy"`.

---

## 8. Clickable Image Links

Images ko clickable buttons ya banner links banane ke liye `<img>` tag ko `<a>` (Anchor) tag ke andar wrap kiya jata hai.

```html
<!-- Clickable Logo Link returning to Home Page -->
<a href="index.html" title="Return to Home Page">
    <img src="assets/logo.png" alt="Bhavishya Tech Home Logo" width="180" height="45">
</a>
```

---

## 9. Accessibility & Screen Reader Mechanics

- When a screen reader encounters `<img src="dog.jpg" alt="Golden Retriever playing fetch in grass">`, it announces:  
  *"Graphic: Golden Retriever playing fetch in grass"*.
- When a screen reader encounters `<img src="divider.png" alt="">`, it **completely skips** the decorative element, avoiding screen clutter for visually impaired users.

---

## 10. Common Beginner Mistakes to Avoid 🛑

1. ❌ **Omitting `alt` Attribute**: Validation error and bad accessibility.
2. ❌ **Omitting `width` and `height`**: Causes Cumulative Layout Shift (CLS) during page rendering.
3. ❌ **Writing Filename in `alt`**: `alt="DSC_0091.jpg"` or `alt="image.png"`.
4. ❌ **Using Heavy Uncompressed Images**: Uploading 10MB raw DSLR photos instead of 100KB WebP images.
5. ❌ **Broken Relative Paths**: Image subfolder path specify karne me `./images/` ki jagah galat path daalna.
6. ❌ **Using `<div>` with background-image for Content Images**: Background images screen readers read nahi kar pate aur SEO me index nahi hote. Content images ke liye hamesha HTML `<img>` use karein.

---

## 11. Placement Interview Questions & Answers 🎯

### Q1: What is Cumulative Layout Shift (CLS) and how do HTML image attributes help prevent it?
**Answer**: Cumulative Layout Shift (CLS) is a visual stability metric that measures unexpected layout jumps when page assets load late. Adding explicit `width` and `height` attributes to `<img>` tags allows the browser layout engine to calculate and reserve the aspect ratio space beforehand, preventing layout jumps when the image finishes downloading.

### Q2: What is the difference between `<figure>` and `<div>` for images?
**Answer**: `<figure>` is a semantic HTML5 element used to encapsulate self-contained media (images, diagrams, code blocks) along with an optional `<figcaption>` caption. A `<div>` is a generic non-semantic block container with no contextual relationship to its inner content.

### Q3: Why is WebP preferred over JPEG and PNG in modern web development?
**Answer**: WebP is a modern image format developed by Google that provides both lossy and lossless compression, transparency support, and animation capability, while yielding file sizes approximately 25%–35% smaller than comparable JPEG/PNG images without losing visual quality.

### Q4: When should you use `alt=""` (empty alt string)?
**Answer**: An empty `alt=""` attribute should be used on purely decorative images (background decorations, divider lines, decorative icons) so that screen readers skip announcing irrelevant graphics to visually impaired users.

### Q5: How does `loading="lazy"` improve web page performance?
**Answer**: `loading="lazy"` defers the loading of off-screen images until the user scrolls near their position in the viewport. This reduces initial page load time, bandwidth usage, and memory consumption.

---

## 12. Quick Revision Table ⚡

| Concept | Syntax | Primary Purpose |
|---|---|---|
| Image Tag | `<img src="path.jpg" alt="desc">` | Embeds image asset (Void element) |
| Alt Attribute | `alt="Descriptive text"` | Accessibility, broken fallback & SEO |
| Dimension Attributes | `width="800" height="400"` | Allocates aspect ratio space & prevents CLS |
| Semantic Figure | `<figure><img><figcaption>Cap</figcaption></figure>` | Semantic image container with caption |
| Lazy Loading | `<img ... loading="lazy">` | Defers loading of off-screen images |
| Clickable Image | `<a href="url"><img ...></a>` | Wraps image inside hyperlink |
| SVG Vector | `<svg>...</svg>` or `<img src="file.svg">` | Resolution-independent scalable vector graphic |

---

*End of Unit 04 Notes. Open `example_01_basic_images.html` to run code!* 🚀
