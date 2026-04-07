# RelativeLayout App - Toko Profil

Proyek ini adalah implementasi **RelativeLayout** pada aplikasi Android sederhana untuk menampilkan halaman profil toko yang detail dan estetis. Proyek ini dibangun sebagai bagian dari tugas pemrograman mobile.

## 📱 Ringkasan Proyek

Aplikasi **RelativeLayout App** memberikan gambaran tentang bagaimana membangun antarmuka pengguna (UI) Android yang responsif dan terstruktur dengan menggunakan `RelativeLayout`. Aplikasi ini meniru profil nyata suatu layanan e-commerce atau jasa, lengkap dengan header, profil toko, ringkasan statistik, dekskripsi operasional, serta tombol _Call-to-Action_ (CTA).

### ✨ Fitur Utama Layout

- **Header & Profile Picture:** Menggunakan `RelativeLayout` bersarang dengan _elevation_ untuk memberikan efek kartu (_card-like_) pada foto profil.
- **Toko Info:** Informasi nama toko dan deksripsi singkat yang disusun terpusat (_center horizontal_).
- **Statistik Dinamis:** Penggunaan `LinearLayout` di dalam struktur utama untuk merapikan informasi _Rating_, _Lokasi_, dan _Status Buka/Tutup_ secara sejajar (_horizontal weight sum_).
- **Tentang Toko:** Teks deskripsi paragraf komprehensif.
- **Call-to-Action (CTA):** Tombol "Chat" dan "Pesan Sekarang" yang ditempatkan di bagian bawah (_aligned to bottom_) menggunakan kombinasi `RelativeLayout` dan `LinearLayout`.

## 🎨 Palet Warna Terpasang

Desain menggunakan warna khusus untuk menciptakan kesan _smooth_, bersih, dan rileks:

- `bg_ivory` (#FDFBF7) - Latar belakang utama aplikasi yang memberikan kesan hangat dan nyaman.
- `sage_green` (#9CAF88) - Warna aksen utama untuk banner, tombol aksi utama, dan teks penanda status.
- `white` (#FFFFFFFF) - Aksen netral untuk komponen menonjol.
- `text_dark` (#4A4A4A) - Warna teks sekunder agar lebih mudah dan nyaman dibaca.
- `black` (#FF000000) - Warna untuk teks utama (_heading_).

## 🛠 Teknologi & Struktur

- **Bahasa / Format:** XML (Android Layout), Kotlin / Java.
- **Struktur UI:** `RelativeLayout` sebagai kontainer utama dengan _nesting_ `LinearLayout` minimal untuk grup baris/kolom otomatis.
- **Minimum SDK:** Sesuai konfigurasi default Android Studio terbaru.

## 🚀 Instalasi & Menjalankan Aplikasi

1. *Clone* repositori ini:
   ```bash
   git clone https://github.com/Vraken9/RelativeLayoutApps.git
   ```
2. Buka proyek ini menggunakan **Android Studio**.
3. Tunggu hingga _Gradle Sync_ selesai.
4. Jalankan aplikasi pada *Emulator* (Android Virtual Device) atau di *Perangkat Android Fisik* (via USB Debugging/Wireless).

---
> Proyek disusun untuk memenuhi tugas Pemrograman Mobile (Topik: Layout - RelativeLayout).

