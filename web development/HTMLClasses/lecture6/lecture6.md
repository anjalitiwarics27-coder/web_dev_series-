# Coding and Web Development
## Lecture 06 — Lists, Tables & Forms in HTML
*Summary Notes — By Nishant Sir*

---

## 1. Lists in HTML

HTML mein do tarah ki list banayi jaati hai: **Ordered List** aur **Unordered List**. Dono ke andar list items `<li>` tag se likhe jaate hain.

### 1.1 Ordered List — `<ol>`

Ordered list ka use tab hota hai jab items ka ek sequence/order important ho. Numbering apne aap generate hoti hai.

```html
<ol>
  <li>List Item 1</li>
  <li>List Item 2</li>
  <li>List Item 3</li>
</ol>
```

**Nested Ordered List Example** (jaisa image mein tha):

```html
<ol type="I">        <!-- I, II, III -->
  <li>List Item 1
    <ol type="a">    <!-- a, b, c -->
      <li>Nested Item 1.1</li>
      <li>Nested Item 1.2</li>
    </ol>
  </li>
  <li>List Item 2
    <ol type="1">    <!-- 1, 2, 3 -->
      <li>Nested Item 2.1</li>
    </ol>
  </li>
</ol>
```

> **`type` attribute (ordered list numbering styles)**
> `type="1"` → 1,2,3 &nbsp;|&nbsp; `type="a"` → a,b,c &nbsp;|&nbsp; `type="A"` → A,B,C &nbsp;|&nbsp; `type="i"` → i,ii,iii &nbsp;|&nbsp; `type="I"` → I,II,III

### 1.2 Unordered List — `<ul>`

Unordered list ka use tab hota hai jab items ka koi fixed order/sequence zaroori nahi hai — sirf bullet points chahiye.

```html
<ul>
  <li>Nested Item 3.1</li>
  <li>Nested Item 3.2</li>
  <li>Nested Item 3.3</li>
</ul>
```

Yaad rakhein: List items kitni bhi baar nest ki ja sakti hain — ek `<ol>` ke andar `<ul>`, ya `<ul>` ke andar `<ol>` bhi use kar sakte ho.

---

## 2. Tables in HTML

Table banane ke liye 4 main tags use hote hain:

| Tag | Purpose |
|---|---|
| `<table>` | Poora table container |
| `<tr>` | Table Row |
| `<th>` | Table Header cell (bold + centered by default) |
| `<td>` | Table Data cell (normal cell) |

**Basic Table Structure — Time Table Example:**

```html
<table>
  <tr>
    <th colspan="6">Time Table</th>
  </tr>
  <tr>
    <th>Hours</th><th>Mon</th><th>Tues</th><th>Wed</th><th>Thurs</th><th>Fri</th>
  </tr>
  <tr>
    <td>1</td><td>Science</td><td>Maths</td><td>Science</td><td>Maths</td><td>Arts</td>
  </tr>
  <tr>
    <td colspan="5">Lunch</td>
  </tr>
</table>
```

> **colspan vs rowspan**
> `colspan` → ek cell ko horizontally (columns ke across) merge karta hai.
> `rowspan` → ek cell ko vertically (rows ke across) merge karta hai.
> Dono `<td>` ya `<th>` ke attribute hain.

**Advanced Example — Seminar Schedule** (rowspan/colspan ke saath):

```html
<table border="1">
  <tr>
    <th rowspan="2">Day</th>
    <th colspan="3">Seminar</th>
  </tr>
  <tr>
    <th>Begin</th><th>End</th><th>Topic</th>
  </tr>
  <tr>
    <td>Monday</td><td>8:00am</td><td>5:00pm</td>
    <td>Introduction to XML</td>
  </tr>
  <tr>
    <td rowspan="3">Tuesday</td>
    <td>8:00am</td><td>11:00am</td><td>XPath</td>
  </tr>
  <tr>
    <td>11:00am</td><td>2:00pm</td><td>XSL Transformations</td>
  </tr>
</table>
```

Note: rowspan/colspan ki wajah se kai cells merge ho jaate hain, isliye actual `<td>` count table mein dikhne wali cells se kam ho sakta hai.

---

## 3. Forms in HTML

`<form>` ek container tag hai jiske andar saare input fields (text box, password, radio, checkbox, dropdown, button, etc.) rehte hain. Forms ka use login page, sign-up, checkout/payment, comment box, social media post banane jaise real-life use cases mein hota hai.

```html
<form action="..." method="GET/POST">
  <!-- input fields yahan aayenge -->
</form>
```

