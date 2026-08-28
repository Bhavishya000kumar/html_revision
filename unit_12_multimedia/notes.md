# Unit 12 — Audio, Video, Embeds & HTML5 Widgets (Master Study Notes)

Welcome to **Unit 12: Audio, Video, Embeds & HTML5 Widgets**! HTML5 introduce native media elements (`<audio>`, `<video>`), embedding (`<iframe>`), interactive accordions (`<details>`, `<summary>`), status meters (`<progress>`, `<meter>`), and native modal dialogs (`<dialog>`).

---

## 1. Overview & Priority System

- ⭐⭐⭐ **Native Video & Audio (`<video>`, `<audio>`, `<source>`)**: MUST KNOW (Media playback without flash plugins).
- ⭐⭐⭐ **Inline Frames (`<iframe>`)**: MUST KNOW (Embedding YouTube videos, Google Maps, & third-party widgets).
- ⭐⭐ **Native Accordion (`<details>` & `<summary>`)**: Important (Collapsible disclosure widget without JavaScript).
- ⭐⭐ **Native Modal Dialog (`<dialog>`)**: Important (Browser native popup modal with JS `.showModal()` API).
- ⭐ **Progress & Meter (`<progress>`, `<meter>`)**: Good to know (Status progress bars and scalar measurements).

---

## 2. Native Audio & Video (`<audio>` & `<video>`) ⭐⭐⭐

Legacy web applications audio/video ke liye third-party Flash plugins require karte the. HTML5 media elements native browser playback allow karte hain.

### 1. The `<video>` Element
```html
<video width="640" height="360" controls poster="thumbnail.jpg" preload="metadata">
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    Your browser does not support HTML5 video.
</video>
```

#### Key Video Attributes:
- **`controls`**: Browser native play, pause, volume, and fullscreen controls render karta hai.
- **`poster`**: Video play hone se pehle preview thumbnail image display karta hai.
- **`autoplay`**: Page load hote hi video auto-play karta hai (*Note*: Modern browsers require `muted` alongside `autoplay`).
- **`muted`**: Video audio track ko default mute rakhta hai.
- **`loop`**: Video end hone par automatically restart karta hai.
- **`preload`**: Loading strategy specify karta hai (`none`, `metadata`, `auto`).

### 2. The `<audio>` Element
```html
<audio controls preload="none">
    <source src="audio.mp3" type="audio/mpeg">
    <source src="audio.ogg" type="audio/ogg">
    Your browser does not support HTML5 audio.
</audio>
```

---

## 3. Inline Frames (`<iframe>`) ⭐⭐⭐

`<iframe>` (Inline Frame) current HTML document ke andar **doosre HTML page ya external web service** ko embed karta hai (e.g. YouTube Videos, Google Maps, Stripe Checkout).

```html
<iframe 
    src="https://www.youtube.com/embed/dQw4w9WgXcQ" 
    width="560" 
    height="315" 
    title="YouTube Video Player" 
    loading="lazy" 
    sandbox="allow-scripts allow-same-origin"
    allowfullscreen
></iframe>
```

### Critical iFrame Attributes & Security:
1. **`title`**: Screen readers ke liye compulsory accessibility description.
2. **`loading="lazy"`**: Defers loading off-screen iframe until scrolled into view.
3. **`sandbox`**: **SECURITY ATTRIBUTE** jo iframe embedded page ke access rights restrict karta hai (`allow-scripts`, `allow-forms`, etc.).
4. **`allowfullscreen`**: Fullscreen playback permission deta hai.

---

## 4. Native Collapsible Accordion (`<details>` & `<summary>`) ⭐⭐

`<details>` aur `<summary>` elements bina kisi JavaScript code ke **Native Collapsible Disclosure Accordion** create karte hain.

```html
<details>
    <summary>What is the MERN Stack?</summary>
    <p>MERN stands for MongoDB, Express.js, React, and Node.js.</p>
</details>
```

- **`<summary>`**: Clickable title header tag.
- **`<details>`**: Outer container (Adding `open` attribute makes it expanded by default: `<details open>`).

---

## 5. Native Modal Dialog (`<dialog>`) ⭐⭐

HTML5 `<dialog>` element browser **native popup modal** create karta hai.

```html
<dialog id="login-modal">
    <h2>User Login</h2>
    <p>Please enter credentials...</p>
    <button id="close-btn">Close</button>
</dialog>
```

### JavaScript Control API:
```javascript
const modal = document.querySelector("#login-modal");

// Opens modal as a backdrop-blocked modal dialog:
modal.showModal();

// Closes the modal dialog:
modal.close();
```

---

## 6. Progress & Meter Widgets ⭐

```html
<!-- Progress Bar: Represents task completion percentage -->
<label for="file-progress">Upload Progress:</label>
<progress id="file-progress" value="70" max="100">70%</progress>

<!-- Meter Widget: Represents scalar measurement within a known range -->
<label for="disk-usage">Disk Usage:</label>
<meter id="disk-usage" value="0.8" min="0" max="1.0" low="0.3" high="0.7" optimum="0.2">80%</meter>
```

---

## 7. Concept Comparisons

### 1. `<progress>` vs `<meter>`

| Feature | `<progress>` | `<meter>` |
|---|---|---|
| **Semantic Role** | Task completion progress (0% to 100%) | Static scalar measurement in a range |
| **Real-World Case** | File download, form wizard step | Disk space, battery level, temperature |

---

## 8. MERN Stack & React Connection ⚛️

React me custom modal states coordinate karne ke liye `<dialog>` ya `<iframe>` ref objects connect kiye jaate hain:

```jsx
// React Dialog Ref connection pattern:
const dialogRef = useRef(null);

const openModal = () => dialogRef.current.showModal();
const closeModal = () => dialogRef.current.close();

return (
    <dialog ref={dialogRef}>
        <h3>React Native Modal</h3>
        <button onClick={closeModal}>Close</button>
    </dialog>
);
```

---

## 9. Quick Revision Table ⚡

| Element | Purpose | Key Attributes |
|---|---|---|
| `<video>` | Embeds video playback | `controls`, `poster`, `muted`, `autoplay` |
| `<audio>` | Embeds audio playback | `controls`, `loop`, `preload` |
| `<source>` | Specifies media format fallbacks | `src`, `type` |
| `<iframe>` | Embeds external web pages/maps | `src`, `title`, `sandbox`, `loading` |
| `<details>` / `<summary>` | Native accordion without JS | `open` |
| `<dialog>` | Native browser popup modal | `.showModal()`, `.close()` JS API |

---

## 10. Placement Must Know 🎯

1. Browsers restrict `autoplay` audio/video execution unless the element also specifies the `muted` attribute.
2. `<source>` elements inside `<video>` or `<audio>` allow specifying multiple format fallbacks (MP4, WebM, Ogg).
3. `<iframe>` elements MUST specify a descriptive `title` attribute for web accessibility compliance.
4. `sandbox` attribute on `<iframe>` enforces strict security restrictions on third-party embedded content.
5. `<details>` and `<summary>` create collapsible FAQ accordions natively without requiring any JavaScript event handlers.
