# Lists & Tables
### HTML ke Structural Elements — Lecture 05
**Coding and Web Development** | Summary Notes | By – Nishant Sir
 
---
 
## 1. Lists in HTML
 
HTML mein **3 tarah ki lists** hoti hain, jo use hoti hain data ko organized tarike se dikhane ke liye:
 
- Unordered List
- Ordered List
- Description List
| List Type | Tag | Kab use karein |
|---|---|---|
| Unordered List | `<ul>` | Jab order/sequence matter nahi karta — jaise shopping items, kisi bhi order mein likho farak nahi padta. |
| Ordered List | `<ol>` | Jab order/sequence matter karta hai — jaise recipe ke steps (pehle pyaaz kaato, phir tel garam karo). |
| Description List | `<dl>` | Jab kisi term ka naam aur uski explanation deni ho — jaise glossary, FAQs, definitions. |
 
### 1.1 Unordered List — `<ul>`
 
`<ul>` poori list ka **container** hai, aur `<li>` (List Item) har individual item ke liye hota hai jo iske andar hota hai.
 
> `<ul>` ek dabbe jaisa hai jisme `<li>` items rakhe jaate hain — `<ul>` khud kuch nahi dikhata, uske andar ke `<li>` hi dikhte hain.
 
```html
<ul>
  <li>Hindi</li>
  <li>English</li>
  <li>Maths</li>
</ul>
```
 
### 1.2 Ordered List — `<ol>`
 
`<ol>` mein bhi `<li>` hi use hota hai — sirf container tag `<ul>` se `<ol>` mein badal jaata hai, aur items automatically numbered (1, 2, 3...) ho jaate hain.
 
```html
<ol>
  <li>Pyaaz kaato</li>
  <li>Tel garam karo</li>
</ol>
```
 
### 1.3 Description List — `<dl>`
 
`<dl>` poori description list ka container hai. Isme do tags hote hain:
 
| Tag | Full Form | Kaam |
|---|---|---|
| `<dt>` | Description Term | Term ya title hota hai |
| `<dd>` | Description Details | Us term ki description/explanation hoti hai |
 
> `<dl>` ek dabbe jaisa hai jisme `<dt>` terms aur unki `<dd>` descriptions rakhi jaati hain — `<dl>` khud kuch nahi dikhata, uske andar ke `<dt>` aur `<dd>` hi dikhte hain.
 
```html
<dl>
  <dt>HTML</dt>
  <dd>HyperText Markup Language</dd>
</dl>
```
 
### 1.4 List Styling — CSS `list-style-type`
 
Unordered list ke bullet ka style change karne ke liye `list-style-type` property use hoti hai:
 
| Value | Description |
|---|---|
| `disc` | Default filled circle |
| `circle` | Hollow circle |
| `square` | Filled square |
| `none` | Koi bullet point nahi |
 
### 1.5 Nested Lists
 
Lists ko **ek dusre ke andar** bhi likha ja sakta hai — jaise ek main list item ke andar poori sub-list. Yeh **nested list** kehlati hai.
 
**Example — Nested Ordered + Unordered:**
 
```html
<ol>
  <li>Fruits
    <ol>
      <li>Mango</li>
      <li>Orange</li>
    </ol>
  </li>
  <li>Vegetables
    <ol>
      <li>Cabbage</li>
      <li>Capsicum
        <ul>
          <li>Green Capsicum</li>
          <li>Yellow Capsicum</li>
          <li>Red Capsicum</li>
        </ul>
      </li>
    </ol>
  </li>
</ol>
```
 
👉 Yahaan outer list **ordered** hai, aur sabse andar wali (Capsicum ke colours) **unordered** hai.
 
> **📝 Homework — Nested List Practice**
>
> Ek deep nested list banao is structure ke saath:
> - I. List Item 1 → a, b (alphabetic)
> - II. List Item 2 → 1, 2 (numeric) → 2.2 ke andar bullets → usme bhi square bullets
> - III. List Item 3 → simple bullets
>
> Hint: `type="a"`, `type="1"` attributes aur nested `<ul>`/`<ol>` ka combination use karo.
 
---
 
## 2. Tables in HTML
 
### 2.1 List vs Table — Kab kya use karein?
 
