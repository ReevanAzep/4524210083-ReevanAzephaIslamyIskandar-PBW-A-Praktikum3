# 📘 Laporan Praktikum Pertemuan Ke-3

🧑‍🎓 **Reevan Azepha Islamy Iskandar — 4524210083**

# 🌐 LaraPress — Website Berbasis Laravel

LaraPress merupakan aplikasi website sederhana yang dikembangkan menggunakan Laravel 12 dan PHP. Website ini dibuat untuk mempelajari dasar pengembangan aplikasi web menggunakan framework Laravel, khususnya dalam penerapan routing, Blade Templates, dan pengaturan tampilan halaman.

Aplikasi ini memiliki tiga halaman utama, yaitu Home, Tentang Kami, dan Kontak, dengan tampilan antarmuka yang modern dan navigasi ant halaman.

<p align="center">
  <img src="https://img.shields.io/badge/PHP-8.2-777BB4?style=for-the-badge&logo=php&logoColor=white" alt="PHP 8.2">
  <img src="https://img.shields.io/badge/Laravel-12-FF2D20?style=for-the-badge&logo=laravel&logoColor=white" alt="Laravel 12">
  <img src="https://img.shields.io/badge/MySQL-Database-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/Blade-Templates-F05340?style=for-the-badge&logo=laravel&logoColor=white" alt="Blade Templates">
</p>

## 📋 Daftar Isi

- Tentang Aplikasi
- Fitur Utama
- Teknologi yang Digunakan
- Persyaratan Sistem
- Instalasi
- Penggunaan Aplikasi
- Konfigurasi Database MySQL
- Struktur Project
- Pengujian
- Pengembangan Selanjutnya
- Kesimpulan

## 🎯 Tentang Aplikasi

LaraPress adalah proyek praktikum Pemrograman Berbasis Web yang bertujuan untuk memahami cara membangun website menggunakan Laravel. Aplikasi ini menggunakan sistem routing untuk menghubungkan URL dengan halaman yang ditampilkan, serta Blade Templates untuk menyusun tampilan website.

### Halaman Utama

1. **Home** — Menampilkan halaman sambutan dan informasi utama mengenai LaraPress.
2. **Tentang Kami** — Menampilkan informasi mengenai website dan fitur yang diperkenalkan.
3. **Kontak** — Menampilkan informasi kontak dan sarana komunikasi.

## ✨ Fitur Utama

- ✅ **Halaman Home** — Halaman utama dengan desain modern dan informasi sambutan.
- ✅ **Halaman Tentang Kami** — Menyediakan informasi mengenai LaraPress.
- ✅ **Halaman Kontak** — Menampilkan informasi kontak.
- ✅ **Navigasi Website** — Mempermudah perpindahan ant halaman.
- ✅ **Desain Antarmuka** — Menggunakan CSS untuk mengatur warna, tata letak, kartu informasi, dan tombol.
- ✅ **Routing Laravel** — Menghubungkan URL dengan halaman Blade.
- ✅ **Blade Templates** — Memisahkan kode tampilan website ke dalam file template.
- ✅ **Konfigurasi Database MySQL** — Menyiapkan koneksi database melalui konfigurasi lingkungan Laravel.

Catatan: Konfigurasi MySQL disediakan sebagai bagian dari petunjuk instalasi. Halaman yang ada pada Praktikum 3 belum menggunakan operasi database untuk menyimpan informasi Home, Tentang Kami, atau Kontak.

## 🛠️ Teknologi yang Digunakan

### Backend

- **Laravel 12** — Framework PHP untuk pengembangan aplikasi web.
- **PHP 8.2** — Bahasa pemrograman utama.
- **Routing Laravel** — Mengatur URL dan halaman aplikasi.
- **Blade Templates** — Template engine untuk membuat halaman dinamis.

### Frontend

- **HTML5** — Menyusun struktur halaman website.
- **CSS3** — Mengatur desain, warna, tata letak, dan interaksi visual.
- **JavaScript** — Dapat digunakan untuk menambahkan interaksi pada sisi frontend.

### Database

- **MySQL** — Sistem manajemen basis data relasional yang digunakan untuk konfigurasi lingkungan aplikasi.

