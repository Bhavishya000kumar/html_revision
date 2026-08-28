# Unit 01 — HTML Basics (Master Study Notes)

Welcome to **Unit 01: HTML Basics**! Ye notes aapko HTML ka solid foundation samjhane ke liye banaye gaye hain. Isme har concept ko simple Hinglish me, line-by-line breakdown aur technical accuracy ke saath explain kiya gaya hai.

---

## 1. What is HTML?

### Full Form
**HTML** ka full form hai **HyperText Markup Language**.

- **HyperText**: HyperText ka matlab wo text jo dusre pages ya documents se linked ho (via links/hyperlinks). Web par ek page se dusre page par jump karna HyperText ki wajah se possible hota hai.
- **Markup**: Markup ka matlab hota hai text ko "mark" karna ya annotate karna tags (`<tag>`) ka use karke, taaki browser ko pata chale ki kaun sa text **heading** hai, kaun sa **paragraph** hai, aur kaun sa **image** hai.
- **Language**: Ye ek markup language hai (programming language nahi hai).

### What HTML Does
1. Webpage ka **structure** (ढांचा / Skeleton) banata hai.
2. Content ka **meaning / role** define karta hai (jaise ye text Heading hai ya Paragraph).
3. Text, images, videos, tables, aur forms ko document me arrange karta hai.

### What HTML Does NOT Do
- HTML me programming logic nahi hoti (no loops, no variables, no functions, no condition logic like `if/else`).
- HTML webpage ko beautiful styling nahi deta (wo kaam **CSS** ka hai).
- HTML webpage me dynamic behaviour ya interactive features create nahi karta (wo kaam **JavaScript** ka hai).

### HTML vs CSS vs JavaScript (Real-Life Analogy)

| Technology | Role | Real-Life Analogy (Human Body) | Real-Life Analogy (Car) |
|---|---|---|---|
| **HTML** | Structure & Content | **Skeleton (Haddiyan)** | **Car Chassis & Metal Frame** |
| **CSS** | Styling & Appearance | **Skin, Hair, Clothes, Color** | **Car Paint, Interior Design, Leather Seats** |
| **JavaScript** | Logic & Behaviour | **Brain, Muscles, Movement** | **Car Engine, Steering, Brakes, Acceleration** |

---

## 2. How Browser Understands HTML

Jab aap Chrome, Firefox, ya Edge me koi web page kholte hain, to background me browser ye steps follow karta hai:

```
[ HTML File (.html) ] 
        ↓
  1. Network Request / Local File Read
        ↓
  2. HTML Parsing (Tokens & Nodes creation)
        ↓
  3. DOM Tree Construction (Document Object Model)
        ↓
  4. CSSOM & Render Tree Construction
        ↓
  5. Layout & Painting on Screen
```

### Breakdown of Steps:
1. **Reading File**: Browser `.html` file ke plain text code ko read karta hai.
2. **Parsing**: Browser code ko line-by-line analyze karta hai aur tags ko identify karta hai.
3. **DOM Construction**: Browser HTML elements ka ek tree structure banata hai jise **DOM (Document Object Model)** kehte hain.
4. **Rendering**: Browser screen par visible content ko draw (paint) kar deta hai.

> 💡 **JS Connection**: Aapne JavaScript me jo `document.getElementById()` padha hai, wo isi **DOM Tree** ke nodes ko select karne ke liye use hota hai!

---

## 3. HTML Document Structure

Ek standard HTML5 document ka complete skeleton aisi dikhti hai:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My First Webpage</title>
</head>
<body>
    <h1>Welcome to My Webpage</h1>
    <p>This is my first line of HTML code!</p>
