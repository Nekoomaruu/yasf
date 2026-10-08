<p align="center">
  <a href="https://github.com/Nekoomaruu/yasf">
    <img src="public/img/logo.png" alt="YASF Logo" width="200"/>
  </a>
</p>

<p align="center">
  <a href="https://github.com/Nekoomaruu/yasf/stargazers"><img src="https://img.shields.io/github/stars/Nekoomaruu/yasf?style=social" alt="GitHub Stars"></a>
  <a href="https://github.com/Nekoomaruu/yasf/network"><img src="https://img.shields.io/github/forks/Nekoomaruu/yasf?style=social" alt="GitHub Forks"></a>
  <a href="https://github.com/Nekoomaruu/yasf/issues"><img src="https://img.shields.io/github/issues/Nekoomaruu/yasf?color=red" alt="Issues"></a>
  <a href="https://github.com/Nekoomaruu/yasf/pulls"><img src="https://img.shields.io/github/issues-pr/Nekoomaruu/yasf?color=green" alt="Pull Requests"></a>
  <a href="https://github.com/Nekoomaruu/yasf/blob/main/LICENSE"><img src="https://img.shields.io/github/license/Nekoomaruu/yasf?color=blue" alt="License"></a>
  <br>
  <img src="https://img.shields.io/static/v1?label=Node.js&message=%3E%3D18&color=brightgreen&logo=node.js" alt="Node.js">
  <img src="https://img.shields.io/badge/FFmpeg-Required-ff0000?logo=ffmpeg" alt="FFmpeg">
</p>

<h1 align="center">🔥 YASF</h1>

<p align="center">
  <strong>Yet Another StreamFire</strong><br>
  Panel live streaming 24/7 pribadi: ringan, stabil, dan murah.
</p>

> **Fork dari [StreamFire](https://github.com/broman0x/streamfire) oleh [broman0x](https://github.com/broman0x).**
> YASF dikembangkan lebih lanjut dengan penambahan fitur dan perbaikan.

---

## Tentang

**YASF** adalah panel kontrol live streaming **self-hosted** agar kamu bisa streaming 24/7 tanpa harus menyalakan PC/laptop terus. Cukup VPS murah (Rp30.000/bulan pun cukup), upload video MP4, atur loop, lalu stream ke YouTube, Twitch, Facebook, TikTok, atau RTMP manapun.

## Fitur

- Dasbor modern & responsif (HP & PC)
- Resolusi 360p → 1080p 60FPS (preset siap pakai)
- Jalan lancar di VPS termurah (1 Core, 1 GB RAM)
- Monitoring CPU, RAM, dan Disk secara real-time
- Auto-loop 24/7
- Memakai FFmpeg sistem, sehingga lebih tahan crash dan memory leak
- Multi-platform: YouTube, Twitch, Facebook, TikTok, dan Custom RTMP

## Instalasi

### Otomatis

Jalankan di terminal VPS kamu (Ubuntu/Debian):

```bash
curl -fsSL https://raw.githubusercontent.com/Nekoomaruu/yasf/main/install.sh | sudo bash
```

Script ini akan menginstall FFmpeg, Node.js, meng-clone repository, lalu menjalankan aplikasi.

### Manual

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install ffmpeg nodejs npm git curl -y
git clone https://github.com/Nekoomaruu/yasf.git
cd yasf
npm install
npm start
```

Salin dan edit konfigurasi:

```bash
cp .env.example .env
nano .env
```

Isi `.env`:

```env
PORT=7575
PUBLIC_IP=your_ip_atau_kosongin
```

## Dashboard

Buka di browser: `http://IP_VPS_KAMU:7575`

## Reverse Proxy (Nginx + HTTPS Gratis), Direkomendasikan

Kalau mau pakai domain dan HTTPS gratis:

```bash
sudo apt install nginx certbot python3-certbot-nginx -y
sudo certbot --nginx -d streamfire.kamu.com
```

Ganti `streamfire.kamu.com` dengan domainmu sendiri.

## Kontribusi

Ingin berkontribusi? Silakan!

1. Fork repositori ini.
2. Buat branch baru untuk fitur/fix kamu.
3. Commit perubahan kamu.
4. Push ke branch tersebut.
5. Buat Pull Request.

Kalau menemukan bug atau punya ide fitur baru, buat [Issue](https://github.com/Nekoomaruu/yasf/issues) baru.

## Kredit

- Proyek asli: [StreamFire](https://github.com/broman0x/streamfire) oleh broman0X

## Lisensi

Dirilis di bawah [MIT License](LICENSE). Hak cipta proyek asli tetap milik broman0x.
