# 🏛️ Generator & Parser NIK PPPK

Aplikasi berbasis web statis (HTML/CSS/JS) untuk **menggenerate**, **memparse**, dan **memvalidasi** Nomor Induk Kependudukan (NIK) sebagai data dummy/simulasi. Didesain khusus untuk keperluan testing sistem, pengembangan aplikasi kepegawaian/pendidikan, dan edukasi struktur NIK sesuai standar Dukcapil Indonesia.

> ⚠️ **DISCLAIMER PENTING**: Aplikasi ini hanya menghasilkan data **DUMMY/SIMULASI**. NIK yang dihasilkan **TIDAK VALID secara hukum**, tidak terdaftar di database Dukcapil, dan **DILARANG** digunakan untuk keperluan resmi, verifikasi identitas, atau tindakan penipuan. Gunakan hanya untuk testing & edukasi.

## ✨ Fitur Utama

| Fitur | Deskripsi |
|-------|-----------|
| 🔢 **Generate NIK** | Buat NIK berdasarkan pilihan provinsi, kabupaten, kecamatan, tanggal lahir, dan jenis kelamin |
| 🔍 **Parse NIK** | Analisis 16 digit NIK menjadi informasi wilayah, tanggal lahir, gender, dan perkiraan usia |
| ✅ **Validasi NIK** | Cek kelengkapan format, logika tanggal, dan validitas kode wilayah |
| 📊 **Generate Massal** | Generate hingga 100 NIK sekaligus dengan parameter random yang dapat dikonfigurasi |
| 📥 **Export CSV** | Unduh hasil generate massal dalam format CSV untuk keperluan testing database |
| 📱 **Responsive UI** | Tampilan modern & adaptif di desktop maupun mobile |
| 🎨 **Visualisasi NIK** | Pemetaan warna per blok digit untuk memudahkan pemahaman struktur NIK |

## 🚀 Cara Penggunaan

Aplikasi ini bersifat **serverless** dan dapat dijalankan langsung di browser tanpa instalasi tambahan.

1. **Simpan** kode aplikasi sebagai file `index.html`
2. **Buka** file tersebut menggunakan browser modern (Chrome, Firefox, Edge, Safari, dll)
3. **Gunakan** fitur sesuai kebutuhan:
   - Pilih tab **Generate** untuk membuat NIK perorangan
   - Pilih tab **Parse** untuk menganalisis NIK yang sudah ada
   - Pilih tab **Validasi** untuk mengecek keformatan NIK
   - Pilih tab **Generate Massal** untuk membuat data testing dalam jumlah besar
4. Klik **📋 Salin** atau **📥 Export CSV** sesuai kebutuhan

## 📐 Struktur NIK (16 Digit)

Format NIK mengikuti standar Kementerian Dalam Negeri Republik Indonesia:

| Digit ke- | Komponen | Keterangan |
|-----------|----------|------------|
| 1-2 | Kode Provinsi | Berdasarkan Kepmendagri No. 49/2015 |
| 3-4 | Kode Kabupaten/Kota | Wilayah administratif tingkat II |
| 5-6 | Kode Kecamatan | Wilayah administratif tingkat III |
| 7-8 | Tanggal Lahir | Untuk perempuan ditambahkan `+40` |
| 9-10 | Bulan Lahir | Format `MM` |
| 11-12 | Tahun Lahir | Format `YY` (2 digit terakhir) |
| 13-16 | Nomor Urut | Kode unik pencatatan (0001–9999) |

**Contoh Parse Tanggal:**
- Laki-laki lahir 15 Agustus 1990 → `150890`
- Perempuan lahir 15 Agustus 1990 → `550890` (15 + 40 = 55)

## 🛠️ Teknologi yang Digunakan

- **HTML5** – Struktur semantik & aksesibilitas
- **CSS3** – Flexbox, Grid, CSS Variables, Animations
- **JavaScript (ES6+)** – Vanilla JS, DOM Manipulation, Clipboard API, Blob/CSV Export
- **Zero Dependencies** – Tidak memerlukan framework, library, atau server backend

## 📂 Struktur File
