FRUIT SLASH 3D — PWA MOBILE EDITION
====================================

Isi paket:
- index.html              Game utama Three.js
- manifest.webmanifest    Metadata PWA
- sw.js                   Service worker/offline cache
- icons/                  Ikon Android/iOS/PWA

Fitur mobile yang ditambahkan:
- Responsive + viewport-fit=cover
- Safe-area untuk notch / Dynamic Island
- Orientasi PWA landscape
- Kamera & area spawn adaptif untuk portrait/landscape
- Adaptive graphics HIGH / MED / LOW
- Penurunan kualitas otomatis jika FPS rendah
- Pause otomatis saat aplikasi masuk background
- Tombol install pada browser yang mendukung beforeinstallprompt
- Service worker untuk cache/offline
- High score tetap memakai localStorage

PENTING TENTANG OFFLINE
-----------------------
Three.js masih diambil dari CDN pada kunjungan online pertama:
https://cdn.jsdelivr.net/npm/three@0.180.0/build/three.module.js

Service worker lalu menyimpannya ke Cache Storage. Jadi setelah kunjungan/install
pertama berhasil saat online, game dapat dibuka kembali secara offline.

PWA TIDAK BERJALAN PENUH DARI file://
--------------------------------------
Service worker hanya aktif melalui HTTPS atau localhost.

Tes di komputer:
1. Buka terminal di folder ini.
2. Jalankan:
   python -m http.server 8080
3. Buka:
   http://localhost:8080

Tes di HP dalam jaringan Wi-Fi yang sama:
- Untuk service worker/PWA penuh, gunakan hosting HTTPS.
- Cara termudah: upload folder ini ke GitHub Pages, Netlify, Vercel, Cloudflare Pages,
  atau hosting HTTPS lain.

Install Android:
- Buka URL HTTPS di Chrome.
- Pilih Install app / Add to Home screen.
- Jika browser memunculkan tombol INSTALL APP di menu game, tombol itu juga bisa dipakai.

Install iPhone/iPad:
- Buka URL HTTPS di Safari.
- Share.
- Add to Home Screen.

Catatan orientasi:
Manifest meminta landscape. Game tetap adaptif jika browser membukanya portrait,
tetapi landscape memberi area slicing yang lebih nyaman.
