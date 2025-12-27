# Sistem Pendukung Keputusan Pemilihan Supplier Terbaik (SWARA)

Aplikasi web sederhana untuk membantu pengambilan keputusan dalam memilih supplier terbaik menggunakan metode **SWARA (Step-wise Weight Assessment Ratio Analysis)**.  
Sistem ini dikembangkan sebagai studi kasus pada **Toko Fajar Mario, Kolaka – Sulawesi Tenggara**.

---

## 📌 Ringkasan
Sistem Pendukung Keputusan (SPK) ini digunakan untuk:
- Menentukan bobot kriteria menggunakan metode SWARA
- Menilai alternatif supplier berdasarkan kriteria yang telah ditentukan
- Menghasilkan ranking supplier terbaik secara objektif dan transparan

Metode SWARA termasuk dalam **Multi-Criteria Decision Making (MCDM)** dan cocok digunakan ketika kriteria memiliki tingkat kepentingan yang berurutan.

---

## 🧮 Metode SWARA
**SWARA (Step-wise Weight Assessment Ratio Analysis)** adalah metode pembobotan kriteria yang diperkenalkan oleh Kersuliene et al. (2010).

### Langkah-langkah SWARA:
1. Mengurutkan kriteria berdasarkan tingkat kepentingan (urutan 1 = paling penting)
2. Menentukan nilai **Sj** (tingkat penurunan kepentingan relatif terhadap kriteria sebelumnya)
   - Kriteria pertama: `Sj = 0`
3. Menghitung koefisien:
Kj = 1 + Sj

markdown
Salin kode
4. Menghitung bobot sementara:
Q1 = 1
Qj = Q(j-1) / Kj

markdown
Salin kode
5. Normalisasi bobot akhir:
Wj = Qj / ΣQj

yaml
Salin kode

### Keunggulan SWARA:
- Mudah dipahami dan diimplementasikan
- Bobot ditentukan secara berurutan dan logis
- Transparan dan dapat dipertanggungjawabkan
- Cocok untuk SPK berbasis prioritas kriteria

---

## 🚀 Fitur Sistem
- Kelola data kriteria (urutan, jenis, nilai Sj)
- Kelola data supplier
- Input nilai supplier untuk setiap kriteria (skala 1–5)
- Perhitungan bobot SWARA otomatis
- Normalisasi dan perhitungan nilai akhir
- Ranking supplier (Top 3 + tabel lengkap)
- Dashboard statistik sistem

---

## 🛠️ Teknologi yang Digunakan

### Backend
- PHP 8.2+
- MySQL / MariaDB
- XAMPP (Apache + PHP + MySQL)

### Frontend
- HTML5
- CSS3
- Bootstrap 5.3
- JavaScript
- Bootstrap Icons

> ⚠️ **Catatan Keamanan**  
> Sistem ini dirancang untuk penggunaan lokal / demo.  
> Tidak menggunakan sistem login. Untuk produksi, disarankan menambahkan autentikasi dan otorisasi.

---

## 📦 Persyaratan Sistem
- XAMPP (Apache, PHP, MySQL)
- Web browser (Chrome / Firefox)
- File database: `supplier_swara.sql`

---

## ⚙️ Cara Menjalankan (Windows + XAMPP)

1. Salin folder proyek ke:
C:\xampp\htdocs\supplier4

markdown
Salin kode
atau atur VirtualHost ke folder proyek.

2. Import database ke MySQL:
- Melalui **phpMyAdmin** → Import → pilih `supplier_swara.sql`
- Atau via command line:
  ```bash
  mysql -u root -p < supplier_swara.sql
  ```

3. Sesuaikan koneksi database di `config.php`:
```php
host     = localhost
username = root
password = (kosong)
database = supplier_swara
Jalankan aplikasi melalui browser:

bash
Salin kode
http://localhost/supplier4/index.php
```
## 🧭 Alur Penggunaan Sistem
1. Kelola Data Kriteria  
2. Kelola Data Supplier  
3. Input Nilai Supplier  
4. Hitung Bobot SWARA  
5. Lihat Perhitungan & Ranking Supplier  

---

## 🏪 Studi Kasus
**Toko Fajar Mario**  
📍 Kolaka, Sulawesi Tenggara  

Sistem ini dikembangkan untuk membantu toko dalam memilih supplier terbaik berdasarkan:
- Harga  
- Kualitas  
- Ketepatan pengiriman  
- Ketersediaan stok  
- Pelayanan  

---

## 📄 Informasi Tambahan
- **Versi:** 1.0  
- **Tahun:** 2025  
- **Lisensi:** Bebas digunakan untuk keperluan akademik dan pembelajaran  

---

## ✅ Status
- ✔ Sistem siap digunakan  
- ✔ Database terintegrasi  
- ✔ Metode SWARA terimplementasi penuh  
