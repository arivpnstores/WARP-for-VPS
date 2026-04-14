# 🚀 WARP for VPS Server

<p align="center">
  <img src="https://img.shields.io/badge/WARP-Cloudflare-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Status-Stable-brightgreen?style=for-the-badge">
  <img src="https://img.shields.io/badge/Script-fscarmen-blue?style=for-the-badge">
</p>

Panduan lengkap instalasi dan optimasi **Cloudflare WARP** pada VPS agar mendapatkan IP yang stabil dan kompatibel dengan berbagai layanan seperti ChatGPT, Netflix, dan lainnya.

---

## 📌 Fitur

* 🌍 Mengubah IP server menggunakan Cloudflare WARP
* ⚡ Mendukung akun Gratis & WARP+
* 🔒 Fix DNS agar tidak merusak network
* 🎯 Bisa mendapatkan IP clean (anti detect bot)
* 🛠 Menu interaktif & mudah digunakan

---

## ⚠️ Penting Sebelum Install

> **WAJIB dibaca!**

Pastikan semua panel / service sudah terinstall sebelum memasang WARP.

**Alasan:**

* Setelah WARP aktif, IP server akan berubah
* Config panel akan mengikuti IP WARP
* Bisa menyebabkan service error / tidak jalan

---

## 🧰 Persiapan (Fix DNS)

Jalankan perintah berikut sebelum install:

```bash
chattr -i /etc/resolv.conf && sudo rm /etc/resolv.conf && echo "nameserver 1.1.1.1" | sudo tee /etc/resolv.conf && chattr +iu /etc/resolv.conf
```

### Fungsi:

* Menghapus `resolv.conf` lama (hindari error symlink)
* Mengatur DNS ke Cloudflare (1.1.1.1)
* Mengunci file agar tidak berubah otomatis

---

## 🚀 Instalasi WARP

### 1. Jalankan Installer

```bash
wget -N https://gitlab.com/fscarmen/warp/-/raw/main/menu.sh && bash menu.sh d
```

---

### 2. Ikuti Pilihan Menu

| Langkah        | Pilihan                    |
| -------------- | -------------------------- |
| Pilih Bahasa   | `1` (English)              |
| Metode Install | `1`                        |
| Mode WARP      | `1` (Full WARP)            |
| Jenis Akun     | `1` (Gratis) / `2` (WARP+) |
| IPv6 Mode      | `3`                        |

---

## 🔑 WARP+ License (Opsional)

Jika ingin performa lebih bagus, gunakan WARP+:

👉 [https://t.me/generatewarpplusbot](https://t.me/generatewarpplusbot)

Masukkan:

* License Key
* Nama Device (bebas)

---

## 🧪 Verifikasi

Cek apakah WARP sudah aktif:

```bash
warp h
```

---

## 🌍 Mendapatkan IP WARP Berkualitas

IP default biasanya kurang bagus (terdeteksi bot).
Gunakan cara berikut untuk mendapatkan IP yang lebih clean:

```bash
warp i
```

Lalu pilih:

```
1
```

---

### ⚠️ PENTING

Jika lokasi server muncul otomatis (contoh: `sg`, `de`, dll):

✅ Langsung tekan **ENTER**
❌ Jangan ketik manual

---

## 🛠 Troubleshooting

### ❌ Lokasi salah (misal jadi US)

Jangan lanjut! Lakukan ini:

```bash
CTRL + C
warp i
```

Ulangi sampai lokasi benar.

---

### ❌ Tidak dapat IP bagus

* Jalankan ulang `warp i`
* Ulangi beberapa kali sampai dapat IP clean

---

## 🔄 Command Penting

| Fungsi        | Command    |
| ------------- | ---------- |
| Bantuan       | `warp h`   |
| Ganti IP      | `warp i`   |
| OFF sementara | `warp o`   |
| Hapus WARP    | `warp u`   |
| Keluar        | `CTRL + C` |

---

## 📊 Tips Optimal

* Gunakan WARP+ untuk IP lebih stabil
* Jangan install WARP sebelum panel
* Gunakan DNS lock untuk hindari error network
* Ulangi generate IP sampai dapat yang bagus

---

## ✅ Hasil Akhir

Jika semua langkah dilakukan dengan benar:

* ✔ IP bersih & stabil
* ✔ Support ChatGPT
* ✔ Support Netflix
* ✔ Tidak terdeteksi sebagai bot

---

## 📎 Credit

* Script by: [https://gitlab.com/fscarmen/warp](https://gitlab.com/fscarmen/warp)

---

## ⭐ Support

Jika repo ini membantu:

* ⭐ Star repo ini
* 🔁 Share ke teman
* 💬 Gunakan dengan bijak

---

<p align="center">
  Made with ❤️ for VPS Users
</p>

---

Kalau mau next level, bilang aja — gue bisa:

* bikin **README auto copy button**
* tambah **preview hasil IP (curl test)**
* atau bikin **script auto install 1 klik** 🔥