### Development Tools

- **Composer** — Mengelola dependensi PHP.
- **NPM** — Mengelola dependensi frontend.
- **Vite** — Menjalankan dan membangun aset frontend.
- **Git dan GitHub** — Mengelola versi kode dan repository proyek.

## 💻 Persyaratan Sistem

Pastikan perangkat memiliki perangkat lunak berikut:

- PHP versi 8.2 atau lebih baru yang kompatibel dengan Laravel 12.
- Composer.
- Node.js dan NPM.
- MySQL Server.
- XAMPP atau Laragon (opsional, untuk menjalankan MySQL secara lokal).
- Browser seperti Google Chrome atau Microsoft Edge.

## 🚀 Instalasi

### 1. Clone Repository

Unduh repository Praktikum 3 dari GitHub.

```bash
git clone <URL_REPOSITORY_GITHUB_ANDA>
```

Masuk ke folder proyek Laravel:

```bash
cd 4524210083-ReevanAzephaIslamyIskandar-PBW-A-Praktikum3-main/LaraPress
```

Jika proyek sudah diunduh dalam bentuk ZIP, ekstrak file terlebih dahulu dan buka terminal di dalam folder `LaraPress`.

### 2. Install Dependencies

Jalankan perintah berikut:

```bash
composer install
npm install
```

### 3. Setup Environment

Salin file `.env.example` menjadi `.env`.

```bash
cp .env.example .env
```

Kemudian buat application key:

```bash
php artisan key:generate
```

Jika menggunakan Windows, file `.env.example` juga dapat disalin secara manual menjadi `.env`.

### 4. Konfigurasi Database MySQL

Jalankan MySQL melalui XAMPP, Laragon, atau layanan MySQL yang digunakan.

Buat database dengan nama `larapress` melalui phpMyAdmin atau terminal MySQL.

```sql
CREATE DATABASE larapress;
```

Buka file `.env` di folder `LaraPress`, kemudian sesuaikan konfigurasi berikut:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=larapress
DB_USERNAME=root
DB_PASSWORD=
```

Keterangan:

- `DB_CONNECTION=mysql` menentukan penggunaan MySQL.
- `DB_HOST=127.0.0.1` menunjukkan server database lokal.
- `DB_PORT=3306` merupakan port MySQL yang umum digunakan.
- `DB_DATABASE=larapress` merupakan nama database aplikasi.
- `DB_USERNAME=root` merupakan contoh username lokal.
- `DB_PASSWORD=` merupakan contoh password kosong. Sesuaikan dengan konfigurasi MySQL milikmu.

### 5. Jalankan Migrasi Database

Setelah database dibuat dan konfigurasi selesai, jalankan:

```bash
php artisan config:clear
php artisan migrate
```

Migrasi akan membuat tabel berdasarkan file migrasi yang tersedia di dalam proyek Laravel, seperti tabel pengguna, cache, dan antrean pekerjaan.

**Penting:** Database MySQL ini baru disiapkan untuk aplikasi. Halaman Home, Tentang Kami, dan Kontak pada Praktikum 3 tidak memerlukan penyimpanan data database untuk menampilkan kontennya.

### 6. Build Assets

Untuk menjalankan aset frontend dalam mode pengembangan:

```bash
npm run dev
```

Untuk membangun aset frontend:

```bash
npm run build
```

### 7. Jalankan Aplikasi

Jalankan server Laravel:

```bash
php artisan serve
```

Buka browser dan akses:

`http://127.0.0.1:8000`

## 📖 Penggunaan Aplikasi

### Halaman Home

Halaman Home merupakan halaman utama LaraPress. Halaman ini menampilkan sambutan, informasi pengantar, dan elemen visual yang memperkenalkan website.

### Halaman Tentang Kami

Halaman Tentang Kami digunakan untuk menampilkan penjelasan mengenai website dan informasi pendukung lainnya.

### Halaman Kontak

Halaman Kontak menampilkan informasi kontak yang tersedia pada tampilan website.

### Navigasi Website

Pengguna dapat berpindah dari satu halaman ke halaman lainnya melalui menu navigasi. Routing aplikasi diatur pada file `routes/web.php`.

