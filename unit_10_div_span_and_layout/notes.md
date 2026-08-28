# Unit 10 — Block vs Inline & Layout Skeletons (Master Study Notes)

Welcome to **Unit 10: Block vs Inline & Layout Skeletons**! Browser layout rendering mechanics me sabse core distinction **Block-level** aur **Inline-level** elements ke beech hota hai. Is unit me hum `<div>` vs `<span>`, CSS display level connection, aur HTML layout skeletons ko samjhenge.

---

## 1. Overview & Priority System

- ⭐⭐⭐ **Block vs Inline Display Mechanics**: MUST KNOW (Core browser box-model & flow layout).
- ⭐⭐⭐ **`<div>` vs `<span>`**: MUST KNOW (Generic Block Container vs Generic Inline Container).
- ⭐⭐⭐ **HTML Page Layout Skeleton**: MUST KNOW (Structuring web applications without CSS).
- ⭐⭐ **Document Flow & Display Levels**: Important (How browser stacks elements).

---

## 2. Block-Level vs Inline-Level Elements ⭐⭐⭐

Every HTML element has a default **display value** in the browser's User Agent Stylesheet.

### 1. Block-Level Elements (`display: block`)
- **Starts on a NEW Line**: Browser har block element ko naye line se render karta hai.
- **Takes 100% Width**: Available parent width ki 100% space occupy karta hai.
- **Can Contain Other Block & Inline Elements**: Block elements ke andar dusre block aur inline elements ho sakte hain.

#### Common Block Elements Examples:
`<div>`, `<p>`, `<h1>`-`<h6>`, `<ul>`, `<ol>`, `<li>`, `<table>`, `<form>`, `<header>`, `<main>`, `<section>`, `<article>`, `<footer>`, `<pre>`, `<fieldset>`.

### 2. Inline-Level Elements (`display: inline`)
- **Does NOT Start on a New Line**: Same line me adjacent elements ke sath sit karta hai.
- **Takes ONLY Content Width**: Jitni text/content ki length hai, utni hi width gherata hai.
- **Cannot Contain Block Elements**: Inline elements ke andar sirf dusre inline elements ya text reh sakte hain (Except `<a>` in HTML5).
- **Height & Width Cannot be Set**: CSS me pure inline element par `width` aur `height` ignore hoti hain.

#### Common Inline Elements Examples:
`<span>`, `<a>`, `<strong>`, `<em>`, `<b>`, `<i>`, `<mark>`, `<code>`, `<small>`, `<sub>`, `<sup>`, `<label>`.

### 3. Inline-Block Elements (`display: inline-block`)
Same line me sit karta hai (like Inline), lekin `width` aur `height` set ho sakti hain (like Block).  
*Examples*: `<img>`, `<input>`, `<button>`, `<select>`, `<textarea>`.

---

## 3. Generic Containers: `<div>` vs `<span>` ⭐⭐⭐

Jab kisi element ka **kohi semantic meaning nahi hota** aur container sirf CSS styling, layout wrapping, ya JavaScript targeting ke liye chahiye hota hai, tab generic containers use hote hain.

```
                   GENERIC CONTAINERS
                           │
        ┌──────────────────┴──────────────────┐
        ▼                                     ▼
   <div> (Block)                        <span> (Inline)
- Wraps block sections               - Wraps inline text words
- Takes 100% line width              - Takes only content width
- Starts on NEW line                 - Stays on SAME line
```

### 1. The `<div>` Element (Division / Block Container)
`<div>` ek **generic block-level container** hai. Iska koi semantic meaning nahi hota. Ye CSS Flexbox/Grid layouts me elements ko group karne ke liye use hota hai.

```html
<!-- Generic block card container -->
<div class="user-card">
    <h2>Bhavishya Kumar</h2>
    <p>Full Stack Developer</p>
</div>
```

### 2. The `<span>` Element (Inline Container)
`<span>` ek **generic inline container** hai. Ye text ke specific word/phrase ko group ya style karne ke liye use hota hai.

```html
<!-- Generic inline text wrapper -->
<p>Status: <span class="badge-active">Online</span></p>
```

---

## 4. Concept Comparisons & Decision Tree 🎯

### `<div>` vs `<span>` Comparison Table

| Feature | `<div>` (Block Container) | `<span>` (Inline Container) |
|---|---|---|
| **Default Display** | `display: block` | `display: inline` |
| **Line Behavior** | Starts on a **NEW Line** | Stays on the **SAME Line** |
| **Width Occupied** | **100% of Parent Width** | **Only Content Width** |
| **Width & Height CSS** | Respects `width` & `height` | Ignores `width` & `height` |
| **Can Contain Block Tags?**| ✅ YES | ❌ NO (Only inline content/text) |
| **Primary Use Case** | Layout wrapping, Grid/Flexbox cards | Styling single words inside paragraphs |

---

## 5. Pure HTML Page Layout Skeleton ⭐⭐⭐

A complete website layout skeleton structured semantically before applying CSS:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Application Layout Skeleton</title>
</head>
<body>

    <!-- Header & Navigation -->
    <header>
        <h1>Bhavishya App</h1>
        <nav>
            <a href="#">Home</a> | <a href="#">Dashboard</a>
        </nav>
    </header>

    <!-- Main Layout Wrapper (Div for layout grouping) -->
    <div class="layout-container">
        <!-- Sidebar Navigation -->
        <aside>
            <h3>Sidebar Menu</h3>
            <ul>
                <li>Profile</li>
                <li>Settings</li>
            </ul>
        </aside>

        <!-- Primary Page Content -->
        <main>
            <section>
                <h2>Welcome Back!</h2>
                <p>User status: <span class="status-active">Active</span></p>
            </section>
        </main>
    </div>

    <!-- Page Footer -->
    <footer>
        <p>&copy; 2026 Bhavishya App.</p>
    </footer>

</body>
</html>
```

---

## 6. MERN Stack & React Connection ⚛️

React me JSX rules HTML block-inline mechanics par depend karte hain:

```jsx
// React JSX requires a single parent wrapper!
// Div is commonly used as a layout wrapper container:
return (
    <div className="card-container">
        <h2>{user.name}</h2>
        <p>Role: <span>{user.role}</span></p>
    </div>
);
```

> 💡 **React Fragment (`<>...</>`)**: Modern React me unnecessary extra `<div>` elements avoid karne ke liye `<Fragment>` ya `<>` wrapper use kiya jata hai!

---

## 7. Quick Revision Table ⚡

| Concept | Display | Line Break | Width | Primary Purpose |
|---|---|---|---|---|
| `<div>` | `block` | Yes (New line) | 100% | Block layout container |
| `<span>` | `inline` | No (Same line) | Content width | Inline text wrapper |
| `<img>`, `<input>` | `inline-block` | No (Same line) | Resizable | Interactive widgets |
| `<p>`, `<h1>` | `block` | Yes (New line) | 100% | Text block elements |
| `<a>`, `<strong>` | `inline` | No (Same line) | Content width | Inline semantic text |

---

## 8. Placement Must Know 🎯

1. Block elements start on a new line and take 100% available width; Inline elements stay in the same line and take content width.
2. `<div>` is a generic block container; `<span>` is a generic inline container. Neither carries semantic meaning.
3. Pure inline elements (`<span>`, `<a>`, `<em>`) ignore `width` and `height` properties in CSS unless changed to `inline-block` or `block`.
4. Putting a block-level `<div>` inside a paragraph `<p>` is invalid HTML5 syntax.
5. In React development, overusing `<div>` wrappers is solved using React Fragments (`<React.Fragment>` or `<>...</>`).
