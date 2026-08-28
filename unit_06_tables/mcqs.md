# Unit 06 — Multiple Choice Questions (MCQs)

This assessment contains **20 mandatory MCQs** testing your understanding of HTML tables (`<table>`, `<tr>`, `<th>`, `<td>`), semantic table sections (`<thead>`, `<tbody>`, `<tfoot>`, `<caption>`), cell spanning (`colspan`, `rowspan`), and React data table rendering.

---

### Q1. Which tag defines the root container for an HTML table?

A. `<tab>`  
B. `<table>`  
C. `<grid>`  
D. `<tcontainer>`  

**Answer:** B

**Explanation:** `<table>` is the root container tag for tabular grid data in HTML.

---

### Q2. Which element defines a single horizontal row inside an HTML table?

A. `<td>`  
B. `<th>`  
C. `<tr>`  
D. `<row>`  

**Answer:** C

**Explanation:** `<tr>` stands for Table Row and contains header cells (`<th>`) or data cells (`<td>`).

---

### Q3. What is the default font weight and text alignment of a `<th>` element in browser stylesheets?

A. Normal font weight, Left aligned  
B. Bold font weight, Center aligned  
C. Italic font weight, Right aligned  
D. Bold font weight, Left aligned  

**Answer:** B

**Explanation:** Browsers render `<th>` (Table Header) cells in bold font with centered text alignment by default.

---

### Q4. Which HTML tag is used to specify the title or caption of a table?

A. `<title>`  
B. `<label>`  
C. `<caption>`  
D. `<header>`  

**Answer:** C

**Explanation:** `<caption>` defines the title or description of a table and must be the first child inside `<table>`.

---

### Q5. What attribute merges a cell across 3 horizontal columns?

A. `rowspan="3"`  
B. `colspan="3"`  
C. `grid-span="3"`  
D. `merge="3"`  

**Answer:** B

**Explanation:** `colspan="3"` merges 3 adjacent horizontal columns into a single cell.

---

### Q6. What attribute merges a cell across 2 vertical rows?

A. `colspan="2"`  
B. `rowspan="2"`  
C. `vspan="2"`  
D. `height-span="2"`  

**Answer:** B

**Explanation:** `rowspan="2"` merges 2 adjacent vertical rows in the same column.

---

### Q7. What are the three semantic section elements used to structure large data tables?

A. `<head>`, `<body>`, `<footer>`  
B. `<thead>`, `<tbody>`, `<tfoot>`  
C. `<top>`, `<middle>`, `<bottom>`  

**Answer:** B

**Explanation:** `<thead>` (header group), `<tbody>` (body data group), and `<tfoot>` (footer total summary group) provide semantic structure for tables.

---

### Q8. Why is using HTML tables for entire webpage layouts considered bad practice in modern web development?

A. Browsers cannot render layout tables  
B. It hurts accessibility, breaks responsive design, produces bloated HTML, and violates semantic standards  
C. CSS does not support tables  
D. Tables only work in Chrome  

**Answer:** B

**Explanation:** Tables are strictly designed for tabular grid data. Page layouts should be constructed using semantic layout containers with CSS Flexbox or Grid.

---

### Q9. What happens when a multi-page table formatted with `<thead>` and `<tfoot>` is printed?

A. Browsers cut off the header after page 1  
B. Browsers automatically repeat `<thead>` and `<tfoot>` at the top and bottom of every printed page  
C. Printing fails  
D. The table turns into plain text  

**Answer:** B

**Explanation:** Print rendering engines automatically repeat semantic `<thead>` and `<tfoot>` rows across multi-page table printouts.

---

### Q10. What DOM property on an HTML `HTMLTableElement` object retrieves an array-like collection of all table rows?

A. `table.children`  
B. `table.rows`  
C. `table.getRows()`  
D. `table.rowList`  

**Answer:** B

**Explanation:** `table.rows` returns an HTMLCollection of all `<tr>` elements in the table.

---

### Q11. Where MUST the `<caption>` element be placed within a `<table>`?

A. Outside the `<html>` document  
B. Inside `<thead>`  
C. Immediately after the opening `<table>` tag as its first child  
D. At the very bottom after `</table>`  

**Answer:** C

**Explanation:** The W3C specification requires `<caption>` to be the very first child element inside `<table>`.

---

### Q12. If a table row has 4 columns and a cell uses `colspan="2"`, how many total `<td>` elements should be written in that `<tr>`?

A. 4 cells  
B. 3 cells (1 spanning cell + 2 standard cells = 4 column units)  
C. 2 cells  
D. 5 cells  

**Answer:** B

**Explanation:** A cell with `colspan="2"` occupies 2 column units. Adding 2 more standard `<td>` cells completes the 4-column row math.

---

### Q13. Which element represents a standard data cell inside a table row?

A. `<th>`  
B. `<td>`  
C. `<data>`  
D. `<cell>`  

**Answer:** B

**Explanation:** `<td>` stands for Table Data and holds standard data values.

---

### Q14. What CSS property is commonly used to combine double table borders into a single clean border line?

A. `border-collapse: collapse;`  
B. `border: single;`  
C. `table-border: 1px;`  
D. `border-spacing: 0;`  

**Answer:** A

**Explanation:** `border-collapse: collapse;` in CSS merges separate cell borders into a single clean line.

---

### Q15. In React JSX, what prop MUST be provided to each `<tr>` when rendering a dynamic database array using `.map()`?

A. `id`  
B. `index`  
C. `key`  
D. `ref`  

**Answer:** C

**Explanation:** React requires a unique `key` prop on mapped list/table row items for DOM reconciliation optimization.

---

### Q16. Can a `<th>` element be used vertically inside a `<tbody>` row?

A. No, `<th>` is only allowed in `<thead>`  
B. Yes, `<th>` can be used as a row header at the start of a `<tbody>` row  
C. Only if styled with CSS  
D. `<th>` is deprecated  

**Answer:** B

**Explanation:** `<th>` can serve as a column header or a row header (e.g., student name header for horizontal grade rows).

---

### Q17. What is the legacy HTML attribute used to display table grid borders without CSS?

A. `grid="1"`  
B. `line="1"`  
C. `border="1"`  
D. `outline="1"`  

**Answer:** C

**Explanation:** The legacy `border` attribute (e.g. `<table border="1">`) enables basic default browser border lines.

---

### Q18. How do screen readers announce table headers (`<th>`) to visually impaired users?

A. They ignore headers completely  
B. They read the associated `<th>` header text before pronouncing each cell's data value  
C. They spell out every letter  
D. They beep on headers  

**Answer:** B

**Explanation:** Screen readers leverage semantic `<th>` headers to provide contextual column/row header info before reading cell values.

---

### Q19. What element contains the total summary row at the bottom of a financial statement table?

A. `<thead>`  
B. `<tbody>`  
C. `<tfoot>`  
D. `<summary>`  

**Answer:** C

**Explanation:** `<tfoot>` (Table Footer) is designed for summary, totals, or pagination controls at the bottom of a table.

---

### Q20. If you apply `rowspan="2"` to a cell in Row 1, what must you do in Row 2?

A. Add an extra `<td>` cell  
B. Omit one `<td>` cell in Row 2 to account for the vertical span from Row 1  
C. Delete Row 2  
D. Change `rowspan` to `colspan`  

**Answer:** B

**Explanation:** Because `rowspan="2"` extends into Row 2, Row 2 must omit one cell so the overall grid alignment remains balanced.

---

*End of Unit 06 MCQs! All 20 questions completed.* 🚀
