# How Internet Works (Lecture 02) — Coding & Web Development
**By – Nishant Sir | PW Earners**
 
---
 
## 1. Internet tak pahunchte kaise ho? (The Basic Chain)
 
**Phone (SIM) → Mobile Tower → ISP → Internet**
 
- Tumhare phone mein ek **SIM card** hota hai
- SIM Tower se radio waves ke through baat karta hai
- Tower connected hota hai **ISP (Internet Service Provider)** se
- ISP hi tumhe internet ka access deta hai
---
 
## 2. Key Terms — Getting Online
 
| Term | Matlab |
|---|---|
| **SIM Card** | Chhota chip jo phone ko telecom company ke paas identify karta hai — ek ID card ki tarah. |
| **ISP (Internet Service Provider)** | Company jo physical infrastructure (towers, cables) ki maalik hai aur internet access bechti hai. Jio, Airtel, Vi, BSNL, ACT Fibernet. |
| **Mobile Tower** | Woh tall antenna structures — phone inse wireless radio waves ke through baat karta hai (walkie-talkie jaisa concept, bas advanced). |
| **Data** | Actual info jo travel karti hai — webpage, video frame, WhatsApp message. MB/GB mein measure hoti hai. |
| **Recharge** | ISP ko payment — fixed data + calling minutes, fixed dino ke liye valid. |
| **Broadband** | Ghar tak seedha wired (cable/fiber) connection, mobile tower ke bina. Usually home WiFi ke liye use hota hai. |
| **Router/Modem** | Broadband connection ko WiFi signal mein convert karne wala box (blinking lights wala). |
 
**Note:** Kabhi kabhi phone "Connected, No Internet" bhi dikhata hai — matlab WiFi se connected ho lekin internet nahi aa raha.
 
---
 
## 3. Network kya hota hai?
 
**Network** = do ya zyada computers/devices jo aapas mein connected hain aur baat kar sakte hain.
 
Example: Ghar ka WiFi ek chhota network hai. College ka WiFi ek bada network hai.
 
### 4 Types of Networks
 
| Type | Full Form | Range/Example |
|---|---|---|
| **PAN** | Personal Area Network | Sabse chhota — kuch meters. Example: Phone ↔ Bluetooth earbuds, Phone ↔ Smartwatch |
| **LAN** | Local Area Network | Ek ghar, classroom, office floor. Example: Home WiFi ke sab devices, school computer lab. Range: ~1 building/1km |
| **MAN** | Metropolitan Area Network | Poore city ya bade campus ki multiple LANs. Example: University ke 10 departments connected, city-wide public WiFi |
| **WAN** | Wide Area Network | Sabse bada — cities, states, countries, ya poori duniya. Example: ISP ka nationwide backbone |
 
**Size order:** PAN (chhota) → LAN → MAN → WAN (sabse bada, "Duniya")
 
---
 
## 4. Client-Server Model
 
Har website/app khulne pe ek conversation hoti hai:
 
- **Client** — jo maangta hai. Tumhara browser (Chrome, Safari) ya Instagram app.
- **Server** — jo cheez deta hai. Ek powerful computer jo hamesha "on" rehta hai, data center mein, requests ka wait karte hue.
- **Request** — client jo message bhejta hai ("hey, give me YouTube homepage")
- **Response** — server jo wapas bhejta hai (actual HTML/video/data)
**Flow:** Client → Request → Server → Response → Client
 
---
 
## 5. IP Address — Har Device ka Phone Number
 
**IP Address (Internet Protocol Address)** — har device ko internet pe connect hote waqt ek unique number milta hai, taaki doosre devices ko pata ho data kahan bhejna hai.
 
Example: `142.250.183.78`
 
### Check karne ka tarika:
- **Windows:** Command Prompt → `ipconfig`
- **Mac:** Terminal → `ifconfig` ya `ipconfig getifaddr en0`
### Analogy (jaise phone contacts):
 
| Naam | Number |
|---|---|
| Varsha | 9759273450 |
| Subh | 8137861356 |
| Ankit | 7623876350 |
 
Bilkul waise hi, domains ke peeche IP addresses hote hain:
 
| Domain | IP Address |
|---|---|
| youtube.com | 196.128.1.3 |
| google.com | 196.128.1.8 |
| instagram.com | 196.128.1.5 |
| x.com | 196.128.1.24 |
| pw.com | 196.128.1.4 |
 
---
 
## 6. DNS (Domain Name System)
 
**DNS** = ek giant, distributed **phonebook** jo domain name (jaise youtube.com) ko uske actual IP address mein convert karta hai.
 
- **Domain name** — human-readable website naam, jaise amazon.com
- **Domain Name Server** — special server jiska kaam hai batana "is domain ka IP address kya hai?"
### Step-by-step Story:
 
1. Tum type karte ho **youtube.com** aur Enter dabate ho
2. Tumhara browser DNS server se poochta hai: *"youtube.com ka IP address kya hai?"*
3. DNS reply karta hai: *"Ye hai 142.250.183.78"*
4. Ab browser ko exactly pata hai Earth pe kis computer se baat karni hai
### Terminal Demo (`nslookup`)
 
```
~ % nslookup google.com
Non-authoritative answer:
Name:   google.com
Address: 192.178.193.139
 
~ % nslookup youtube.com
Non-authoritative answer:
Name:   youtube.com
Address: 142.251.220.78
```
 
---
 
## 7. IPv4 vs IPv6
 
| | IPv4 | IPv6 |
|---|---|---|
| **Format** | 4 numbers (0–255), dots se separated | Hexadecimal + colons |
| **Example** | 142.250.183.78 | 2401:4900:1c20:abcd:0000:0000:0000:1a2b |
| **Bits** | 32-bit | 128-bit |
| **Total Addresses** | ~4.3 billion | Undecillion (bahut zyada) |
| **Status** | Purana, addresses khatam ho rahe hain | Naya, shortage solve karta hai |
 
---
 
## Quick Summary Table
 
| Concept | One-liner |
|---|---|
| SIM Card | Phone ko telecom company ke paas identify karta hai |
| ISP | Company jo internet infrastructure aur access bechti hai |
| Broadband | Wired home internet connection |
| PAN | Personal, kuch meters ka network |
| LAN | Ek building/ghar ka network |
| MAN | Poore city/campus ka network |
| WAN | Poori duniya ka network |
| Client | Jo request bhejta hai (browser/app) |
| Server | Jo response deta hai (data center) |
| IP Address | Har device ka unique internet "phone number" |
| DNS | Domain name ko IP address mein convert karta hai |
| IPv4 | 32-bit, purana, ~4.3 billion addresses |
| IPv6 | 128-bit, naya, undecillion addresses |
 