# Unit 08 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your knowledge of advanced HTML forms, native validations, file uploads, `<datalist>`, and hidden inputs.

---

### Q1. Which `enctype` attribute value MUST be set on a `<form>` to successfully upload file binaries (`<input type="file">`) to a backend server?

A. `application/x-www-form-urlencoded`  
B. `multipart/form-data`  
C. `text/plain`  
D. `application/json`  

**Answer:** B

**Explanation:** `multipart/form-data` is mandatory when uploading files so the browser formats input data into binary multi-part MIME streams.

---

### Q2. What input type is invisible to the user on the webpage but submits its `name` and `value` to the server?

A. `type="invisible"`  
B. `type="none"`  
C. `type="hidden"`  
D. `type="secret"`  

**Answer:** C

**Explanation:** `<input type="hidden">` is rendered invisibly and used to pass IDs, tokens, and state silently.

---

### Q3. Which attribute on `<input type="file">` restricts file selection to PNG and JPEG images only?

A. `filter="image/png, image/jpeg"`  
B. `accept="image/png, image/jpeg"`  
C. `type="image"`  
D. `restrict="png, jpeg"`  

**Answer:** B

**Explanation:** The `accept` attribute limits file picker choices to specified file extensions or MIME types.

---

### Q4. Which HTML5 attribute enforces custom Regular Expression (Regex) validation on text input?

A. `regex`  
B. `rule`  
C. `pattern`  
D. `validate`  

**Answer:** C

**Explanation:** `pattern` accepts a JavaScript Regular Expression that the input value must match before submission.

---

### Q5. What HTML5 element provides autocomplete search suggestions while still allowing custom text input?

A. `<select>`  
B. `<optgroup>`  
C. `<datalist>`  
D. `<autocomplete>`  

**Answer:** C

**Explanation:** `<datalist>` binds to an `<input list="id">` to offer dropdown suggestions while leaving the input editable.

---

### Q6. Which pair of elements is used to group related form controls together visually with a caption border?

A. `<div>` and `<p>`  
B. `<fieldset>` and `<legend>`  
C. `<section>` and `<header>`  
D. `<group>` and `<caption>`  

**Answer:** B

**Explanation:** `<fieldset>` draws a boundary box around form controls, and `<legend>` provides a text caption on the border.

---

### Q7. What input attribute limits the minimum and maximum acceptable numerical values for `<input type="number">`?

A. `start` and `end`  
B. `min` and `max`  
C. `low` and `high`  
D. `floor` and `ceiling`  

**Answer:** B

**Explanation:** `min` and `max` define numerical boundary limits for validation.

---

### Q8. What happens if a user submits a form where an input with `minlength="5"` contains only 3 characters?

A. Server crashes  
B. Browser native validation blocks submission and displays a warning message popup  
C. Data is automatically padded with spaces  
D. Input deletes itself  

**Answer:** B

**Explanation:** Native HTML5 validation checks `minlength` and blocks submission with a browser tooltip error.

---

### Q9. Which attribute allows users to select more than one file inside `<input type="file">`?

A. `multi`  
B. `multiple`  
C. `select-all`  
D. `max="10"`  

**Answer:** B

**Explanation:** The boolean `multiple` attribute enables multi-file selection in file pickers.

---

### Q10. How does `<input type="hidden">` differ from `<input disabled>` regarding form submission payload?

A. Both submit values  
B. `hidden` submits its value; `disabled` excludes its value from submission  
C. `disabled` submits its value; `hidden` excludes its value  
D. Neither submits values  

**Answer:** B

**Explanation:** `hidden` inputs are submitted with form data, whereas `disabled` inputs are skipped during form payload creation.

---

### Q11. Which attribute on `<form>` disables native HTML5 client-side validation popups?

A. `no-check`  
B. `novalidate`  
C. `disable-validation`  
D. `skip`  

**Answer:** B

**Explanation:** `novalidate` bypasses native browser form checks (useful when implementing custom JavaScript validation).

---

### Q12. Which attribute sets the step granularity increment for `<input type="number">` (e.g., allowing decimals like 0.5)?

A. `increment`  
B. `step`  
C. `gap`  
D. `scale`  

**Answer:** B

**Explanation:** `step="0.5"` configures valid numeric interval increments.

---

### Q13. Which HTML5 input type renders a native color picker palette control?

A. `type="palette"`  
B. `type="color"`  
C. `type="rgb"`  
D. `type="picker"`  

**Answer:** B

**Explanation:** `<input type="color">` opens the OS/browser native color picker widget.

---

### Q14. What value format is produced by `<input type="date">` upon form submission?

A. `DD/MM/YYYY`  
B. `YYYY-MM-DD`  
C. `MM-DD-YYYY`  
D. `Unix Timestamp`  

**Answer:** B

**Explanation:** Standard HTML5 date inputs format values into `YYYY-MM-DD` (ISO 8601 format).

---

### Q15. How do you link an `<input>` element to a `<datalist id="city-list">`?

A. `<input datalist="city-list">`  
B. `<input list="city-list">`  
C. `<input target="city-list">`  
D. `<input source="city-list">`  

**Answer:** B

**Explanation:** The `list` attribute on `<input>` takes the `id` of the target `<datalist>`.

---

### Q16. Which input type renders a slider control interface for selecting numbers within a range?

A. `type="slider"`  
B. `type="range"`  
C. `type="bar"`  
D. `type="scale"`  

**Answer:** B

**Explanation:** `<input type="range">` presents a visual slider input widget.

---

### Q17. Why are hidden inputs (`<input type="hidden">`) commonly used in web application security?

A. To hide passwords on screen  
B. To transmit Anti-CSRF (Cross-Site Request Forgery) tokens securely with form submissions  
C. To encrypt the database  
D. To disable JavaScript  

**Answer:** B

**Explanation:** Anti-CSRF tokens are embedded in forms as hidden fields to verify origin authenticity.

---

### Q18. What regex pattern ensures an input accepts exactly 10 digits (`0-9`)?

A. `pattern="[0-9]{10}"`  
B. `pattern="10digits"`  
C. `pattern="[a-z]{10}"`  
D. `pattern="num*10"`  

**Answer:** A

**Explanation:** `[0-9]{10}` matches any numeric sequence of exactly 10 digits.

---

### Q19. In Node.js Express backends, which middleware is commonly used to process `multipart/form-data` file uploads?

A. `body-parser`  
B. `multer`  
C. `cookie-parser`  
D. `cors`  

**Answer:** B

**Explanation:** `multer` is the standard Node.js middleware for handling `multipart/form-data` file requests.

---

### Q20. Can a `<legend>` tag be placed anywhere inside a `<fieldset>`?

A. Yes, anywhere  
B. No, `<legend>` must be the first child inside `<fieldset>`  
C. Only at the bottom  
D. Only outside the `<fieldset>`  

**Answer:** B

**Explanation:** `<legend>` must be the first child of `<fieldset>` to serve as the visual and semantic group header.

---

*End of Unit 08 MCQs! All 20 questions completed.* 🚀
