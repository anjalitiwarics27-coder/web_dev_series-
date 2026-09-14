# Coding & Web Development — Summary Notes
### Lecture 03: What is HTML Boilerplate / Document Structure
**By – Nishant Sir**

---

## 1. Coding Kya Hai?

**Coding** = Computer ko instructions dena, ek aisi language mein jo computer samajh sake.

> **Coding = Set of Instructions** (jo computer ko diye jaate hain)

---

## 2. HTML Kya Hai?

**HTML** = **H**yper**T**ext **M**arkup **L**anguage

| Part | Matlab |
|---|---|
| **HyperText** | Aisa text jo doosre text/pages se **link** hota hai (jaise links jo aap click karte ho) |
| **Markup Language** | Yeh content ko "markup" karta hai — browser ko batata hai *"yeh heading hai"*, *"yeh paragraph hai"*, *"yeh image hai"* |

📌 **Simple words mein:** Markup language browser ko batata hai ki konsi cheez kaise render karni hai.

HTML ka use hota hai **website / webpage** banane ke liye — yeh unka **structure/code** hota hai.

---

## 3. Code Likhne Ke Liye Kya Chahiye?

Code likhne ke liye ek **Code Editor** chahiye.

- **VS Code** → sabse popular Code Editor
- VS Code ek **IDE** hai → **I**ntegrated **D**evelopment **E**nvironment

### Extensions
- Extensions ek tarah ke **add-ons** hote hain jo VS Code mein extra features add karte hain (jaise mobile mein apps install karte ho).

### File Types (Extensions)
- `.html` → HTML file
- `.mp4` → video file
- `.mp3` → audio file

---

## 4. index.html Hi Kyun?

Jab hum apni HTML file banate hain, to usko **`index.html`** naam dena ek **convention (rule)** hai.

> **"index"** ka matlab hota hai **"main / starting point"** — jaise kisi book ka Index page batata hai ki content kahan se shuru hota hai.

✅ Isliye **hamesha `index.html`** hi likhte hain (chahe file "Tanu.html" ho ya "Shankar.html" — starting file `index.html` hi honi chahiye).

---

## 5. Boilerplate Code

**Boilerplate Code** = ek **fixed/ready-made structure** jo har HTML file mein repeat hota hai — isse baar baar type nahi karna padta.

**Workflow:**
```
VS Code (HTML file banao) → Boilerplate likho → Browser mein khol kar dekho
```

VS Code mein boilerplate generate karne ka shortcut: **`!` + Tab / Enter**

---

## 6. Full HTML Boilerplate Structure

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

---

## 7. Line-by-Line Explanation

### 🔹 `<!DOCTYPE html>`
- Browser ko batata hai: **"Bhai, yeh HTML5 document hai"**
- HTML ke pehle versions the (v1, v2, v3...) jo ab **deprecated** ho chuke hain.
- Aaj current version **HTML5** hai — isi ko browser **read/render** karta hai.

### 🔹 `<html lang="en"> ... </html>`
- Yeh **Root Element** hai — matlab **sab kuch** isi ke andar aata hai.
- `lang="en"` attribute batata hai page kis **language** mein hai.
  - `lang="en"` → English content
  - `lang="hin"` → Hindi content
- **Importance (SEO + Accessibility):**
  - Screen readers ko batata hai page kis language mein padhna hai
  - Google (Search Engines) ko bhi language pata chalta hai
  - **SEO** = **S**earch **E**ngine **O**ptimization

### 🔹 `<head> ... </head>` — Head Section
> "Yeh woh information hai jo page pe **dikhti nahi**, but browser/search engines ke liye **zaroori** hai."

Head section ke andar 3 important cheezein:

**a) `<meta charset="UTF-8">`**
- Batata hai konsa **character encoding** use ho raha hai
- UTF-8 almost universal hai — emojis, special characters (₹, é, अ) sab support karta hai

**b) `<meta name="viewport" content="width=device-width, initial-scale=1.0">`**
- Yeh line **mobile responsiveness** ka foundation hai
- Breakdown:
  - `width=device-width` → page ki width, device ki screen width ke equal set ho
  - `initial-scale=1.0` → zoom level 1 (no zoom) se start ho

**c) `<title>Document</title>`**
- Yeh wahi text hai jo **browser tab** pe dikhta hai

### 🔹 `<body> ... </body>` — Body Section
> "Yahan sab kuch hota hai jo user **actually dekhta hai** — text, images, buttons, sab kuch."

- Jo bhi content hum likhते hain (`<h1>`, `<p>`, images, buttons) — sab **body ke andar** hona chahiye.

---

## 8. Quick Summary Table

| Section | Kya karta hai |
|---|---|
| `<!DOCTYPE html>` | HTML5 declare karta hai |
| `<html lang="en">` | Root element + language define |
| `<head>` | Invisible but important info (encoding, viewport, title) |
| `<meta charset>` | Character encoding set karta hai |
| `<meta viewport>` | Mobile responsiveness |
| `<title>` | Browser tab ka text |
| `<body>` | Visible content jo user dekhta hai |

---

*Notes prepared from Lecture 03 — Coding & Web Development series*
