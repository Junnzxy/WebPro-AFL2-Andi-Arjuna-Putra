# WebPro-AFL2-Andi-Arjuna-Putra

# LearnHub - Student Learning Platform

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![Status](https://img.shields.io/badge/status-stable-brightgreen?style=for-the-badge)

> **Multi-page student dashboard** built with pure HTML, CSS, and Bootstrap 5 — no JavaScript frameworks, no backend, no complexity. Just open and use.

---

## 📌 Deskripsi

**EduLearn** adalah platform pembelajaran siswa berbasis web yang sepenuhnya statis dan ringan. Aplikasi ini terdiri dari **4 halaman terpisah** yang saling terhubung: Dashboard, Classroom, Scorecard, dan Settings. Dibangun murni dengan **HTML5**, **CSS3**, dan **Bootstrap 5** — tanpa JavaScript tambahan, tanpa library eksternal (selain Bootstrap CDN), dan tanpa backend. Cocok untuk demo, portofolio, atau prototype sistem learning management system (LMS).

---

## 🚀 Cara Kerja Aplikasi

### Prinsip Dasar

Aplikasi ini bekerja sebagai **multi-page website** tradisional. Setiap halaman adalah file `.html` terpisah yang saling terhubung melalui hyperlink (`<a>` tag) di menu navigasi. Tidak ada JavaScript yang menangani routing atau state — semua perpindahan halaman dilakukan oleh browser secara native.

### Alur Navigasi

```
index.html (Dashboard) ←→ classroom.html
        ↓                      ↓
  scorecard.html ←→ settings.html
```

- Klik menu **Dashboard** → membuka `index.html`
- Klik menu **Classroom** → membuka `classroom.html`
- Klik menu **Scorecard** → membuka `scorecard.html`
- Klik menu **Settings** → membuka `settings.html`

### Interaksi Pengguna

| Komponen | Cara Kerja |
|----------|-------------|
| **Sidebar Navigasi** | Setiap halaman memiliki sidebar yang sama. Link aktif diberi highlight warna biru menggunakan class Bootstrap `active`. |
| **Progress Bar** | Menggunakan komponen `.progress` dari Bootstrap. Lebar progress diatur dengan `style="width: XX%"` (statis/demo). |
| **Tabel Peringkat** | Data leaderboard ditampilkan menggunakan `<table>` dengan styling Bootstrap. Peringkat pengguna aktif diberi highlight. |
| **Form Settings** | Semua input (`<input>`, `<select>`, `<div class="form-check">`) bersifat statis — hanya untuk demo UI. Tidak ada penyimpanan data. |
| **Cards & Layout** | Menggunakan grid system Bootstrap (row/col) dan komponen card untuk menampilkan informasi. |

> ⚠️ **Catatan**: Karena tidak menggunakan JavaScript atau backend, semua data (skor, progress, peringkat) bersifat **statis/hardcoded** sebagai contoh visual. Tidak ada fungsionalitas login, penyimpanan, atau update data real-time.

---

## 🛠️ Teknologi & Elemen yang Digunakan

### Bahasa & Library

| Teknologi | Kegunaan |
|-----------|----------|
| **HTML5** | Struktur dasar setiap halaman, elemen semantik, form, tabel |
| **CSS3** | Styling tambahan (hover effects, transition, custom border radius) |
| **Bootstrap 5.3** | Grid system, komponen UI (cards, buttons, nav-pills, progress bar, badges, alerts, tables, forms) |
| **Bootstrap Icons** | Ikon vektor untuk menu, statistik, dan dekorasi |

### Elemen UI yang Digunakan

#### Bootstrap Components
- `Navbar / Nav-pills` → navigasi sidebar
- `Cards` → kontainer informasi (`.card` / custom `.bg-white.rounded-4`)
- `Progress Bar` → indikator penyelesaian bab
- `Badges` → status (Done, Start, Locked, peringkat)
- `Buttons` → tombol aksi (Lanjutkan, Simpan, dll)
- `Tables` → leaderboard dan riwayat nilai
- `Forms & Switches` → pengaturan notifikasi, privasi, aksesibilitas
- `Alerts` → notifikasi survey dan informasi
- `List Group` → daftar materi/rekomendasi
- `Grid System (Row/Col)` → layout responsif

#### Custom CSS (tanpa JS)
```css
.sidebar-link { border-radius: 12px; transition: 0.2s; }
.sidebar-link:hover { background-color: rgba(13,110,253,0.1); transform: translateX(4px); }
.card-hover:hover { transform: translateY(-3px); box-shadow: 0 0.5rem 1rem rgba(0,0,0,0.08); }
.lecture-item { border-left: 3px solid #0d6efd; }
```

---

## 📁 Struktur File

```
LearnHub/
├── index.html          # Halaman Dashboard (beranda, statistik, rekomendasi)
├── classroom.html      # Halaman Kelas (daftar materi, progress belajar)
├── scorecard.html      # Halaman Skor & Peringkat (leaderboard, riwayat kuis)
├── settings.html       # Halaman Pengaturan (notifikasi, privasi, aksesibilitas)
└── README.md           # Dokumentasi proyek
```

---

## 🖥️ Halaman & Fungsionalitas

### 1. Dashboard (`index.html`)
| Elemen | Deskripsi |
|--------|-----------|
| **Header** | Menampilkan sapaan pengguna dan tanggal dinamis (JavaScript minimal untuk date) |
| **Stat Cards** | Skor (87), Bab selesai (3/16), Highscore kelas (97) |
| **Lanjutkan Belajar** | Menampilkan materi terakhir yang dikerjakan dengan progress bar |
| **Rekomendasi** | Daftar materi yang direkomendasikan |
| **Kalender** | Preview kalender akademik Maret 2026 |
| **Aktivitas** | Likes, komentar, dan pencapaian terbaru |

### 2. Classroom (`classroom.html`)
| Elemen | Deskripsi |
|--------|-----------|
| **Progress Kelas** | Total progress 3/8 materi |
| **Daftar Chapter** | 4 chapter dengan status (Done, Start, Locked) |
| **Materi Preview** | Menampilkan konten reading material chapter aktif |
| **Quiz Info** | Informasi bahwa quiz terkunci hingga materi selesai |

### 3. Scorecard (`scorecard.html`)
| Elemen | Deskripsi |
|--------|-----------|
| **Statistik Ringkas** | Total skor (87), tertinggi (97), peringkat (#4 dari 32) |
| **Leaderboard** | Tabel 5 besar siswa dengan skor dan progress |
| **Highlight Pengguna** | Baris pengguna aktif diberi warna `table-primary` |
| **Riwayat Kuis** | Daftar nilai kuis per chapter |

### 4. Settings (`settings.html`)
| Elemen | Deskripsi |
|--------|-----------|
| **Notifikasi** | Toggle switch untuk email, push, deadline reminder |
| **Privasi & Keamanan** | Two-factor authentication toggle, ubah password |
| **Aksesibilitas** | Mode kontras tinggi, perbesar teks, ukuran font |
| **Profil** | Form nama dan email |

---

## 🧪 Cara Menjalankan

### Prasyarat
- Browser modern (Chrome, Firefox, Edge, Safari)
- Koneksi internet (untuk load Bootstrap CDN — bisa diganti local jika offline)

### Langkah-langkah

1. **Clone atau download** repository ini
   ```bash
   git clone https://github.com/username/LearnHub.git
   cd LearnHub
   ```

2. **Buka file `index.html`** menggunakan browser
   - Klik kanan → Open with → pilih browser
   - Atau double-click file `index.html`

3. **Navigasi** menggunakan sidebar kiri:
   - Klik **Classroom** → membuka halaman kelas
   - Klik **Scorecard** → membuka halaman peringkat
   - Klik **Settings** → membuka halaman pengaturan

4. **Kembali ke Dashboard** kapan saja dengan klik **Dashboard**

> 📁 **Tidak perlu server** — karena ini murni static HTML/CSS. Cukup buka langsung di browser.

---

## 🎨 Kustomisasi

### Mengubah Data Statis

Semua data bersifat hardcoded dan bisa diedit langsung di file HTML:

| Data | Lokasi | Contoh Edit |
|------|--------|-------------|
| Nama siswa | Sidebar di setiap file | `Aulia Rahman` → nama Anda |
| Skor & progress | Dashboard stat cards | `87` → nilai lain |
| Leaderboard | `scorecard.html` tabel | Ubah baris `<tr>` |
| Materi chapter | `classroom.html` list-group | Tambah/hapus chapter |
| Settings default | `settings.html` form | Ubah nilai `checked` atau `value` |

### Mengubah Warna & Tema

Edit variabel atau class di `<style>` setiap file:
```css
.bg-primary → ganti dengan warna lain (#0d6efd → #your-color)
```

Atau ganti theme Bootstrap dengan CDN lain:
```html
<link href="https://cdn.jsdelivr.net/npm/bootswatch@5.3.0/dist/litera/bootstrap.min.css" rel="stylesheet">
```

---

## 📱 Responsivitas

Aplikasi ini **fully responsive** berkat Bootstrap Grid System:

| Breakpoint | Perilaku |
|------------|----------|
| `≥ 992px` (desktop) | Sidebar di kiri (2 kolom), konten 10 kolom |
| `768px - 991px` (tablet) | Sidebar menyusut, tetap di kiri |
| `< 768px` (mobile) | Sidebar menjadi full width di atas konten |

---

## ⚠️ Keterbatasan (Tanpa JS)

| Batasan | Penjelasan |
|---------|-------------|
| **Data statis** | Semua nilai (skor, progress, peringkat) tidak berubah |
| **Tidak ada penyimpanan** | Perubahan di Settings tidak tersimpan |
| **Tidak ada login** | Pengguna hanya 1 akun contoh (Aulia Rahman) |
| **Quiz tidak bisa dikerjakan** | Hanya UI simulasi |
| **Tanggal dinamis minimal** | Hanya menampilkan tanggal hari ini (1 baris JS) |

> 💡 Untuk membuat aplikasi ini **fully functional** (data dinamis, login, quiz interaktif), diperlukan JavaScript dan backend (misal: Firebase, Node.js, atau Laravel).

---

## 📄 Lisensi

MIT License — bebas digunakan, dimodifikasi, dan didistribusikan untuk keperluan pribadi, pendidikan, atau komersial.

---

## 📧 Kontak

Dibuat oleh **Andi Arjuna Putra** — [GitHub](https://github.com/yourusername)

---

*"EduLearn — belajar jadi lebih mudah, tanpa ribet, tanpa JavaScript overload."* 🚀
