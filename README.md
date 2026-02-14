# 🛡️ Sistem Manajemen Pelanggaran Siswa

[![Version](https://img.shields.io/badge/Version-6.0.0--Enterprise-blue?style=for-the-badge)](https://github.com/)
[![Tech](https://img.shields.io/badge/Stack-Vanilla_JS_|_Tailwind-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://github.com/)
[![Architecture](https://img.shields.io/badge/Architecture-OOP--Modular-orange?style=for-the-badge)](https://github.com/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](https://github.com/)

## 📌 Pengenalan
**Sistem Manajemen Pelanggaran Siswa** (Ra-Tech Edition) adalah platform manajemen kedisiplinan berbasis web yang mengadopsi *Local-First Architecture* [Arsitektur Lokal Utama] (a.k.a. sistem yang mengutamakan penyimpanan data di perangkat tanpa ketergantungan internet).

Proyek ini dirancang untuk mendigitalisasi proses penertiban barang bukti (razia) dan pencatatan pelanggaran siswa di SMKN 1 Malteng dengan fokus pada kecepatan akses, keamanan data lokal, dan antarmuka pengguna yang sangat responsif.

---

## 🏗️ Nilai Unggul & Arsitektur
Aplikasi ini tidak dibangun dengan skrip sederhana, melainkan menggunakan standar **Enterprise Frontend Development**:

* **OOP-Based Controller:** Seluruh logika aplikasi dibungkus dalam `class AppController`, memastikan manajemen *state* [keadaan data] (a.k.a. kondisi data yang sedang berjalan) terisolasi dan tidak mencemari ruang lingkup global.
* **Reactive UI Rendering:** Menggunakan pola pembaruan UI otomatis setiap kali terjadi perubahan pada data tanpa perlu memuat ulang halaman (*zero-refresh*).
* **Offline-First Stability:** Memanfaatkan `LocalStorage Engine V6` yang telah dioptimasi untuk menangani penyimpanan data persisten dengan integritas tinggi.
* **Utility-First Styling:** Dibangun dengan Tailwind CSS untuk menghasilkan desain yang ringan, konsisten, dan mendukung sistem tema adaptif.

---

## 🚀 Fitur Utama & Modul Teknis

### 1. Centralized Dashboard & Analytics
Sistem menyediakan ringkasan eksekutif melalui metrik statistik yang dihitung secara *on-the-fly* [langsung] (a.k.a. tanpa delay). Mencakup total pelanggaran, jumlah barang disita, dan laporan aktif.

### 2. Smart Validation Registration
Modul input data yang dilengkapi dengan `Error Boundary` [Batas Kesalahan] (a.k.a. pencegahan sistem mati saat error). Fitur ini mencakup:
* Validasi karakter nama dan kronologi secara real-time.
* Sistem pemilihan kategori barang bukti otomatis.

### 3. High-Performance Data Grid
Tabel data yang dioptimasi untuk kinerja tinggi, memiliki fitur:
* **Live Search Engine:** Algoritma pencarian instan berbasis teks.
* **Categorical Filter:** Pemfilteran data berdasarkan tingkatan kelas (X, XI, XII).
* **Infinite Scrolling:** Teknik pemuatan data bertahap untuk menjaga penggunaan RAM tetap rendah.

### 4. Enterprise Theme Management (Dark/Light)
Integrasi penuh dengan preferensi sistem operasi. Menggunakan transisi CSS halus untuk perpindahan antara mode gelap dan terang guna meningkatkan kenyamanan visual.

### 5. Data Security & JSON Portability
Karena keamanan data adalah prioritas, sistem ini menyediakan:
* **Encapsulated Export:** Mengonversi database lokal menjadi file JSON terstruktur.
* **Intelligent Import:** Mekanisme pemulihan data dengan validasi format untuk mencegah kerusakan database.

---

## 📊 Alur Kerja & Logika Sistem
Aplikasi beroperasi melalui siklus hidup berikut:
1.  **Initialization:** `AppController` melakukan audit terhadap `localStorage` saat aplikasi dimuat.
2.  **Event Handling:** Menggunakan *event delegation* [pendelegasian kejadian] (a.k.a. teknik penghematan performa pada klik tombol) untuk merespons interaksi pengguna.
3.  **Persistence:** Setiap perubahan data secara otomatis disinkronkan ke dalam penyimpanan fisik browser.
4.  **UI Sync:** Fungsi `render()` melakukan pembaruan parsial pada DOM [Document Object Model] (a.k.a. struktur tampilan web) untuk menampilkan data terbaru.

---

## 🛠️ Standar Kualitas Kode
Aplikasi ini secara ketat mengikuti prinsip pengembangan perangkat lunak modern:
* **DRY (Don't Repeat Yourself):** Logika yang sama tidak ditulis berulang kali, melainkan menggunakan fungsi utilitas.
* **SOLID Principles:** Memastikan setiap fungsi hanya memiliki satu tanggung jawab yang jelas.
* **Atomic Updates:** Menjamin bahwa jika terjadi kegagalan pada satu fungsi, data lainnya tetap utuh dan tidak rusak.

---

## 📄 Lisensi & Kontribusi
Proyek ini berada di bawah lisensi **MIT License**. Kami sangat terbuka untuk pengembangan lebih lanjut khususnya pada integrasi sinkronisasi cloud di masa depan.

---
*Developed with Precision and High Integrity Code for Educational Excellence.*
