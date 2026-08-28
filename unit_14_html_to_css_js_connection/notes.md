# Unit 14 — HTML → CSS, JS DOM & React Connection (Master Study Notes)

Welcome to **Unit 14: HTML → CSS, JS DOM & React Connection**! Is unit me hum HTML ke CSS styling, JavaScript DOM API, browser script loading timelines (`defer` vs `async`), aur React JSX component translation ke sath bridge ko detail me samjhenge.

---

## 1. Overview & Priority System

- ⭐⭐⭐ **Script Loading Execution Timeline (`defer` vs `async` vs Normal Script)**: MUST KNOW (Preventing render-blocking scripts).
- ⭐⭐⭐ **Connecting CSS (`<link>` vs `<style>` vs Inline Styles)**: MUST KNOW (External stylesheet integration & specificity priority).
- ⭐⭐⭐ **DOM Element Selection & Manipulation (`querySelector`, `addEventListener`)**: MUST KNOW (Bridge between HTML elements & JS objects).
- ⭐⭐⭐ **HTML to React JSX Translation Rules (`class` → `className`, `for` → `htmlFor`)**: MUST KNOW (MERN stack JSX mental model).

---

## 2. Connecting CSS to HTML ⭐⭐⭐

CSS ko HTML document me 3 tareeqon se link kiya ja sakta hai:

### 1. External Stylesheet (`<link rel="stylesheet">`) - BEST PRACTICE
```html
<head>
    <link rel="stylesheet" href="styles.css">
</head>
```
- **Why Best Practice?**: Caching allowed hai, clean separation of concerns, multi-page styling reuse.

### 2. Internal Stylesheet (`<style>`)
```html
<head>
    <style>
        body { background-color: #f4f4f4; }
    </style>
</head>
```

### 3. Inline Styles (`style="..."`)
```html
<h1 style="color: blue; font-size: 24px;">Inline Styled Heading</h1>
```
- **Highest CSS Specificity**: Overrides external and internal stylesheets (Anti-pattern for main styling).

---

## 3. Connecting JavaScript: `defer` vs `async` Attributes ⭐⭐⭐

Jab browser `<script src="app.js">` tag read karta hai, to HTML parsing ka kya hota hai? Ye `<script>` attributes par depend karta hai.

```
1. Normal <script src="app.js">:
   HTML Parsing ───► [ PAUSED / BLOCKED ] ───► HTML Resumes
                     Download & Execute Script

2. <script src="app.js" async>:
   HTML Parsing ───► [ PAUSED ] ───► HTML Resumes
   Async Download ──► Execute Immediately

3. <script src="app.js" defer>:
   HTML Parsing ──────────────────────────────────────► DOM Ready
   Parallel Download ─────────────────► Execute Script
```

### Breakdown Table:

| Script Tag | Download Behavior | Execution Time | Pauses HTML Parser? | Best Use Case |
|---|---|---|---|---|
| `<script src="app.js">` | Synchronous download | Immediately upon download | ❌ **YES (Render Blocking)** | Legacy scripts at body bottom |
| `<script src="app.js" async>` | Asynchronous download | Immediately when download completes | ❌ **YES** (Pauses HTML to execute) | Independent third-party scripts (Analytics, Ads) |
| `<script src="app.js" defer>` | Asynchronous download | **ONLY after HTML parsing completes** | ✅ **NO (Non-blocking)** | Main application JS manipulating DOM |

> ✅ **PRODUCTION BEST PRACTICE**: Main JavaScript files ko `<head>` me `<script src="app.js" defer></script>` likhna modern web standard hai!

---

## 4. HTML Elements to JavaScript DOM Nodes ⭐⭐⭐

Jab browser HTML parse karta hai, to HTML tags memory me **JS Objects (DOM Nodes)** me translate hote hain:

```html
<!-- HTML Source Markup -->
<button id="btn" class="primary-btn">Click Me</button>
```

```javascript
// JavaScript accessing the DOM node:
const buttonNode = document.querySelector("#btn");

// Reading DOM properties:
console.log(buttonNode.tagName);    // "BUTTON"
console.log(buttonNode.className);  // "primary-btn"

// Adding event listener:
buttonNode.addEventListener("click", () => {
    alert("Button clicked!");
});
```

---

## 5. HTML Markup to React JSX Translation Rules ⭐⭐⭐

React me HTML template string JSX syntax me likhi jaati hai. React JavaScript ke basis par chalta hai, isliye HTML syntax me 3 major changes hote hain:

### JSX Translation Rules:

| HTML Standard | React JSX Equivalent | Reason |
|---|---|---|
| `class="card"` | `className="card"` | `class` is a reserved keyword in JavaScript |
| `for="email"` | `htmlFor="email"` | `for` is a reserved loop keyword in JavaScript |
| `<br>`, `<img>`, `<input>` | `<br />`, `<img />`, `<input />` | **ALL JSX elements MUST be closed** (Self-closing required) |
| `style="color: blue;"` | `style={{ color: "blue" }}` | JSX `style` accepts a JavaScript object, not a CSS string |
| `onclick="fn()"` | `onClick={fn}` | CamelCase event handlers accepting function references |

### JSX Code Comparison Example:

```html
<!-- Standard HTML -->
<form class="login-box">
    <label for="usr">User:</label>
    <input type="text" id="usr" readonly>
    <br>
    <button onclick="submitData()">Submit</button>
</form>
```

```jsx
// React JSX Equivalent
return (
    <form className="login-box">
        <label htmlFor="usr">User:</label>
        <input type="text" id="usr" readOnly />
        <br />
        <button onClick={submitData}>Submit</button>
    </form>
);
```

---

## 6. Quick Revision Table ⚡

| Concept | Syntax | Key Behavior |
|---|---|---|
| Link External CSS | `<link rel="stylesheet" href="style.css">` | External stylesheet attachment |
| Script Defer | `<script src="app.js" defer>` | Downloads parallelly, executes after DOM ready |
| Script Async | `<script src="app.js" async>` | Downloads parallelly, executes immediately |
| DOM Selection | `document.querySelector("#id")` | Selects HTML DOM node via CSS selector |
| JSX Class | `className="name"` | React equivalent of HTML `class` |
| JSX Label Link | `htmlFor="id"` | React equivalent of HTML `for` |

---

## 7. Placement Must Know 🎯

1. `<script defer>` scripts download in parallel with HTML parsing and execute in exact order after the DOM is fully constructed.
2. `<script async>` scripts download in parallel but execute immediately upon download completion, potentially out-of-order.
3. In React JSX, `class` becomes `className` and `for` becomes `htmlFor` because `class` and `for` are reserved JS keywords.
4. Inline CSS styles (`style="..."`) carry the highest specificity overriding class and external stylesheets.
5. All void elements (like `<img>`, `<br>`, `<input>`) MUST be self-closed in React JSX (`<img />`, `<br />`).