## 🗄️ Konfigurasi Database MySQL

Konfigurasi database dilakukan melalui file `.env`, sedangkan pengaturan koneksi database Laravel dikelola melalui `config/database.php`.

Pada Praktikum 3, database belum digunakan untuk menyimpan konten ketiga halaman utama. Migrasi Laravel tetap dapat dijalankan untuk menyiapkan tabel bawaan framework dan memastikan koneksi MySQL berfungsi.

Untuk memeriksa status migrasi, gunakan:

```bash
php artisan migrate:status
```

## 📂 Struktur Project

Berikut struktur direktori utama LaraPress berdasarkan proyek Praktikum 3:

```text
LaraPress/
├── app/
│   ├── Http/
│   │   └── Controllers/
│   │       └── Controller.php
│   ├── Models/
│   │   └── User.php
│   └── Providers/
│       └── AppServiceProvider.php
├── bootstrap/
├── config/
│   └── database.php
├── database/
│   ├── factories/
│   ├── migrations/
│   ├── seeders/
│   └── database.sqlite
├── public/
├── resources/
│   ├── css/
│   ├── js/
│   └── views/
│       ├── welcome.blade.php
│       ├── about.blade.php
│       └── kontak.blade.php
├── routes/
│   ├── console.php
│   └── web.php
├── tests/
├── .env.example
├── artisan
├── composer.json
├── package.json
└── vite.config.js
```

**Keterangan:** File `database.sqlite` merupakan file database SQLite bawaan dari proyek awal. Jika ingin menggunakan MySQL, ubah konfigurasi `.env` dan gunakan database MySQL yang sudah dibuat. File SQLite tidak otomatis dikonversi menjadi database MySQL.

## 🧪 Pengujian Aplikasi

Pengujian dilakukan untuk memastikan halaman dan routing berjalan dengan baik.

| No. | Pengujian | Hasil yang Diharapkan |
|---|---|---|
| 1 | Membuka halaman Home | Halaman Home ditampilkan dengan benar. |
| 2 | Membuka halaman Tentang Kami | Halaman informasi ditampilkan. |
| 3 | Membuka halaman Kontak | Halaman kontak ditampilkan. |
| 4 | Menggunakan navigasi | Pengguna dapat berpindah halaman. |
| 5 | Memeriksa koneksi MySQL | Laravel dapat terhubung ke database yang dikonfigurasi. |
| 6 | Menjalankan migrasi | Tabel yang tersedia pada migrasi berhasil dibuat. |

Pengujian otomatis Laravel dapat dijalankan menggunakan perintah:

```bash
php artisan test
```

Status pengujian perlu ditentukan berdasarkan hasil eksekusi aplikasi pada perangkat masing-masing.

## 🔧 Pengembangan Selanjutnya

Beberapa fitur yang dapat dikembangkan pada LaraPress adalah:

1. Menambahkan formulir kontak yang dapat menyimpan pesan ke database MySQL.
2. Membuat halaman admin untuk mengelola konten website.
3. Menambahkan fitur CRUD untuk informasi website.
4. Menggunakan Blade Layout agar struktur navigasi dan footer dapat digunakan bersama.
5. Menambahkan validasi formulir dan pengujian otomatis.

Fitur-fitur tersebut merupakan rencana pengembangan lanjutan dan belum diklaim sebagai fitur yang tersedia pada versi Praktikum 3.

## 📝 Kesimpulan

Praktikum 3 menghasilkan website sederhana bernama LaraPress yang menerapkan konsep dasar pengembangan web menggunakan Laravel 12. Aplikasi ini memiliki halaman Home, Tentang Kami, dan Kontak yang dihubungkan melalui routing serta ditampilkan menggunakan Blade Templates.

Konfigurasi MySQL dapat disiapkan melalui file `.env` dan sistem migrasi Laravel. Dengan demikian, proyek dapat menjadi dasar untuk pengembangan aplikasi web yang lebih kompleks pada praktikum berikutnya.

---

<p align="center">
  Dibuat oleh <strong>Reevan Azepha Islamy Iskandar</strong><br>
  4524210083<br>
  Praktikum Pemrograman Berbasis Web — Pertemuan Ke-3
</p>
