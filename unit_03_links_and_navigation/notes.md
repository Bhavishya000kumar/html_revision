# Unit 03 — Links & Navigation (Master Study Notes)

Welcome to **Unit 03: Links & Navigation**! HTML ka "HT" matlab **HyperText**, aur HyperText ka core element hai **Anchor Tag (`<a>`)**. Is unit me hum web pages ko interconnect karna, absolute vs relative paths, internal page anchors, security best practices, aur special link protocols ko detail me samjhenge.

---

## 1. Introduction to Hyperlinks in Web Architecture

Hyperlinks (Links) internet ki neev (foundation) hain. Ek hyperlink user ko:
1. Current page se kisi **dusre external website** par navigate karwa sakta hai.
2. Same website ke **kisi dusre page** (`about.html`, `contact.html`) par le ja sakta hai.
3. Same page ke kisi **part/section** par jump (scroll) karwa sakta hai.
4. Email client (`mailto:`), phone dialer (`tel:`), ya file download action trigger karwa sakta hai.

> 💡 **MERN Stack Connection**: React me jo aap `Link` component (`<Link to="/about">`) use karte hain, wo browser DOM level par compile ho kar yahi HTML `<a>` tag banta hai!

---

## 2. The Anchor Tag & Syntax

Anchor tag `<a>` is an **inline paired element**. Iska sabse main attribute **`href` (Hypertext Reference)** hota hai.

```html
<a href="destination_url">Link Display Text</a>
```

### Breakdown:
- **`<a>`**: Opening Anchor tag.
- **`href="..."`**: Attribute jo target URL ya path specify karta hai.
- **`Link Display Text`**: Screen par clickable text jo user ko dikhta hai.
- **`</a>`**: Closing Anchor tag.

```html
<!-- Basic Example -->
<a href="https://google.com">Visit Google</a>
```

---

## 3. Absolute vs Relative File Paths 🎯 (CRITICAL CONCEPT)

Beginners sabse zyada galati **File Paths** me karte hain. File path do type ke hote hain:

```
                          FILE PATH TYPES
                                │
        ┌───────────────────────┴───────────────────────┐
        ▼                                               ▼
  Absolute URL                                    Relative Path
(Full web address with protocol)             (Path relative to current file)
e.g. https://site.com/page.html              e.g. about.html, ../contact.html
```

### 1. Absolute URLs (External Web Links)
Absolute URL ek complete web address hota hai jisme protocol (`http://` ya `https://`), domain name, aur file path shamil hote hain.

```html
<!-- Absolute URL (External Link) -->
<a href="https://github.com/Bhavishya">View My GitHub Profile</a>
```

### 2. Relative File Paths (Internal Website Navigation)
Relative path aapke local project folder structure ke according decide hota hai. Ye is baat par depend karta hai ki **current HTML file kahan hai** aur **destination file kahan hai**.

#### Relative Path Rules & Notation:

| Symbol | Meaning | Example Path | Use Case |
|---|---|---|---|
| `filename.html` or `./filename.html` | Same Directory | `about.html` | File sibling level par same folder me hai |
| `folder/filename.html` | Child Subfolder | `pages/contact.html` | File current folder ke andar `pages` subfolder me hai |
| `../filename.html` | Parent Directory (One step UP) | `../index.html` | Parent folder me 1 level up jaane ke liye |
| `../../filename.html` | 2 Levels UP | `../../index.html` | Parent folder me 2 levels up jaane ke liye |
| `/filename.html` | Root Directory | `/index.html` | Domain ke exact root path se start hota hai |

#### Visual Folder Tree Example:

```
my-website/
├── index.html               <-- (File A)
├── pages/
│   ├── about.html           <-- (File B)
│   └── contact.html         <-- (File C)
└── assets/
    └── resume.pdf
```

- **From `index.html` (File A) to `about.html` (File B)**:
  `<a href="pages/about.html">About Us</a>`
- **From `about.html` (File B) to `index.html` (File A)** (One level UP):
  `<a href="../index.html">Home</a>`
- **From `about.html` (File B) to `contact.html` (File C)** (Same subfolder):
  `<a href="contact.html">Contact</a>`
- **From `about.html` (File B) to `resume.pdf`**:
  `<a href="../assets/resume.pdf">Download Resume</a>`

