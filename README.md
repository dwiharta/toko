# db_tokoku

Proyek aplikasi berbasis **Laravel** untuk pengelolaan toko (`db_tokoku`).

---

## 📋 Fitur Utama

- **Manajemen Transaksi & Penjualan**
- **Pencetakan Struk Pembelian**
- **Pengelolaan Database Toko (`db_tokoku`)**

---

## 🛠️ Persyaratan Sistem (Prerequisites)

Sebelum menjalankan proyek ini, pastikan sistem Anda telah memenuhi persyaratan berikut:

- **PHP**: `^8.3`
- **Composer**: Terinstal
- **MySQL / MariaDB** (atau SQLite untuk pengujian lokal)
- **Node.js & NPM** (untuk kompilasi aset frontend)

---

## 🚀 Panduan Instalasi & Pengoperasian

Ikuti langkah-langkah di bawah ini untuk menjalankan proyek di lingkungan lokal:

### 1. Clone Repository & Masuk ke Folder Proyek
```bash
git clone <URL_REPOSITORY_ANDA>
cd db_tokoku
```

### 2. Instalasi Dependensi PHP & Node.js
```bash
composer install
npm install
```

### 3. Konfigurasi Lingkungan (`.env`)
Salin file `.env.example` menjadi `.env`:
```bash
cp .env.example .env
```

Pastikan pengaturan basis data pada `.env` sudah sesuai dengan lingkungan MySQL Anda:
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=db_tokoku
DB_USERNAME=root
DB_PASSWORD=
```

### 4. Generate Application Key
```bash
php artisan key:generate
```

### 5. Jalankan Migrasi Database
Pastikan database dengan nama `db_tokoku` sudah dibuat di MySQL/PHPMyAdmin, kemudian jalankan:
```bash
php artisan migrate
```

### 6. Kompilasi Aset Frontend
```bash
npm run build
```

---

## 💻 Cara Menjalankan Server Lokal

Jalankan perintah pengembang berikut untuk memulai server Laravel dan pengompilasi aset:

```bash
composer run dev
```
atau menggunakan perintah standar Laravel:

```bash
php artisan serve
```
Aplikasi dapat diakses melalui browser di: `http://localhost:8000`

---

## 📂 Struktur Penting Terkait Cetak Struk

Untuk mengelola atau mengedit tampilan dan fungsi **Print Struk**, Anda dapat memeriksa berkas berikut:

- **Tampilan Struk (View/Blade):** `resources/views/` (contoh: `transaksi/print.blade.php` atau `struk.blade.php`)
- **Pengontrol Logika (Controller):** `app/Http/Controllers/` (contoh: `TransaksiController.php` / `POSController.php`)
- **Routing:** `routes/web.php` (mencakup rute ke cetak struk)

---

## 🧪 Pengujian (Testing)

Untuk menjalankan pengujian otomatis pada proyek ini:
```bash
composer run test
```

---

## 📄 Lisensi
Proyek ini dikembangkan dengan kerangka kerja [Laravel](https://laravel.com), yang dilindungi di bawah lisensi [MIT](https://opensource.org/licenses/MIT).