</body>
</html>
```

### Line-by-Line Breakdown Table

| Code Line | Name | Role & Explanation | What happens if Missing? |
|---|---|---|---|
| `<!DOCTYPE html>` | DOCTYPE Declaration | Browser ko batata hai ki ye **HTML5** document hai. | Browser **Quirks Mode** me chala ja sakta hai aur web standard breach ho sakta hai. |
| `<html lang="en">` | Root Element | Pure HTML document ka container hai. `lang="en"` browser & screen reader ko batata hai ki language English hai. | Browser default language assume karega, SEO aur accessibility affect hogi. |
| `<head>` | Document Header | Isme document ki metadata, title, charsets, external CSS/JS links hote hain jo screen par seedhe render nahi hote. | Browser document metadata read nahi kar payega, page title blank dikhega. |
| `<meta charset="UTF-8">` | Character Encoding | World ke almost sare characters & symbols (Hindi, Emoji, English) ko browser me correctly display karta hai. | Unreadable symbols (junk characters ``) screen par dikh sakte hain. |
| `<meta name="viewport"...>` | Mobile Viewport Meta | Mobile screens par page ko properly scale aur responsive banata hai. | Mobile devices par page desktop size me zoomed-out dikhega. |
| `<title>...</title>` | Page Title | Browser Tab par jo title text dikhta hai, wo yahan set hota hai. | Browser tab par file path ya `Untitled` dikhega. |
| `<body>` | Document Body | Screen par jitna bhi visible content (Headings, Paragraphs, Images, Forms) dikhta hai, wo body ke andar rehta hai. | Screen bilkul blank dikhegi. |

---

## 4. The DOCTYPE Declaration

```html
<!DOCTYPE html>
```

### Key Points:
1. **Meaning**: Ye browser ko batata hai ki page HTML ke konse version me likha gaya hai. `<!DOCTYPE html>` ka matlab hai **HTML5** (current modern standard).
2. **Case Insensitive**: Aap `<!DOCTYPE html>`, `<!doctype html>`, ya `<!DocType html>` likh sakte hain, lekin standard convention uppercase `<!DOCTYPE html>` hai.
3. **MISCONCEPTION ALERT 🚨**: `<!DOCTYPE html>` koi **HTML tag nahi hai**! Ye ek instruction (declaration) hai jo document ki sabse pehli line (Line 1) par aati hai.

---

## 5. The html Element

```html
<html lang="en">
    <!-- Everything in your webpage sits here -->
</html>
```

- **Root Element**: `<html>` pure document ka root container element hota hai. `<!DOCTYPE html>` ke elawa baki saare tags `<html>` ke andar hi aate hain.
- **`lang` Attribute**: `lang="en"` batata hai ki page English language me hai. Agar aap Hindi me page bana rahe hain to `lang="hi"` likh sakte hain.

---

## 6. The head Element

```html
<head>
    <meta charset="UTF-8">
    <title>My Portfolio</title>
</head>
```

### What belongs inside `<head>`?
- `<title>`: Tab name set karne ke liye.
- `<meta>`: Page info, character set, responsive settings, SEO descriptions.
- `<link>`: External CSS file attach karne ke liye (introduced later).
- `<script>`: JavaScript file connect karne ke liye (introduced later).

### Crucial Difference: `<head>` vs `<body>`
- **`<head>`**: Information **ABOUT** the document (Behind the scenes info). Visible webpage area par display nahi hota.
- **`<body>`**: Information **IN** the document. Jo kuch bhi screen par user ko dikhana hai, wo sirf `<body>` me aayega.

---

## 7. The body Element

```html
<body>
    <h1>Main Heading</h1>
    <p>This is a paragraph inside the body tag.</p>
</body>
```

- Screen par dikhne wala 100% content (`<h1>`, `<p>`, `<a>`, `<img>`, `<table>`, `<form>`) hamesha `<body>` tag ke andar rehta hai.
- Ek HTML document me sirf **EK HI `<body>` element** ho sakta hai.

---

## 8. HTML Tags vs Elements

Boht se beginners Tags aur Elements ke beech me confuse ho jaate hain. Dono me clear difference hai:

```
    ┌────────────────────── HTML ELEMENT ──────────────────────┐
    │                                                          │
   <h1>              Welcome to My Website                  </h1>
  └────┘            └─────────────────────┘                └─────┘
 Opening Tag                Content                       Closing Tag
```

### Definitions:
- **HTML Tag**: Angle brackets `< >` ke andar wala text. (e.g., `<h1>` is opening tag, `</h1>` is closing tag).
- **HTML Element**: Opening tag + Content + Closing tag ko mila kar poora **HTML Element** banta hai.

### Quick Example:
- `<h1>` → Tag
- `<h1>Hello World</h1>` → Complete HTML Element

---

## 9. Opening, Closing, and Void Tags

### 1. Paired Elements (Regular Elements)
Most HTML elements paired hote hain. Inka ek opening tag aur ek closing tag hota hai, jiske beech me content aata hai:

```html
<p>This is content inside paragraph element.</p>
```
Closing tag me hamesha aage slash `/` hota hai (`</p>`).

### 2. Void Elements (Self-Closing Tags)
Kuch elements aise hote hain jinke andar koi text content nahi hota. Isliye inka **koi closing tag nahi hota**. Inhe **Void Elements** ya **Self-Closing Elements** kehte hain.

#### Common Void Elements Examples:
- `<br>` : Line break ke liye
- `<hr>` : Horizontal line rule ke liye
- `<img>` : Image embed karne ke liye
- `<meta>` : Metadata ke liye
- `<link>` : External file link karne ke liye
- `<input>` : Form input box ke liye

```html
<!-- Void elements do NOT have closing tags -->
<br>
<hr>
<img src="logo.png" alt="Company Logo">
```
*Note*: HTML5 me `<br>` ya `<br />` dono valid hain, lekin clean HTML5 style me simple `<br>` likha jata hai.

---

## 10. Nested Elements (Parent-Child Hierarchy)

HTML elements ko ek dusre ke andar put kiya ja sakta hai. Is process ko **Nesting** kehte hain.

```html
<body>
    <div>
        <h1>Article Title</h1>
        <p>This paragraph is inside a div element.</p>
    </div>
