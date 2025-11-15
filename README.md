<!-- AnonShort – README -->

<div align="center">
  <h1>AnonShort</h1>
  <p><strong>Anonymous • Secure • Fast</strong></p>

  <p>
    <a href="https://anonshort.com"><b>Website</b></a> ·
    <a href="https://anonshort.com/api"><b>API</b></a> ·
    <a href="https://t.me/AnonShortBot"><b>Telegram Bot</b></a> ·
    <a href="https://t.me/+E2QR7t6ahJUyMzVl"><b>Telegram Channel</b></a>
  </p>

  <p>
    <img alt="Privacy First" src="https://img.shields.io/badge/Privacy-First-2b6cb0?style=for-the-badge" />
    <img alt="Secure HTTPS" src="https://img.shields.io/badge/Secure-HTTPS-38a169?style=for-the-badge" />
    <img alt="Public API" src="https://img.shields.io/badge/Public%20API-Unlimited-dd6b20?style=for-the-badge" />
    <img alt="Ad Free" src="https://img.shields.io/badge/Interface-Ad--Free-e53e3e?style=for-the-badge" />
  </p>
</div>

---

## Table of Contents

- [What is AnonShort?](#-what-is-anonshort)
- [Highlights](#-highlights)
- [Feature Overview](#-feature-overview)
- [Quick Start](#-quick-start)
- [API & Documentation](#-api--documentation)
- [Preview](#-preview)
- [How It Works](#-how-it-works)
- [Contact & Links](#-contact--links)
- [License](#license)

---

## 🚀 What is AnonShort?

**AnonShort** adalah **URL shortener berfokus pada privasi** untuk pengguna yang mengutamakan anonimitas.  
Tidak ada log, pelacakan, atau cookies — hanya **redirect yang cepat dan aman**.

---

## ✨ Highlights

- 🔒 **Privacy‑first:** tanpa tracking, tanpa cookies, tanpa iklan.  
- ⚡ **Fast redirects:** stabil dan responsif.  
- 🛡️ **No‑referrer:** menyembunyikan referrer ke situs tujuan.  
- 📊 **Private stats:** statistik link bersifat privat.  
- 🧰 **Developer‑friendly:** **Public API** tanpa batas.

---

## 🧩 Feature Overview

| Kategori | Fitur |
| --- | --- |
| **Kontrol Link** | Custom short path, password‑protected links |
| **Masa Berlaku** | Expiry berbasis waktu, one‑time access, self‑destruct by max‑clicks |
| **Privasi** | Anonymous redirects (no‑referrer), private stats |
| **Kenyamanan** | Generator QR code bawaan, antarmuka bersih dan bebas iklan |
| **Integrasi** | Unlimited Public API |

> 💡 **Tips:** Pin link terpenting Anda dan bagikan QR langsung dari halaman stats.

---

## ⚡ Quick Start

### 1) Shorten via Website
1. Buka **[anonshort.com](https://anonshort.com)**  
2. Tempel URL panjang Anda  
3. (Opsional) Atur password, custom path, expiry, atau max‑clicks  
4. Buat & bagikan

### 2) Shorten via Telegram
- Chat dengan **[@AnonShortBot](https://t.me/AnonShortBot)**  
- Kirim URL dan (opsional) parameter dalam satu pesan — bot akan membalas dengan short link + QR.

---

## 📦 API & Documentation

Dokumentasi lengkap: **https://anonshort.com/api**

> **Contoh payload** *(sesuaikan dengan skema API sebenarnya—lihat dokumen di atas)*:
```bash
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
