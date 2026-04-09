## Ringkasan Proyek

Pada halaman Profil Toko Bunga (`2_RelativeLayoutApp`), `RelativeLayout`
dimanfaatkan untuk membangun komposisi visual secara dinamis tanpa terjebak posisi
bertumpuk parah (*nested layout*). Keunggulan utamanya ada pada kemampuan meletakkan 
satu bingkai mengacu pada koordinat referensi komponen di sisinya. Sebagai contoh,
posisi foto profil toko (ikon melengkung) diletakkan tumpang tindih (*overlapping*)
menjemput garis batas bawah pita *banner* punggung. Tulisan statistik serta tombol
keranjang belanja sukses ditautkan bergantungan dari elemen utama satu sama lain
hingga dasar halaman.

## Dokumentasi Teknis

### 1. Penjelasan File Resource Pendukung

Sistem antarmuka menolak keras penggunaan sandi absolut seperti HEX secara lugu.
Sebagai gantinya, pustaka tata warna disandarkan pada file eksternal `colors.xml`.

-   **Fungsinya:** Memberikan label variabel (*alias*) untuk sandi warna 
    eksperimental seperti hijau dedaunan lebat menjadi `@color/sage_green`, dan 
    abu pucat menjadi `@color/bg_ivory`. 
-   **Mengapa dipisah?:** Pemisahan tabel warna ke pusaran `/res/values/`
    merupakan doktrin kebersihan arsitektur yang mutlak. Manakala identitas merek
    Toko Bunga ini hijrah nuansa, programmer tak perlu berburu belasan sandi
    pada baris kode XML, melainkan secukupnya mengganti sebuah variabel global 
    agar riasan seisi wajah aplikasi bermutasi sekejap mata.

### 2. Penjelasan Logika Layout Utama (`activity_main.xml`)

Berbekal **RelativeLayout**, komponen tak diuntai lurus seperti peron gerbong,
namun ditanam berdasarkan kait jangkar antara elemen tetangga yang disasarkan.

-   **`layout_alignParentTop="true"`**: Digunakan khusus memborgol posisi pita
    iklan (Banner) murni merekat tanpa celah di atap peranti langit. 
-   **`layout_below="@id/header_banner"`**: Properti utama yang menggantungkan 
    selingan kontainer profil layaknya sarang laba-laba, jatuh tepat di telapak
    kaki banner.
-   **`layout_marginTop="-60dp"`**: Memodifikasi wujud absolut. Margin minus
    ini mendorong pilar profil menabrak dinding ke atas, mengizinkan gambar
    bulat toko tenggelam memotong siluet batasan banner hijau di atasnya.

### 3. Alur Visual

Lompatan layar disusun berdasarkan jejaring ikat magnet antar blok kode:

1.  **Lempengan Cakrawala (Header Banner)**: Sehelai bentangan pita dipantek kaku
    berwarna dedaunan menghabiskan seperlima volume kanvas seluler paling udik.
2.  **Serangan Lumba-Lumba (Icon Profile Overlap)**: Kontainer putih lambang 
    toko memusat presisi horisontal, ditarik ke ambang garis bawah pita banner,
    kemudian dikenakan margin pantul balik (minus) agar tertelan setengah rupa.
3.  **Terjun Bebas Indikator Angka**: Gelar identitas toko dan baris panjang
    bintang ulasan (statistik rating) dirajut rontok bergantung mengikuti punggung
    elemen sebelumnya (Teks Nama Toko).
4.  **Fondasi Sepatu**: Segala elemen tertutup dengan pemanggilan aksi di tombol 
    perintah obrolan bawah (*Action Buttons*) yang merapat pada tepian lantai
    abadi menggunakan `layout_alignParentBottom="true"`.