---

## 4. `target` Attribute & Window Behaviors

`target` attribute batata hai ki clicked link kahan open hogi.

```html
<a href="https://wikipedia.org" target="_blank">Open Wikipedia</a>
```

### Values of `target`:

| Value | Behavior | Default? |
|---|---|---|
| `_self` | Same browser tab / frame me open hota hai | Yes (Default) |
| `_blank` | **Naye browser tab** / new window me open hota hai | No |
| `_parent` | Parent frame me open hota hai (used in iframes) | No |
| `_top` | Full window body me top-level frame clear karke open hota hai | No |

### 🔒 CRITICAL SECURITY BEST PRACTICE: Tabnabbing Vulnerability & `rel="noopener noreferrer"`

Jab aap `target="_blank"` use karke naya tab kholte hain, to naya page `window.opener` JavaScript object ke zariye aapke original page par access pa sakta hai. Is security risk ko **Tabnabbing Attack** kehte hain.

#### ❌ Vulnerable Code:
```html
<!-- Dangerous Security Flaw -->
<a href="https://external-website.com" target="_blank">Visit External Site</a>
```

#### ✅ Secure Code:
```html
<!-- Secure Production Standard -->
<a href="https://external-website.com" target="_blank" rel="noopener noreferrer">Visit External Site</a>
```

- **`noopener`**: Naye page ko `window.opener` property dene se rokta hai.
- **`noreferrer`**: HTTP Referer header leak hone se bachata hai.

---

## 5. Page Anchors & Internal Navigation (`#id` Bookmarking)

Single-page websites me specific section par smooth jump karne ke liye **Page Anchors** use kiye jaate hain.

### How it works:
1. Target element ko ek unique `id` attribute dein (e.g. `<section id="contact-us">`).
2. Anchor link ke `href` attribute me `#` ke sath wo `id` likhein (e.g. `href="#contact-us"`).

```html
<!-- Navigation Links at top of page -->
<nav>
    <a href="#about">About</a> | 
    <a href="#projects">Projects</a> | 
    <a href="#contact">Contact</a>
</nav>

<!-- Page Content Sections -->
<section id="about">
    <h2>About Me</h2>
    <p>Details about developer...</p>
</section>

<section id="projects">
    <h2>My Projects</h2>
    <p>Details about projects...</p>
</section>

<section id="contact">
    <h2>Contact Us</h2>
    <p>Email form details...</p>
</section>

<!-- Jump to Top Link -->
<a href="#">Back to Top ⬆</a>
```

---

## 6. Special Protocol Links

Browser standard web pages ke alawa special URI schemes ko treat karna janta hai:

### 1. Email Links (`mailto:`)
Default email client (like Gmail, Outlook) ko mail composer ke sath open karta hai.

```html
<!-- Basic Email Link -->
<a href="mailto:support@bhavishya.com">Send Email</a>

<!-- Email Link with Pre-filled Subject and Body -->
<a href="mailto:support@bhavishya.com?subject=Inquiry%20About%20Course&body=Hello%20Team,">
    Email Support Team
</a>
```

### 2. Telephone Links (`tel:`)
Mobile devices par Phone Dialer open karta hai.

```html
<a href="tel:+919876543210">Call Us: +91 9876543210</a>
```

### 3. SMS Links (`sms:`)
Messaging app trigger karta hai.

```html
<a href="sms:+919876543210">Send SMS</a>
```

### 4. File Download Attribute (`download`)
Browser me PDF/Image open karne ke bajaye user ki device me direct **Download Action** force karta hai.

```html
<!-- Forces browser to download the file -->
<a href="assets/sample_resume.pdf" download="Bhavishya_Resume.pdf">
    Download Official Resume (PDF)
</a>
```

---

## 7. Link Tooltips & SEO Rel Attributes

### 1. `title` Attribute
Mouse hover karne par browser tooltip message dikhata hai.

```html
<a href="https://react.dev" title="Official React Documentation Website">React Docs</a>
```

### 2. SEO Links & `rel="nofollow"`
Search Engine Crawlers ko link follow na karne ke liye instructions deta hai (paid links / untrusted user-generated links ke liye).