</body>
```

### Tree Relationship Terms:
- `<body>` is the **Parent** of `<div>`.
- `<div>` is the **Child** of `<body>`.
- `<h1>` and `<p>` are **Children** of `<div>`.
- `<h1>` and `<p>` are **Siblings** (kyunki dono ka parent same `<div>` hai).

### ⚠️ Golden Rule of Nesting:
Elements ko **Correct Order (LIFO - Last In First Out)** me close karna zaroori hai!

```html
<!-- ✅ CORRECT Nesting -->
<p>This is <strong>important text</strong> here.</p>

<!-- ❌ INCORRECT Nesting (Overlapping) -->
<p>This is <strong>important text</p></strong>
```

---

## 11. HTML Attributes

Attributes HTML elements ko **extra information / properties** provide karte hain. Attributes hamesha **Opening Tag** ke andar likhe jaate hain.

### Syntax:
```html
<elementname attributename="attributevalue">Content</elementname>
```

### Example:
```html
<a href="https://google.com" target="_blank" title="Go to Google">Click Here</a>
```
Here:
- `href` is an attribute name, `"https://google.com"` is its value.
- `target` is an attribute name, `"_blank"` is its value.
- `title` is an attribute name, `"Go to Google"` is its value.

### Important Global Attributes Introduced in Unit 01:
1. `id`: Element ki unique identity set karne ke liye (JS selection me use hota hai).
2. `class`: Grouping elements ke liye (CSS styling & JS selection me use hota hai).
3. `lang`: Element ki language specify karne ke liye.
4. `title`: Mouse hover karne par tooltip dikhane ke liye.
5. `hidden`: Element ko screen par hide karne ke liye.

---

## 12. HTML Comments

Comments wo lines hoti hain jise browser parse karta hai lekin screen par render nahi karta. Ye developers ke samajhne ke liye hoti hain.

### Syntax:
```html
<!-- This is a single-line comment -->

<!-- 
    This is a 
    multi-line comment
    in HTML
-->
```

### Why use comments?
- Code ki readable explanation ke liye.
- Temporarily kisi code segment ko disable karne ke liye.
- Team members ke sath collaboration easy banane ke liye.

---

## 13. Basic Metadata

Metadata ka matlab hota hai **"Data about Data"**. HTML document ka metadata `<head>` section me rehata hai.

### Essential Metadata Tags:
1. **Title**:
   ```html
   <title>My Portfolio | Bhavishya</title>
   ```
2. **Character Set (`charset`)**:
   ```html
   <meta charset="UTF-8">
   ```
   `UTF-8` covers almost all written characters, emojis, and symbols in the world.
3. **Viewport Setting**:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```
   Batata hai ki mobile screen width ke hisab se webpage adjust hoga.

---

## 14. HTML File Creation and Execution

### Step-by-Step Practical Workflow:

1. **Create File**: Naya file banayein jiska extension `.html` ho (e.g., `index.html`).
2. **Write HTML Code**: HTML5 standard skeleton code likhein.
3. **Save File**: `Ctrl + S` daba kar save karein.
4. **Open in Browser**: File par double click karein ya Chrome me drag & drop karein.
5. **Inspect with DevTools**:
   - Webpage par `Right Click → Inspect` karein (Ya `F12` dabayein).
   - **Elements** tab par jayein.
   - Aap dekhenge ki browser ne aapke HTML tags se exact **DOM Tree** create kar di hai!

### Using VS Code + Live Server Extension:
- VS Code me `Emmet Shortcut`: Empty file me `!` dabayein aur `Tab` dabayein. HTML5 skeleton auto-generate ho jayegi!
- File par Right Click karein → **"Open with Live Server"**. Auto-reload enabled web view open ho jayega.

---

## 15. JavaScript & DOM Connection

