# Coding and Web Development — Lecture 04
## Topic: Tag & Element

---

## 1. Tag Kya Hota Hai?

Tag ek **keyword** hota hai jo **angle brackets `< >`** ke andar likha jata hai.

```
<keyword>
```

Yeh browser ko batata hai — **"yeh content kis type ka hai"**.

**Example:**
```
<p>
```
Yahan `p` ek tag hai jo bata raha hai ki andar wala content ek *paragraph* hai.

---

## 2. Element Kya Hota Hai?

**Element = Opening Tag + Content + Closing Tag**

Yani element ek **poora package** hota hai — sirf tag nahi, balki uske andar ka content aur closing tag bhi.

```
<p> Hii Anish </p>
 ↑        ↑        ↑
Opening  Content  Closing
 Tag                Tag
```

| Part | Kya hai |
|---|---|
| `<p>` | Opening tag |
| `Hii Anish` | Content |
| `</p>` | Closing tag |
| Poora `<p>Hii Anish</p>` | **Element** |

### Tag ke Types:
- **Opening Tag** → `<p>`
- **Closing Tag** → `</p>`
- **Self-Closing Tag** → jaise `<img />`, `<br />` (inhe closing tag ki zaroorat nahi hoti)

---

## 3. Attribute Kya Hota Hai?

Attribute ek **extra detail/property** hota hai jo hum **opening tag ke andar** likhte hain — yeh tag ko extra information deta hai.

**Example:**
```
<img class="photo" title="My Picture" />
```
- `class` aur `title` — yeh dono **attributes** hain.
- Ek tag mein **multiple attributes** bhi ho sakte hain.

---

## 4. Heading Tags (`<h1>` to `<h6>`)

Heading ek **title ya subtitle** hota hai jo batata hai **"yeh section kis baare mein hai"**.

- HTML mein total **6 headings** hote hain: `<h1>` se `<h6>` tak.
- `<h1>` sabse important/bada heading hota hai, `<h6>` sabse chhota.
- ⚠️ **Rule:** Ek page mein normally **sirf ek hi `<h1>`** use karna chahiye — yeh page ka **main title** hota hai.

```
<h1>Main Title</h1>
<h2>Sub Heading</h2>
...
<h6>Smallest Heading</h6>
```

---

## 5. Paragraph Tag (`<p>`)

`<p>` tag **normal text/content** ke liye use hota hai — jaise koi paragraph kisi essay mein hota hai.

```
<p>Yeh ek paragraph hai.</p>
```

---

## 6. Text Formatting Tags

| Tag | Kaam |
|---|---|
| `<strong>` | Text ko **bold** banata hai (important text) |
| `<i>` / `<em>` | Text ko *italic* banata hai |
| `<mark>` | Text ko highlight karta hai |

**Example:**
```
Hii <strong>Rishikesh</strong>       → Hii **Rishikesh**
Hii <i>Rishikesh</i>                 → Hii *Rishikesh*
Hii <mark>Rishikesh</mark>           → Hii highlighted-Rishikesh
```

---

## 7. Block-level vs Inline Elements

### Block-level Elements
- Apni **poori line** lete hain — jaise ek poora row/box hota hai.
- Example: `<div>`, `<p>`, `<h1>`...`<h6>`

### Inline Elements
- Sirf **content jitni jagah** lete hain — poori line nahi lete.
- Example: `<span>`, `<a>`, `<strong>`, `<i>`

| Property | Block | Inline |
|---|---|---|
| Line space | Poori line leta hai | Sirf content jitni jagah leta hai |
| Example tags | `div`, `p`, `h1`-`h6` | `span`, `a` |

---

## 8. `<div>` Tag

- Ek **generic container/box** hota hai.
- Iska koi apna **special meaning** nahi hota (jaise `<h1>` ka matlab "heading" hota hai, waise `<div>` ka koi fixed meaning nahi).
- Sirf **content ko group/wrap** karne ke liye use hota hai.
- **Block-level** element hai.

---

## 9. `<span>` Tag

- Yeh bhi ek **generic container** hai, lekin **chhote level** pe.
- Usually ek chhote se hisse (jaise ek **word ya phrase**) ko wrap karne ke liye use hota hai — **poore section ke liye nahi**.
- **Inline** element hai.

### Div vs Span

| | `<div>` | `<span>` |
|---|---|---|
| Type | Block-level | Inline |
| Use | Bada section/group wrap karne ke liye | Chhota text/word wrap karne ke liye |

---

### 🔑 Quick Recap
- **Tag** = keyword in `< >` → tells browser content type
- **Element** = Opening tag + Content + Closing tag
- **Attribute** = extra info inside opening tag
- **Headings** `h1`-`h6` = section titles (only 1 `h1` per page)
- **`<p>`** = normal paragraph text
- **Block** = full line | **Inline** = only content space
- **`<div>`** = block container | **`<span>`** = inline container

---
*Notes based on Lecture 04 — Coding and Web Development (By Nishant Sir)*
[text](../../../../../Downloads/HTML_Tag_Element_Notes_Lecture04.pdf)