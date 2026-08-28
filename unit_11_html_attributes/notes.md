# Unit 11 — Global Attributes & Data Attributes (Master Study Notes)

Welcome to **Unit 11: Global Attributes & Data Attributes**! Attributes HTML elements ko extra properties aur identification provide karte hain. Is unit me hum Core **Global Attributes** (`id`, `class`, `style`, `title`, `tabindex`, `hidden`) aur Custom **Data Attributes** (`data-*`) ko detail me samjhenge.

---

## 1. Overview & Priority System

- ⭐⭐⭐ **Global Attributes (`id`, `class`, `title`, `hidden`, `tabindex`)**: MUST KNOW (Core element identification & accessibility).
- ⭐⭐⭐ **Custom Data Attributes (`data-*`)**: MUST KNOW (Passing custom data from HTML to JavaScript DOM `dataset`).
- ⭐⭐⭐ **HTML Attributes vs DOM Properties**: MUST KNOW (Top JavaScript DOM placement interview question).
- ⭐⭐ **Boolean Attributes**: Important (`disabled`, `required`, `checked`, `hidden`).

---

## 2. Core Global Attributes ⭐⭐⭐

**Global Attributes** wo attributes hain jo **HTML ke HAR element par valid hote hain** (chahe `<h1>` ho, `<div>`, `<p>`, ya `<a>`).

### 1. `id` (Unique Identifier)
- Document me element ko **Unique Identity** deta hai.
- **Rule**: Entire HTML page par ek `id` value **sirf EK element** ki ho sakti hai (No duplicates!).
- **Usage**: JavaScript selection (`document.getElementById("user-card")`), CSS ID selectors (`#user-card`), and Page Anchors (`href="#user-card"`).

### 2. `class` (Group Classifier)
- Elements ko category ya group me assign karta hai.
- **Rule**: Multiple elements ka `class` name **SAME** ho sakta hai, aur ek element par **multiple classes** (`class="card active primary"`) space se separate karke di ja sakti hain.
- **Usage**: CSS Styling (`.card`) & JS Selection (`querySelectorAll(".card")`).

### 3. `title` (Tooltip Text)
- Element par mouse hover karne par native browser tooltip popup display karta hai.

### 4. `hidden` (Boolean Hidden State)
- Element ko browser viewport se completely hide kar deta hai (Equivalent to CSS `display: none`).

```html
<!-- Element hidden from viewport -->
<p hidden>This paragraph is invisible on screen.</p>
```

### 5. `tabindex` (Keyboard Focus Navigation)
- Keyboard `Tab` key navigation order control karta hai.
- `tabindex="0"`: Non-interactive element (e.g. `<div>`) ko keyboard focusable banata hai.
- `tabindex="-1"`: Element ko Tab order se remove kar deta hai (Programmatic JS focus only).
- `tabindex="1+"`: Custom tab order force karta hai (Anti-pattern! Avoid positive values).

---

## 3. Custom Data Attributes (`data-*`) ⭐⭐⭐

HTML5 me developers ko HTML elements me **custom data store karne** ka feature mila jise **Data Attributes** kehte hain.

### Syntax
Data attribute ka prefix hamesha `data-` se start hota hai, followed by lowercase name:

```html
<div class="user-profile" data-user-id="usr_98765" data-role="admin" data-is-premium="true">
    <h3>Bhavishya Kumar</h3>
</div>
```

### How JavaScript Reads `data-*` Attributes (`element.dataset`)
JavaScript DOM me `data-*` attributes **`element.dataset`** object me CamelCase property key ke roop me map hote hain:

```javascript
// Selecting the element in JavaScript
const userCard = document.querySelector(".user-profile");

// Reading data attributes via dataset object:
console.log(userCard.dataset.userId);    // Output: "usr_98765"
console.log(userCard.dataset.role);      // Output: "admin"
console.log(userCard.dataset.isPremium); // Output: "true"

// Modifying data attribute dynamically:
userCard.dataset.role = "super-admin";
```

### Real-World Usage of `data-*`
1. **E-Commerce Shopping Carts**: Storing Product ID and Price on Add-to-Cart buttons (`data-product-id="101" data-price="999"`).
2. **Dynamic UI Filtering**: Filtering items by category (`data-category="electronics"`).
3. **Modal Popups**: Storing target modal ID (`data-modal-target="#login-modal"`).

---

## 4. Concept Comparisons & Decision Tree 🎯

### 1. `id` vs `class`

| Feature | `id` Attribute | `class` Attribute |
|---|---|---|
| **Uniqueness** | **Must be UNIQUE** per page | Can be reused across multiple elements |
| **Multiple Values?** | ❌ No (Single ID string) | ✅ Yes (`class="btn btn-primary active"`) |
| **CSS Selector** | `#my-id` | `.my-class` |
| **JS Method** | `document.getElementById("id")` | `document.getElementsByClassName("class")` |

### 2. HTML Attribute vs DOM Property (CRITICAL DOM INTERVIEW QUESTION)

```
HTML Source Code (Markup)             Browser Memory (Live JS DOM)
┌─────────────────────────────┐       ┌─────────────────────────────┐
│  <input id="usr" value="A"> │ ───►  │ HTMLInputElement Object     │
└─────────────────────────────┘       │  id: "usr"                  │
                                      │  value: "B" (User typed B)  │
                                      └─────────────────────────────┘
```

| Aspect | HTML Attribute | DOM Property |
|---|---|---|
| **Definition** | Written in HTML source markup | Property of live JavaScript DOM object |
| **Initialization** | Initializes DOM property default value | Represents live current state in memory |
| **Change Behavior** | Static (Doesn't change when user types) | Dynamic (Updates live when user types text) |
| **Access Method** | `element.getAttribute("value")` | `element.value` |

---

## 5. MERN Stack & React Connection ⚛️

React JSX me HTML attributes JavaScript properties me convert hote hain:

```jsx
// React JSX Attribute Naming Conventions:
// class -> className
// for -> htmlFor
// data-* remains data-*

return (
    <div 
        className="card-container" 
        id="user-101" 
        data-user-id={user.id} 
        hidden={!user.isActive}
    >
        <h3>{user.name}</h3>
    </div>
);
```

---

## 6. Quick Revision Table ⚡

| Attribute | Category | Syntax | Purpose |
|---|---|---|---|
| `id` | Global | `id="unique-id"` | Unique element identifier |
| `class` | Global | `class="c1 c2"` | CSS styling & group selection |
| `title` | Global | `title="Tooltip"` | Hover tooltip pop-up |
| `hidden` | Global Boolean | `<p hidden>` | Hides element from viewport |
| `tabindex` | Global | `tabindex="0"` | Keyboard focus navigation |
| `data-*` | Custom Data | `data-user-id="123"` | Passes data to JS `element.dataset` |

---

## 7. Placement Must Know 🎯

1. `id` attributes page par strictly unique hone chahiye; multiple elements ko same `id` Dena invalid HTML5 specification violation hai.
2. `data-*` attributes JavaScript me `element.dataset` object ke through read/write hote hain (`data-user-role` becomes `dataset.userRole` in CamelCase).
3. `element.getAttribute("value")` HTML source code ka original initial attribute return karta hai, jabki `element.value` user dwara typed live DOM property value return karta hai.
4. `tabindex="0"` non-interactive elements (`<div>`, `<span>`) ko keyboard focusable banata hai.
5. `hidden` attribute boolean tag hai (Presence means `true`, absence means `false`).
