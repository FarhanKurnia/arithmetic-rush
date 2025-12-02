# 🧠 CLASH OF MINDS - ARITHMETIC RUSH ⚡

Aplikasi web game Hitung Cepat (Arithmetic Rush) interaktif yang dirancang untuk acara **BSI Day 2025**. Game ini menguji kecepatan berpikir dan akurasi berhitung peserta.

---

## 🚀 Ikhtisar Fitur Utama

Proyek ini dibangun menggunakan HTML, CSS, dan JavaScript murni, berfokus pada kinerja cepat, kemudahan kustomisasi, dan tampilan modern yang responsif.

* **Game Loop Penuh:** Siklus permainan lengkap, dari Halaman Cover hingga Halaman Selesai.
* **Perhitungan Otomatis:** Jawaban soal aritmatika dihitung secara *real-time* oleh JavaScript saat tombol "Tampilkan Jawaban" diklik (menggunakan fungsi `eval()`).
* **Data Eksternal (JSON):** Data soal (`questions.json`) dan peraturan (`rules.json`) dimuat secara asinkron, memudahkan *update* konten.
* **Timer Interaktif:** Timer mundur 20 detik yang berfungsi sebagai batas waktu menjawab.
* **Audio Interaktif:** Musik latar (backsound) dan efek suara saat navigasi, menambah suasana dramatis.
* **Desain Responsif:** Tampilan dioptimalkan untuk berbagai perangkat (desktop, tablet, dan mobile).

---

## 📋 Struktur Proyek
.   ├── assets/ 
    │ ├── css/ 
    │ │ └── style.css # Styling utama dan media queries 
    │ ├── js/ 
    │ │ └── script.js # Logika game (game state, timer, perhitungan) 
    │ ├── data/ 
    │ │ ├── questions.json # Sumber data soal matematika (ekspresi) 
    │ │ └── rules.json # Sumber data peraturan game 
    │ └── audio/ # Folder untuk semua file audio (.mp3, .m4a) 
    │ └── img/ # Folder untuk semua gambar background dan aset 
    ├── index.html # Struktur HTML utama (4 halaman game) 
    └── README.md
---

## 🖥️ Cara Menjalankan

1.  **Kloning Repositori:** Unduh atau *clone* seluruh folder proyek.
2.  **Server Lokal:** Karena game memuat data dari file JSON, Anda **harus** menjalankan proyek melalui server lokal (misalnya, menggunakan ekstensi **"Live Server"** di Visual Studio Code, atau melalui XAMPP/WAMP).
3.  **Buka Browser:** Buka `index.html` melalui URL server lokal Anda (misalnya: `http://127.0.0.1:5500/index.html`).

---

## ⚙️ Konfigurasi dan Kustomisasi

### 1. Mengubah Soal

Soal harus ditulis dalam format ekspresi matematika yang dapat dihitung oleh JavaScript (`eval()`).

* Edit file: `assets/data/questions.json`
* **Format Contoh:** `{"id": 1, "pertanyaan": "100 + 5 * (4 - 2)"}`

### 2. Mengubah Waktu Timer

Untuk mengubah batas waktu per soal, modifikasi konstanta di `assets/js/script.js`:

```javascript
// assets/js/script.js
const INITIAL_TIME = 20; // Ubah nilai ini (dalam detik)