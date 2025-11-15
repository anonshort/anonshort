<!--
  AnonShort — README
  Tip: place a banner image at /assets/banner.png (or remove the <img> block).
-->

<div align="center">

  <!-- Optional: project banner -->
  <a href="https://anonshort.com">
    <img src="https://anonshort.com/assets/img/logo.png" alt="AnonShort banner" width="250">
  </a>

  <h1>AnonShort</h1>
  <p><strong>Anonymous • Secure • Fast</strong></p>

  <p>
    <a href="https://anonshort.com"><strong>Website</strong></a> ·
    <a href="https://anonshort.com/api"><strong>API Docs</strong></a> ·
    <a href="https://t.me/AnonShortBot">Telegram Bot</a> ·
    <a href="https://t.me/+E2QR7t6ahJUyMzVl">Telegram Channel</a>
  </p>

  <!-- Capability badges -->
  <p>
    <img alt="Privacy First" src="https://img.shields.io/badge/Privacy-First-0ea5e9?style=for-the-badge" />
    <img alt="Secure HTTPS" src="https://img.shields.io/badge/Secure-HTTPS-22c55e?style=for-the-badge" />
    <img alt="Public API" src="https://img.shields.io/badge/Public%20API-Available-f59e0b?style=for-the-badge" />
    <img alt="Ad Free" src="https://img.shields.io/badge/Interface-Ad--Free-64748b?style=for-the-badge" />
  </p>

</div>

---

## Table of Contents
- [What is AnonShort?](#what-is-anonshort)
- [Highlights](#highlights)
- [Features](#features)
- [Quick Start](#quick-start)
- [API & Documentation](#api--documentation)
- [Privacy & Security](#privacy--security)
- [Preview](#preview)
- [How It Works](#how-it-works)
- [Contact & Links](#contact--links)
- [Credits](#credits)
- [License](#license)

---

## What is AnonShort?
**AnonShort** is a **privacy‑focused URL shortener** for people who value anonymity.  
No logs, no tracking, no cookies — just fast, secure redirects.

---

## Highlights
- 🔒 **Privacy-first:** anonymity by default with no referrer leaks.
- ⚡ **Fast:** snappy redirects and clean UI.
- 🧰 **Developer-friendly:** public API with QR support.
- 🎯 **Zero-nonsense:** no ads, no trackers, no cookies.

---

## Features
- ✏️ Custom short paths  
- 🔐 Password-protected links  
- ⏳ Link expiry (time-based)  
- 🕐 One-time access links  
- 💣 Self-destruct links (max-clicks)  
- 🔭 Private stats page  
- 🕵️ Anonymous redirect (no-referrer)  
- 🧾 Built-in QR code generator  
- 🧩 Public API  
- 🧼 Clean, ad‑free interface

> [!TIP]
> Pin your most important links on your profile and share the QR directly from the stats page.

---

## Quick Start

### 1) Website
1. Go to **[anonshort.com](https://anonshort.com)**
2. Paste your long URL
3. *(Optional)* set password, custom path, expiry, max-clicks, or **no‑referrer**
4. Create & share

### 2) Telegram
- Chat with **[@AnonShortBot](https://t.me/AnonShortBot)** and send your long URL  
- *(Optional)* include parameters in the same message; the bot replies with a short link + QR

### 3) API
- Use the **Public API** for programmatic shortening  
- Full spec: **[anonshort.com/api](https://anonshort.com/api)**

> [!WARNING]
> Avoid sharing password-protected links together with the password in the same chat/message.

---

## API & Documentation
All endpoints and parameters live here:

👉 **https://anonshort.com/api**

```bash
# Example (adjust to the actual API schema — see docs above)
curl -X POST https://anonshort.com/api/shorten \
  -H "Content-Type: application/json" \
  -d '{
    "url": "https://example.com",
    "custom": "my-link",
    "password": "optional",
    "expire_in": "1d",
    "max_clicks": 1,
    "no_referrer": true
  }'
