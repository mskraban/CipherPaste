# 🔒 CipherPaste

**CipherPaste** is a lightweight, **zero-knowledge** web application that transforms sensitive information into unreadable, portable "Locked Codes." 

Unlike traditional "paste-bins," CipherPaste never stores your data on a server. Using industry-standard **Authenticated Encryption ($AES-256-GCM$)**, your text is locked and unlocked entirely within your own browser. This ensures that your private notes, passwords, or messages remain invisible to everyone—including the host.



---

## 🚀 How it Works (for Everyone)

1. **Lock It:** Type or paste your sensitive text into the editor and hit **Lock**. Your text is instantly scrambled into a jumbled code.
2. **Send It:** Copy that code and send it via email, text, or chat. To anyone watching the "pipes" of the internet, it looks like random gibberish.
3. **Reveal It:** The recipient pastes the code into the **Unlock** box on their end to see the original message. 

---

## 🛡️ Security Features

* **Zero-Knowledge Architecture:** We have no database. We don't want your data, and we literally cannot see it.
* **Local Processing:** Encryption and decryption happen in your browser's RAM. Unencrypted text never touches the network.
* **Authenticated Logic:** We use $AES-256-GCM$. This doesn't just hide your data; it uses an "Authentication Tag" to ensure the data hasn't been tampered with or corrupted during transit.
* **Lossless Compression:** Uses the `CompressionStream` API to shrink your data before locking it, making the resulting codes easier to share.

---

## 🛠️ Technical Specs

| Feature | Technology |
| :--- | :--- |
| **Encryption** | $AES-256-GCM$ |
| **Key Derivation** | $PBKDF2$ (100,000 iterations) |
| **Compression** | Deflate (`CompressionStream` API) |
| **Styling** | Tailwind CSS |
| **Rich Text** | Quill.js |



---

## 🌐 Deployment

This is a **100% Static Project**. You can host it for free in seconds:

1. **Vercel:** Drop the folder onto the Vercel dashboard.
2. **GitHub Pages:** Push the code and enable "Pages" in your repository settings.
3. **Local:** Simply double-click `index.html` to run it offline.

> **⚠️ Important:** This tool requires a **Secure Context** (HTTPS) to function correctly, as the browser's Web Crypto API is disabled on unencrypted HTTP connections.

---

## 📄 License
MIT License - Feel free to use and modify for your own projects.
