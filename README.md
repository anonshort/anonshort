
<div align="center">
  <a href="https://anonshort.com">
    <img src="https://anonshort.com/assets/img/banner4.png" alt="AnonShort banner — privacy-focused URL shortener" width="100%">
  </a>

  <h1>AnonShort - Anonymous URL Shortener</h1>
  <p><strong>Anonymous • Secure • Fast - The Private Link Shortener for clean, trackless redirects</strong></p>

  <p>
    <a href="https://anonshort.com"><strong>Website</strong></a> ·
    <a href="https://anonshort.com/api"><strong>API Docs</strong></a> ·
    <a href="https://t.me/AnonShortBot">Telegram Bot</a> ·
    <a href="https://t.me/+E2QR7t6ahJUyMzVl">Telegram Channel</a>
  </p>

  <p>
    <img alt="AnonShort Privacy First" src="https://img.shields.io/badge/Privacy-First-0ea5e9?style=for-the-badge" />
    <img alt="Secure HTTPS Redirects" src="https://img.shields.io/badge/Secure-HTTPS-22c55e?style=for-the-badge" />
    <img alt="Public API for Developers" src="https://img.shields.io/badge/Public%20API-Available-f59e0b?style=for-the-badge" />
    <img alt="Ad-Free Interface" src="https://img.shields.io/badge/Ad--Free-Clean%20UI-64748b?style=for-the-badge" />
  </p>

</div>

---

## Table of Contents
- [What is AnonShort?](#what-is-anonshort)
- [Highlights](#highlights)
- [Features](#features)
- [Use Cases](#use-cases)
- [Quick Start](#quick-start)
- [API & Developer Documentation](#api--developer-documentation)
- [Privacy & Security](#privacy--security)
- [Preview](#preview)
- [FAQ](#faq)
- [Contact & Links](#contact--links)
- [Credits](#credits)
- [License](#license)

---

## What is AnonShort?
**AnonShort** is a **privacy‑focused URL shortener** that delivers **anonymous, secure, and fast redirects** with a clean UI.  
No logs. No tracking. No cookies. No ads. Just straightforward link management that protects your privacy.

> Ideal for privacy advocates, developers, security researchers, journalists, and anyone who needs **trackless redirect** and **private link sharing**.

---

## Highlights
- 🔒 **Privacy-first:** no tracking, no ads, and optional no‑referrer redirects.  
- ⚡ **Fast and reliable:** lightweight service optimized for low latency.  
- 🧰 **Developer-friendly:** generous **Public API** with QR support.  
- 🎯 **Zero-nonsense:** clean, accessible, and responsive interface.

---

## Features
- Custom short paths / slugs  
- Password‑protected links  
- Time‑based expiry (TTL)  
- One‑time access links  
- Self‑destruct links (max‑clicks)  
- Private stats page  
- Anonymous redirect (no‑referrer)  
- Built‑in QR code generator  
- Public API for automation  
- Lightweight, ad‑free interface

> Tip: Pin important links and share the QR directly from the stats page.

---

## Use Cases
- Share sensitive links without exposing the original source (no‑referrer).  
- Distribute single‑use URLs (one‑time access) for gated content.  
- Time‑bound sharing with **expiry** for temporary access.  
- Programmatic link creation and QR generation via the **Public API**.  
- Minimal‑footprint links for documentation, chats, and social posts.

---

## Quick Start

### 1) Website
1. Visit **https://anonshort.com**  
2. Paste your long URL  
3. *(Optional)* set password, custom path, expiry, max‑clicks, or no‑referrer  
4. Create and share your short link

### 2) Telegram Bot
Chat with **[@AnonShortBot](https://t.me/AnonShortBot)** and send your long URL.  
The bot responds with a short link (and a QR code when applicable).

### 3) API
Automate link creation with the **Public API**.  
See the full reference at **https://anonshort.com/api**.

---

## API & Developer Documentation

Full documentation lives here: **https://anonshort.com/api**

### Example: Create a short link
> Endpoint names and fields below are representative use the official docs if they differ.

**cURL**
```bash
curl -X POST -d "url=https://www.example.com" -d "custom_path=mycustompath" https://anonshort.com/api/
  }'
```

**Get URL Statistics**
```bash
curl -X POST https://anonshort.com/api/?stats={stats_token}
```
**Node JS (request)**
```node
const axios = require('axios');

const url = 'https://anonshort.com/api/';
const data = {
    url: 'https://www.example.com',
    custom_path: 'mycustompath'
};

axios.post(url, new URLSearchParams(data))
    .then(response => {
        console.log('Shortened URL:', response.data.short_url);
        console.log('Stats URL:', response.data.stats_url);
    })
    .catch(error => {
        console.error('Error:', error.response ? error.response.data : error.message);
    });
```

**Python (requests)**
```python
import requests

url = "https://anonshort.com/api/"
data = {
    'url': 'https://www.example.com',
    'custom_path': 'mycustompath'
}

response = requests.post(url, data=data)

if response.status_code == 200:
    print("Shortened URL:", response.json().get('short_url'))
    print("Stats URL:", response.json().get('stats_url'))
else:
    print("Error:", response.status_code, response.json())
```

**Response**
```json
{
    "short_url": "https://anonshort.com/shortened-path",
    "stats_url": "https://anonshort.com/index.php?stats=stats-token"
}
```

**Response Stats**
```json
{
    "url": "https://www.example.com",
    "clicks": 0,
    "created_at": "2024-09-03 06:42:09"
}
```

---

## Privacy & Security
- **No logs:** identifying access logs are not retained.  
- **No tracking:** no third‑party trackers or ad scripts.  
- **No cookies:** public pages avoid tracking cookies.  
- **No‑referrer:** hide referrer when redirecting to the destination.  
- **TLS/HTTPS only:** all traffic is encrypted in transit.  
- **Per‑link controls:** password protection, expiry, and max‑clicks.

> Avoid sharing passwords in the same place you share the short link.

---

## Preview

> Replace the placeholder image with your screenshot or GIF.

<p align="center">
  <img src="assets/preview.gif" alt="AnonShort URL shortener interface preview and privacy features" width="860">
</p>

---

---

## FAQ

**Is AnonShort a secure URL shortener?**  
Yes. HTTPS is enforced, and links can be password‑protected, time‑bound, or limited by click count.

**Does AnonShort track me?**  
No. There are no tracking cookies or third‑party analytics on public pages.

**Are stats public or private?**  
Stats are private by default.

**Can I create custom slugs?**  
Yes, if available. Use the `custom` field when creating the link.

**Is there an API for QR codes?**  
Yes. A QR endpoint/field is provided per short link (see docs).

---

## Contact & Links
- 🌐 Website: **https://anonshort.com**  
- 🤖 Telegram Bot: **https://t.me/AnonShortBot**  
- 📣 Channel: **https://t.me/+E2QR7t6ahJUyMzVl**  
- ✉️ Email: **anonshort@protonmail.com**

---

## License
© 2025 AnonShort - A privacy‑first URL shortener.
