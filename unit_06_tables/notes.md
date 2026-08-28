# Unit 06 — Tables (Master Study Notes)

Welcome to **Unit 06: Tables**! Web applications me tabular grid data (jaise student report cards, financial ledgers, product comparisons, aur admin panel data tables) ko organize aur render karne ke liye **HTML Tables** ka use hota hai.

---

## 1. Overview & Priority System

Is unit ke topics aur unki MERN / Placement relevance:

- ⭐⭐⭐ **Basic Table Elements (`<table>`, `<tr>`, `<th>`, `<td>`)**: MUST KNOW (Core tabular markup).
- ⭐⭐⭐ **Semantic Table Structure (`<thead>`, `<tbody>`, `<tfoot>`, `<caption>`)**: MUST KNOW (Screen reader accessibility & large paginated datasets).
- ⭐⭐⭐ **Cell Spanning (`colspan` & `rowspan`)**: MUST KNOW (Grid cell merging in complex reports & placement questions).
- ⭐⭐⭐ **React & MERN Data Table Rendering**: MUST KNOW (Rendering dynamic API arrays into table rows).

---

## 2. Basic Table Elements (`<table>`, `<tr>`, `<th>`, `<td>`) ⭐⭐⭐

### What is it?
HTML Data Table rows (`<tr>`), header cells (`<th>`), aur data cells (`<td>`) ka ek 2-dimensional grid structure hota hai.

### Why do we need it?
Structured row-column data ko alignment aur semantic clarity ke sath render karne ke liye.

### How does it work?
Browser `<table>` ko tabular grid container ki tarah parse karta hai jisme har `<tr>` ek horizontal row create karta hai, aur row ke andar `<th>` ya `<td>` vertical columns create karte hain.

### Key Elements Breakdown:
- **`<table>`**: Main table container.
- **`<tr>` (Table Row)**: Container for a horizontal row of cells.
- **`<th>` (Table Header)**: Header cell (Default: **Bold text, Centered alignment**).
- **`<td>` (Table Data)**: Standard data cell (Default: Normal font, Left alignment).

### Syntax
```html
<table>
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
    </tr>
    <tr>
        <td>Data 1</td>
        <td>Data 2</td>
    </tr>
</table>
```

### Simple Example
```html
<table border="1">
    <tr>
        <th>Roll No</th>
        <th>Student Name</th>
        <th>Marks</th>
    </tr>
    <tr>
        <td>101</td>
        <td>Bhavishya</td>
        <td>95</td>
    </tr>
</table>
```

### Expected Browser Output
Visual border grid with a header row (Bold/Centered) and student data row.

### Important Attributes
- `border` *(Legacy Attribute)*: Table cells ke aage border lines draw karta hai (e.g. `border="1"`). Modern development me styling CSS (`border: 1px solid black;`) se di jaati hai.

### Real-World Usage
1. **Admin Panel Dashboard Tables**: Users list, transactions history.
2. **Financial Reports & Invoices**: Item price, quantity, tax calculations.
3. **Sports Scorecards**: Runs, wickets, overs table.

### JavaScript / DOM Connection
HTML Tables have specialized DOM properties:
```javascript
// Accessing HTML Table DOM object properties directly
const table = document.querySelector("table");
console.log("Total Rows:", table.rows.length);
console.log("First Cell Content:", table.rows[0].cells[0].textContent);
```

### Common Mistakes
- ❌ **Putting text directly inside `<table>` or `<tr>`**: `<table>Hello<tr>...</tr></table>` (Invalid! Text MUST sit inside `<th>` or `<td>`).
- ❌ **Using Tables for Page Layout**: Webpage layout (Nav, Sidebar, Content) ke liye `<table>` use karna (Anti-pattern! Layout ke liye CSS Flexbox/Grid use karein).

### Interview Point
**Q**: What is the structural and semantic difference between `<th>` and `<td>`?  
**A**: `<th>` represents a header cell for a column or row (rendered bold & centered by default, announced as header by screen readers). `<td>` represents a standard data cell holding values.

---

## 3. Semantic Table Structure (`<thead>`, `<tbody>`, `<tfoot>`, `<caption>`) ⭐⭐⭐

### What is it?
Large data tables ko semantic sections me split karne ke liye **HTML5 Table Structural Elements** use kiye jaate hain.

```
┌─────────────────────────────────────────┐
│              <caption>                  │  <-- Table Title / Description
├─────────────────────────────────────────┤
│              <thead>                    │  <-- Header Row Group
├─────────────────────────────────────────┤
│                                         │
│              <tbody>                    │  <-- Scrollable Data Rows
│                                         │
├─────────────────────────────────────────┤
│              <tfoot>                    │  <-- Summary / Total Row
└─────────────────────────────────────────┘
```