```html
<a href="https://untrusted-forum.com" rel="nofollow">User Link</a>
```

---

## 8. Web Accessibility (a11y) & SEO in Links

Screen Readers user ko link tabulate karke batate hain.

### 🛑 BAD vs ✅ GOOD Accessible Link Text:

- ❌ **BAD**: `<a href="about.html">Click Here</a>` to read about us.
- ❌ **BAD**: Read more about our course `<a href="course.html">Here</a>`.
- ✅ **GOOD**: Read our complete <a href="course.html">Full Stack Web Development Syllabus</a>.

### Why generic "Click Here" text is bad:
1. **Screen Reader Failure**: Screen reader jab links ki list padhta hai, to usko sirf "Click Here, Click Here, Click Here" sunaai deta hai, bina kisi context ke.
2. **SEO Penalty**: Google Search Engine link text (Anchor Text) se destination page ki relevance judge karta hai.

---

## 9. Common Beginner Mistakes to Avoid 🛑

1. ❌ **404 Broken Links due to Wrong Paths**: Relative path me `./` ya `../` misconfigure kar dena.
2. ❌ **Forgetting `rel="noopener noreferrer"` with `target="_blank"`**: Security vulnerability chodh dena.
3. ❌ **Using Generic "Click Here" Anchor Text**: Accessibility aur SEO loss.
4. ❌ **Forgetting `#` in Internal Page Anchors**: `<a href="contact">` write karna instead of `<a href="#contact">`.
5. ❌ **Forgetting `mailto:` or `tel:` Protocols**: Direct email address path me likhna `<a href="bhavishya@gmail.com">`.
6. ❌ **Unclosed Anchor Tags**: `<a>` tag close na karne par poora page clickable link ban jaata hai!

---

## 10. Placement Interview Questions & Answers 🎯

### Q1: What is Tabnabbing vulnerability and how does HTML prevent it?
**Answer**: Tabnabbing is a phishing attack where a newly opened tab (`target="_blank"`) accesses the original tab via `window.opener.location` to redirect the user to a fake malicious page. HTML prevents this by adding `rel="noopener noreferrer"` to external links opening in new tabs.

### Q2: Explain the difference between `href="page.html"`, `href="./page.html"`, and `href="../page.html"`.
**Answer**: 
- `href="page.html"` and `href="./page.html"` reference a file in the **same directory** as the current document.
- `href="../page.html"` moves **one directory up** (parent folder) to locate `page.html`.

### Q3: How do you create an internal page jump link to a specific section?
**Answer**: Give the target section element a unique `id` attribute (e.g. `<section id="pricing">`), and set the anchor link `href` attribute to `#pricing` (`<a href="#pricing">Go to Pricing</a>`).

### Q4: Why is using "Click Here" as link text considered bad practice?
**Answer**: It violates Web Accessibility (a11y) standards because screen readers listing links out of context cannot infer the destination. It also harms SEO because search engine crawlers rely on descriptive anchor text to index destination page relevance.

### Q5: How do you trigger an email composer or phone dialer in HTML?
**Answer**: Use the `mailto:` scheme for emails (`<a href="mailto:user@site.com">`) and the `tel:` scheme for phone numbers (`<a href="tel:+919876543210">`).

---

## 11. Quick Revision Table ⚡

| Concept | Syntax / Tag | Primary Purpose |
|---|---|---|
| External Link | `<a href="https://site.com" target="_blank" rel="noopener noreferrer">` | Opens external site safely in new tab |
| Same Directory Relative | `<a href="about.html">` | Navigates to file in same folder |
| Parent Directory Relative | `<a href="../index.html">` | Navigates to file 1 directory level UP |
| Child Directory Relative | `<a href="pages/contact.html">` | Navigates to file in subfolder |
| Page Anchor Bookmark | `<a href="#contact">` $\rightarrow$ `<section id="contact">` | Jumps to section on same page |
| Email Link | `<a href="mailto:name@site.com">` | Opens device default email composer |
| Phone Dialer | `<a href="tel:+919876543210">` | Opens phone dialer on mobile |
| File Download | `<a href="file.pdf" download="Name.pdf">` | Forces direct file download |

---

*End of Unit 03 Notes. Open `example_01_basic_links.html` to run code!* 🚀