Aapne JavaScript me DOM selection padha hoga:

```javascript
// JavaScript selecting an HTML element via its ID attribute
const heading = document.getElementById("main-heading");
console.log(heading.innerText);
```

### Behind the Scenes:
1. Jab browser `<h1 id="main-heading">Hello</h1>` HTML line dekhta hai, to wo memory me ek **DOM Node Object** create karta hai.
2. JavaScript `document.getElementById("main-heading")` call karke isi DOM node object par action karti hai!
3. HTML = Structure, CSS = Style, JS = DOM node properties modify karne wala logic.

---

## 16. Common Beginner Mistakes to Avoid 🛑

1. ❌ **Forgetting `<!DOCTYPE html>`**: Quirks mode trigger kar deta hai.
2. ❌ **Putting visible tags inside `<head>`**: `<h1>` ya `<p>` ko `<head>` me mat daaliye, ye galat hai. Visible content hamesha `<body>` me jayega.
3. ❌ **Incorrect Tag Nesting**: Overlapping closing tags (`<p><b>text</p></b>`).
4. ❌ **Forgetting Closing Tags**: Paired tags (jaise `<p>`, `<h1>`) ko close na karna rendering bugs create kar sakta hai.
5. ❌ **Confusing Tags and Attributes**: `<id="test">` likhna galat hai. Correct: `<h1 id="test">`.
6. ❌ **Wrong File Extension**: File ko `index.html.txt` save kar dena. Double check extension `.html` hona chahiye.
7. ❌ **Unclosed Quote Marks in Attributes**: `<a href="google.com>` (closing quote missing).
8. ❌ **Using Spaces in File Names**: File ka naam `my first page.html` na rakhein, `my_first_page.html` ya `my-first-page.html` use karein.

---

## 17. Interview / Placement Points 🎯

### Q1: What is HTML and why is `<!DOCTYPE html>` required?
**Answer**: HTML (HyperText Markup Language) is the standard markup language used to structure web pages. `<!DOCTYPE html>` is an instruction to the browser that informs it that the document is written in modern **HTML5**, preventing the browser from rendering the page in legacy "Quirks Mode".

### Q2: What is the difference between an HTML Tag and an HTML Element?
**Answer**: An HTML **Tag** refers to the syntax markers enclosed in angle brackets like `<h1>` or `</h1>`. An HTML **Element** includes the opening tag, the content inside, and the closing tag altogether (e.g. `<h1>Hello World</h1>`).

### Q3: What are Void Elements? Give 3 examples.
**Answer**: Void elements (also called self-closing elements) are elements that cannot contain any text content or child elements. Therefore, they do not have a closing tag. Examples: `<img>`, `<br>`, `<hr>`, `<meta>`, `<input>`.

### Q4: What is the difference between `<head>` and `<body>` tags?
**Answer**: `<head>` contains metadata, title, character encoding, and external script/stylesheet links that are NOT directly rendered in the visible viewport area. `<body>` contains all the visible content (headings, paragraphs, images, forms) shown to the user.

### Q5: What is the purpose of the `lang` attribute in `<html>` tag?
**Answer**: The `lang` attribute specifies the primary language of the HTML document (e.g., `lang="en"`). It helps search engines (SEO) and screen readers (accessibility) parse text pronunciation correctly.

### Q6: Can we invent custom tags like `<mycustomtag>` in HTML?
**Answer**: Standard HTML browsers will treat unrecognized tags as generic inline elements, but it is invalid HTML5 syntax unless defined as a Web Component via Custom Elements API in JavaScript.

---

## 18. Quick Revision Table ⚡

| Concept | Syntax / Marker | Key Purpose |
|---|---|---|
| DOCTYPE | `<!DOCTYPE html>` | Tells browser the document is HTML5 |
| Root Tag | `<html lang="en">` | Encloses entire HTML document |
| Metadata Container | `<head>` | Holds title, meta, scripts, styles |
| Visible Area | `<body>` | Holds visible webpage elements |
| Page Tab Title | `<title>Title Text</title>` | Displays title on browser tab |
| Tag vs Element | Tag: `<h1>` \| Element: `<h1>Hi</h1>` | Tag is markup; Element is Tag + Content |
| Void Element | `<br>`, `<hr>`, `<img>` | Elements without closing tags or inner content |
| Attributes | `<tag attr="value">` | Extra properties written inside opening tag |
| Comments | `<!-- Comment text -->` | Ignored by browser rendering engine |

---

*End of Unit 01 Notes. Now open and run `example_01_skeleton.html`!* 🚀
