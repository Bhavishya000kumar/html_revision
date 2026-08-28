# Unit 07 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your understanding of HTML forms (`<form>`), input types (`<input>`), labels (`<label for>`), HTTP submission methods (`GET`/`POST`), dropdowns (`<select>`), buttons, and React form handling.

---

### Q1. Which attribute specifies the server endpoint URL where form data is sent upon submission?

A. `target`  
B. `method`  
C. `action`  
D. `href`  

**Answer:** C

**Explanation:** The `action` attribute specifies the URL or API endpoint destination for form data submission.

---

### Q2. What is the main security risk of using `method="GET"` for user login forms?

A. The browser crashes  
B. Form input values (including passwords) are appended directly to the URL bar as clear text  
C. Images stop loading  
D. `GET` forms cannot submit text  

**Answer:** B

**Explanation:** `GET` appends form key-value pairs into the browser address bar query string, exposing sensitive credentials in browser history and server logs.

---

### Q3. What attribute links a `<label>` element explicitly to an `<input>` field?

A. `link`  
B. `for`  
C. `target`  
D. `name`  

**Answer:** B

**Explanation:** The `for` attribute on a `<label>` must match the `id` attribute of the corresponding `<input>` element.

---

### Q4. What happens when a user clicks on the text of a correctly associated `<label>` tag?

A. Nothing happens  
B. The browser automatically focuses or toggles the associated input control  
C. The page reloads  
D. The label text deletes itself  

**Answer:** B

**Explanation:** Clicking a `<label>` element transfers browser focus directly to the associated input field, enhancing user experience and accessibility.

---

### Q5. What happens if an `<input>` element inside a form does NOT have a `name` attribute?

A. HTML compiler error  
B. Its value will NOT be included in the submitted form payload  
C. The input turns red  
D. The button disables itself  

**Answer:** B

**Explanation:** Browsers identify form submission data using `name=value` pairs. Without a `name` attribute, the input value is skipped during submission.

---

### Q6. How do you group multiple radio buttons (`<input type="radio">`) so that selecting one automatically deselects the others?

A. Give them unique `id` values  
B. Give all radio buttons in the group the exact SAME `name` attribute value  
C. Wrap them in a `<div>`  
D. Set `type="group"`  

**Answer:** B

**Explanation:** Radio buttons sharing the same `name` attribute form a mutually exclusive single-choice selection group.

---

### Q7. What input attribute displays light gray hint text inside an empty input field before the user starts typing?

A. `value`  
B. `hint`  
C. `placeholder`  
D. `title`  

**Answer:** C

**Explanation:** `placeholder` specifies a temporary hint string displayed inside an input box until user input is entered.

---

### Q8. Which `<button>` attribute value prevents a button inside a `<form>` from triggering a page submit?

A. `type="submit"`  
B. `type="button"`  
C. `type="reset"`  
D. `type="none"`  

**Answer:** B

**Explanation:** Inside a `<form>`, the default button behavior is `type="submit"`. Setting `type="button"` creates a generic clickable button that does not submit the form.

---

### Q9. Which HTML element is designed for multi-line text input (such as comments or user bios)?

A. `<input type="text">`  
B. `<textarea>`  
C. `<textbox>`  
D. `<multiline>`  

**Answer:** B

**Explanation:** `<textarea>` creates a multi-line plain text editing control.

---

### Q10. What boolean attribute forces native HTML browser validation to block form submission if an input is left blank?

A. `validate`  
B. `required`  
C. `mandatory`  
D. `important`  

**Answer:** B

**Explanation:** The `required` attribute specifies that an input field must be completed before submitting the form.

---

### Q11. Which child elements define individual selectable options inside a `<select>` dropdown?

A. `<choice>`  
B. `<item>`  
C. `<option>`  
D. `<li>`  

**Answer:** C

**Explanation:** `<select>` dropdown containers use `<option>` tags to define selectable items.

---

### Q12. What attribute pre-selects a default choice inside a `<select>` dropdown?

A. `checked`  
B. `selected`  
C. `default`  
D. `active`  

**Answer:** B

**Explanation:** The `selected` attribute on an `<option>` sets it as the default visible dropdown selection.

---

### Q13. What JavaScript DOM method prevents the default browser page reload when a form `submit` event fires?

A. `e.stopForm()`  
B. `e.preventDefault()`  
C. `e.blockReload()`  
D. `form.cancel()`  

**Answer:** B

**Explanation:** `e.preventDefault()` inside a submit event listener cancels the browser's default page navigation/reload behavior.

---

### Q14. What is the difference between `disabled` and `readonly` input attributes?

A. `disabled` inputs submit data, `readonly` inputs do not  
B. `disabled` inputs cannot be edited or submitted with form data, while `readonly` inputs cannot be edited but WILL be submitted  
C. They are identical  
D. `readonly` hides the input box  

**Answer:** B

**Explanation:** `disabled` controls are grayed out and excluded from form submission data. `readonly` controls prevent user modification but include their values in submission payloads.

---

### Q15. Which input type masks user characters into dots (`••••••`) on screen?

A. `type="text"`  
B. `type="secret"`  
C. `type="password"`  
D. `type="hidden"`  

**Answer:** C

**Explanation:** `type="password"` masks entered characters for visual credential protection.

---

### Q16. What is the HTTP method used by default when `<form>` omits the `method` attribute?

A. `POST`  
B. `GET`  
C. `PUT`  
D. `DELETE`  

**Answer:** B

**Explanation:** In HTML, omitting the `method` attribute defaults form submission to `GET`.

---

### Q17. How do React Controlled Components handle HTML form inputs?

A. React reads inputs using direct file system access  
B. React state binds to the input `value` and updates state on every `onChange` event  
C. React disables all HTML forms  
D. React uses `action` URLs exclusively  

**Answer:** B

**Explanation:** Controlled components in React sync input `value` with React component state via `onChange` event listeners.

---

### Q18. What input attribute pre-checks a checkbox or radio button when the page loads?

A. `selected`  
B. `checked`  
C. `active`  
&nbsp;&nbsp;&nbsp;&nbsp;D. `chosen`  

**Answer:** B

**Explanation:** The boolean `checked` attribute sets a radio button or checkbox to selected state upon page load.

---

### Q19. What element groups related form fields together with a visual border box?

A. `<group>`  
B. `<fieldset>`  
C. `<container>`  
D. `<section>`  

**Answer:** B

**Explanation:** `<fieldset>` groups related form controls visually, and `<legend>` provides a caption for the group.

---

### Q20. What is the main difference between `<button type="submit">` and `<input type="submit">`?

A. `<button>` is an inline tag  
B. `<button>` can contain nested HTML markup (like icons and formatted text), whereas `<input type="submit">` can only accept plain text in its `value` attribute  
C. `<input type="submit">` cannot submit forms  
D. `<button>` does not work in Chrome  

**Answer:** B

**Explanation:** `<button>` allows rich HTML content (icons, images, bold text) inside the button container, whereas `<input type="submit">` is restricted to plain text defined in `value`.

---

*End of Unit 07 MCQs! All 20 questions completed.* 🚀