### 3.1 Form Attributes

| Attribute | Kya karta hai |
|---|---|
| `action` | Form submit hone par data kahan (kis URL/backend) jaayega, yeh batata hai. |
| `method` | Data kaise bheja jaaye — GET ya POST. GET → data URL mein visible, POST → data body mein, zyada secure. |

### 3.2 Anchor Tag — `<a>`

`<a>` HTML ka woh tag hai jo clickable hyperlink/hypertext link banata hai.

```html
<a href="https://example.com" target="_blank">Click Here</a>
```

| Attribute | Explanation |
|---|---|
| `href` | Hypertext REFerence — batata hai link kahan (kis page/URL) jaayega. Bina href ke `<a>` tag kuch nahi karega — yeh sabse important attribute hai. |
| `target="_blank"` | Link ko naye tab mein open karta hai. |

### 3.3 Input Tag — `<input>`

`<input>` HTML ka sabse versatile (flexible) tag hai — yeh ek hi tag hai, lekin `type` attribute change karke yeh bilkul alag field ban jaata hai. Yeh self-closing tag hai.

```html
<input type="text" name="username">
<input type="email" name="email" placeholder="Enter email">
<input type="password" name="pwd">
<input type="radio" name="gender" value="male"> Male
<input type="radio" name="gender" value="female"> Female
```

| Attribute | Explanation |
|---|---|
| `type` | Field ka type decide karta hai — text, email, password, radio, checkbox, submit, button, date, etc. |
| `name` | Server ko field identify karne ke liye unique naam deta hai (form data ke saath bhejta hai). |
| `placeholder` | Input ke andar halka grey hint text dikhata hai — user ko batata hai kya type karna hai. |
| `value` | Field ki default/fixed value set karta hai. |

> **Radio buttons — important rule**
> Ek hi group ke saare radio buttons ka `name` attribute SAME hona chahiye (jaise `"gender"`), tabhi ek time par sirf ek hi option select ho payega. Har option ka `value` alag hona chahiye.

### 3.4 Label Tag — `<label>`

`<label>` input field ke baare mein batata hai ki usme kya type karna hai. `for` attribute ka value input ke `id` se match hona chahiye — isse label par click karne par bhi input select ho jaata hai.

```html
<label for="male">Male</label>
<input type="radio" id="male" name="gender" value="male">
```

### 3.5 Select Dropdown — `<select>`

`<select>` ek parent tag hai jiske andar `<option>` tags hote hain — yeh ek dropdown menu banata hai.

```html
<select name="state">
  <option value="UP">Uttar Pradesh</option>
  <option value="MH">Maharashtra</option>
</select>
```

### 3.6 Fieldset & Legend — `<fieldset>`

`<fieldset>` related form fields ko ek box/border ke andar group karta hai (jaise "Employee Details" section). `<legend>` uss box ka title/heading dikhata hai.

```html
<fieldset>
  <legend>Employee Details</legend>
  <label>First name:</label> <input type="text">
  <label>Last name:</label> <input type="text">
</fieldset>
```

### 3.7 Textarea — `<textarea>`

`<textarea>` multi-line text input ke liye use hota hai — jaise comment box ya delivery instructions box (Pete's Pizza order form example mein dekha gaya).

```html
<textarea rows="4" cols="40" placeholder="Delivery instructions"></textarea>
```

### 3.8 Submit — 2 Ways

Form data collect karke submit karne ke do tareeke hote hain:

- `<input type="submit" value="Submit">`
- `<button type="submit">Submit</button>`

Form ka flow: **Frontend** par user data fill karta hai → `action` attribute batata hai data kahan jaayega → **Backend** par data process hota hai.

---

## 4. Real-Life Form Examples Discussed

- Login page → username/email + password + sign-in button
- Sign-up page → welcome / registration form
- Checkout/Payment page → address, card details
- Comment box → textarea + submit
- Instagram Post → caption textarea + post button

Practical examples cover kiye gaye: **Novell Services Login** form (username, password, dropdown, radio buttons, checkboxes), aur **Pete's Pizza Delivery** order form (fieldset ke saath customer details, radio buttons for topping/size, checkboxes for extras, textarea for delivery instructions).

---

## Homework

Pete's Pizza Delivery jaisa ek complete HTML order form khud se banao — jisme fieldset (Customer details, Topping, Size, Extras, Delivery), input types (text, radio, checkbox), label, aur textarea (delivery instructions) ka use ho. Form ko browser mein open karke check karo ki layout diye gaye screenshot jaisa aa raha hai ya nahi.