| Situation | Use karein |
|---|---|
| Data ek hi dimension mein ho (sirf items, ek ke baad ek) | **List** |
| Data grid mein ho (rows aur columns dono) | **Table** |
 
Table basically **rows aur columns ka collection** hota hai.
 
### 2.2 Table ke Core Tags
 
| Tag | Full Form | Kaam |
|---|---|---|
| `<table>` | Table | Poori table ka container (jaise poori marksheet ka frame) |
| `<tr>` | Table Row | Ek horizontal row |
| `<td>` | Table Data | Ek individual cell (box), row ke andar |
 
```html
<table>
  <tr>
    <td>90</td>
    <td>50</td>
  </tr>
</table>
<!-- Emmet shortcut: table>tr*2>td*3 -->
```
 
### 2.3 Table ke Structural Tags — thead, tbody, th
 
| Tag | Full Form | Kaam |
|---|---|---|
| `<thead>` | Table Head | Header rows ko group karta hai |
| `<tbody>` | Table Body | Actual data rows ko group karta hai |
| `<th>` | Table Header | Column ya row ka title/label (bold + center by default) |
 
**Example — Marks Table:**
 
|  | Maths | Hindi | English | Science |
|---|---|---|---|---|
| **Sita** | 90 | 50 | 70 | 30 |
 
### 2.4 Caption
 
`<caption>` table ke upar ek title/heading dikhane ke liye use hota hai — jaise "A test table with merged cells".
 
### 2.5 Merging Cells — colspan & rowspan
 
| Attribute | Kaam |
|---|---|
| `colspan` | Ek cell ko horizontally (left-right) multiple **columns** jitna bada banata hai |
| `rowspan` | Ek cell ko vertically (top-bottom) multiple **rows** jitna bada banata hai |
 
**Example — Merged Cells Table** *(A test table with merged cells)*
 
```html
<table>
  <caption>A test table with merged cells</caption>
  <tr>
    <th rowspan="2"></th>
    <th colspan="2">Average</th>
    <th rowspan="2">Red eyes</th>
  </tr>
  <tr>
    <th>height</th>
    <th>weight</th>
  </tr>
  <tr>
    <td><b>Males</b></td><td>1.9</td><td>0.003</td><td>40%</td>
  </tr>
  <tr>
    <td><b>Females</b></td><td>1.7</td><td>0.002</td><td>43%</td>
  </tr>
</table>
```
 
👉 "Average" header `colspan="2"` se do columns (height + weight) cover karta hai. Blank corner cell aur "Red eyes" header `rowspan="2"` se do rows cover karte hain.
 
> **📝 Theek-Thaak Homework — Time Table**
>
> Ek weekly Time Table banao jisme:
> - Top row mein **"Time Table"** heading — poori width mein colspan se merged
> - Left side mein **"Hours"** label — rowspan se saari rows cover kare
> - Mon–Fri columns, beech mein ek **"Lunch"** row jo poori width cover kare
> - Friday ke last do periods mein **"Project"** cell — rowspan se merged
 
> **📝 Crazy Homework — Seminar Schedule**
>
> Ek advanced nested-merge table banao:
> - **Day** column — Monday, Tuesday, Wednesday rows ko rowspan se group karo (jitne slots utni height)
> - "Seminar" ek top-level header — poori width colspan
> - Uske neeche "Schedule" (Begin + End columns) aur "Topic" column
> - Monday: 2 topics (2 rows), Tuesday: 3 alag time-slots (3 rows), Wednesday: 1 row
>
> Yeh homework **colspan + rowspan dono ko ek saath, multiple levels mein** use karne ki practice karwata hai.
 
---
 
## ✅ Quick Recap
 
- **Lists:** `<ul>` (unordered), `<ol>` (ordered), `<dl>`+`<dt>`+`<dd>` (description) — sabme `<li>` item hota hai (dl chhod ke)
- **Nested Lists:** ek list dusri list ke andar — different types combine kar sakte hain
- **Tables:** `<table>` → `<tr>` (row) → `<td>`/`<th>` (cell)
- **Structure:** `<thead>` (header rows), `<tbody>` (data rows)
- **Merging:** colspan = columns merge, rowspan = rows merge
- **Caption:** table ka title dikhane ke liye
---
*Coding and Web Development — Lecture 05 | Notes based on Nishant Sir's class*
 