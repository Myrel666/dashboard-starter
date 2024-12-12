<a href="https://github.com/bezhansalleh/filament-shield" class="filament-hidden">
<img style="width: 100%; max-width: 100%;" alt="filament-shield-art" src="https://user-images.githubusercontent.com/10007504/148662315-35d4bd74-fc1c-4f8c-8c02-689309b414b0.png" >
</a>

<p align="center" class="flex items-center justify-center">
    <a href="https://filamentadmin.com/docs/2.x/admin/installation">
        <img alt="FILAMENT 8.x" src="https://img.shields.io/badge/FILAMENT-3.x-EBB304?style=for-the-badge">
    </a>
    <a href="https://packagist.org/packages/bezhansalleh/filament-shield">
        <img alt="Packagist" src="https://img.shields.io/packagist/v/bezhansalleh/filament-shield.svg?style=for-the-badge&logo=packagist">
    </a>
    <a href="https://github.com/bezhansalleh/filament-shield/actions?query=workflow%3Arun-tests+branch%3A3.x">
        <img alt="Tests Passing" src="https://img.shields.io/github/actions/workflow/status/bezhansalleh/filament-shield/run-tests.yml?style=for-the-badge&logo=github&label=tests" class="filament-hidden">
    </a>
    <a href="https://github.com/bezhansalleh/filament-shield/actions?query=workflow%3A"Check+%26+fix+styling"+branch%3A3.x" class="filament-hidden">
        <img alt="Code Style Passing" src="https://img.shields.io/github/actions/workflow/status/bezhansalleh/filament-shield/laravel-pint.yml?style=for-the-badge&logo=github&label=code%20style">
    </a>

<a href="https://packagist.org/packages/bezhansalleh/filament-shield">
    <img alt="Downloads" src="https://img.shields.io/packagist/dt/bezhansalleh/filament-shield.svg?style=for-the-badge" >
    </a>
</p>


> Proteksi, otorisasi, dan pengelolaan peran pengguna yang canggih dengan [Filament Shield](https://filamentphp.com/plugins/bezhansalleh-shield).

Filament Shield adalah plugin untuk [Filament Admin](https://filamentphp.com/) yang memungkinkan Anda dengan mudah membuat **Role-Based Access Control (RBAC)** dengan fungsionalitas otorisasi yang mudah dikelola. Plugin ini memungkinkan Anda menentukan **izin pengguna, peran, dan pengelolaan akses pengguna** secara efisien.

---

## 🚀 **Fitur Utama**
- 🔐 **Akses Berbasis Peran** (Role-Based Access Control)
- ⚙️ **Generator Izin Otomatis** untuk resource, halaman, dan widget.
- 📄 **Dukungan Custom Policy**.
- 🔍 **Pengelolaan Izin dan Peran** langsung dari antarmuka Filament.
- 💾 **Mudah disimpan dan disinkronkan** menggunakan cache.
- 📦 **Migrasi, seeder, dan perintah artisan** untuk pengaturan cepat.

---

## 📥 **Instalasi**
Untuk mulai menggunakan **Filament Shield**, ikuti langkah-langkah berikut.

Install package:
```bash
composer require bezhansalleh/filament-shield
``````
Setelah itu, jalankan perintah instalasi:
```bash
php artisan shield:install
``````
Jalankan migrasi untuk membuat tabel peran dan izin:
```bash
php artisan migrate
``````
Untuk membuat peran default dan izin yang diperlukan, Anda dapat menggunakan:
```bash
php artisan shield:generate
``````
## 📚 **Daftar Perintah Artisan**

| Perintah                        | Deskripsi                               | Contoh Penggunaan            |
|---------------------------------|-----------------------------------------|------------------------------|
| `php artisan migrate`           | Menjalankan migrasi database            | `php artisan migrate`         |
| `php artisan shield:install`    | Instalasi Filament Shield               | `php artisan shield:install`  |
| `php artisan shield:generate`   | Membuat peran dan izin secara otomatis  | `php artisan shield:generate` |
| `php artisan config:cache`      | Meng-cache konfigurasi Laravel          | `php artisan config:cache`    |

## 📦 **Pengaturan File Konfigurasi**
Setelah menjalankan perintah `php artisan shield:install`, file config/shield.php akan dibuat. Anda dapat mengatur preferensi plugin di sini, termasuk menentukan model pengguna, peran default, dan izin default.

## ❓ Masalah Umum dan Solusinya
### 🔴 **1. Kolom `team_id` Tidak Ditemukan**
**Error:**
SQLSTATE[42S22]: Column not found: 1054 Unknown column 'team_id'
**Solusi:**
- Pastikan kolom `team_id` ada di tabel `model_has_roles`.
- Jika tidak menggunakan multi-team, atur `teams => false` di file **config/permission.php**.

### 🔴 **2. Artisan Shield Tidak Berjalan**
**Error:**
Command "shield:install" is not defined.
**Solusi:**
- Pastikan **composer install** telah dijalankan.
- Periksa apakah paket **bezhansalleh/filament-shield** telah terinstal.

---

##  **Credits**
- [Bezhan Salleh](https://github.com/bezhanSalleh)
- [All Contributors](../../contributors)
- 
##  **Lisensi**
Proyek ini dilisensikan di bawah Lisensi MIT. Lihat file [LICENSE](https://mit-license.org) untuk informasi lebih lanjut.