### Element Roles:
- **`<caption>`**: Table ka title/caption (MUST be the first child inside `<table>`).
- **`<thead>`**: Table Header section (contains header `<tr>` rows).
- **`<tbody>`**: Table Body section (contains actual data rows).
- **`<tfoot>`**: Table Footer section (contains totals, summary, or pagination controls).

### Syntax & Example
```html
<table border="1">
    <caption>Invoice Summary 2026</caption>
    <thead>
        <tr>
            <th>Item</th>
            <th>Qty</th>
            <th>Price</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>HTML5 Course</td>
            <td>1</td>
            <td>&#8377; 999</td>
        </tr>
        <tr>
            <td>React Masterclass</td>
            <td>1</td>
            <td>&#8377; 1,499</td>
        </tr>
    </tbody>
    <tfoot>
        <tr>
            <td colspan="2">Total Amount</td>
            <td>&#8377; 2,498</td>
        </tr>
    </tfoot>
</table>
```

### Why use `<thead>`, `<tbody>`, `<tfoot>`?
1. **Accessibility**: Screen readers complex tables ko easily navigate kar paate hain.
2. **Print Styles & Multi-Page Tables**: Jab webpage print hota hai, to multi-page printed tables par `<thead>` aur `<tfoot>` har page ke top/bottom par auto-repeat hote hain!
3. **CSS Scrollable Table Body**: `<tbody>` ko scrollable banaya ja sakta hai jabki `<thead>` fixed rehta hai.

---

## 4. Merging Cells (`colspan` & `rowspan`) ⭐⭐⭐

Complex tables me cells ko horizontally ya vertically merge (combine) karne ke liye **`colspan`** aur **`rowspan`** attributes use kiye jaate hain.

### 1. Column Spanning (`colspan`)
Horizontal direction me multiple **columns** ko merge karta hai.

```html
<!-- Merges 3 columns into a single wide cell -->
<td colspan="3">Total Summary across 3 columns</td>
```

#### Visual Grid Math:
Agar Table me 3 columns hain (`<th>Col 1</th> <th>Col 2</th> <th>Col 3</th>`), to footer row me `<td colspan="3">` lene par wo akele 3 columns ki space occupy karega.

### 2. Row Spanning (`rowspan`)
Vertical direction me multiple **rows** ko merge karta hai.

```html
<!-- Merges 2 vertical rows in the same column -->
<td rowspan="2">Group Name</td>
```

### Complete Spanning Example
```html
<table border="1">
    <thead>
        <tr>
            <th>Department</th>
            <th>Employee</th>
            <th>Salary</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <!-- Merges 2 vertical rows for Department -->
            <td rowspan="2">Engineering</td>
            <td>Bhavishya</td>
            <td>&#8377; 90,000</td>
        </tr>
        <tr>
            <!-- Department cell skipped here because it is covered by rowspan above -->
            <td>Rahul</td>
            <td>&#8377; 85,000</td>
        </tr>
    </tbody>
</table>
```

> ⚠️ **SPANNING GRID MATH RULE**: Jab aap kisi cell par `rowspan="2"` dete hain, to agli `<tr>` row me ek `<td>` **KAM (omit)** karna padega, varna table outer alignment corrupt ho jayegi!

---

## 5. Concept Connections & Comparisons

### Comparison: `<th>` vs `<td>`

| Feature | `<th>` (Table Header) | `<td>` (Table Data) |
|---|---|---|
| **Semantic Role** | Header column or row label | Actual data cell value |
| **Default Font Weight** | **Bold** | Normal |
| **Default Text Alignment** | **Center** | Left |
| **Screen Reader Behavior** | Announced as column/row header context | Announced as data value |
| **Allowed Parent** | `<tr>` inside `<thead>` or `<tbody>` | `<tr>` inside `<tbody>` or `<tfoot>` |

---

## 6. MERN Stack & React Connection ⚛️

Full Stack MERN applications me backend API JSON response bhegti hai:

```json
[
  { "id": 1, "name": "Bhavishya", "role": "Frontend Dev", "salary": 90000 },
  { "id": 2, "name": "Priya", "role": "Backend Dev", "salary": 95000 }
]
```

### React Table JSX Rendering:
```jsx
// Rendering Dynamic Database API response into HTML Table:
return (
    <table>
        <thead>
            <tr>
                <th>ID</th>
                <th>Name</th>
                <th>Role</th>
                <th>Salary</th>
            </tr>
        </thead>
        <tbody>
            {users.map(user => (
                <tr key={user.id}>
                    <td>{user.id}</td>
                    <td>{user.name}</td>
                    <td>{user.role}</td>
                    <td>₹ {user.salary}</td>
                </tr>
            ))}
        </tbody>
    </table>
);
```

---

*End of Unit 06 Study Notes. Open `mcqs.md` for self-assessment!* 🚀
