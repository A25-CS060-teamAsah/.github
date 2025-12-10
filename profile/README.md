# Lead Scoring Portal - Panduan Pengguna

![Lead Scoring Logo](profilelogo_leadscoring.svg)

**Platform Prediksi Leads Berbasis AI untuk Industri Perbankan**

Maksimalkan efisiensi tim sales dengan fokus pada leads berpotensi tinggi menggunakan teknologi Machine Learning

---

## 📋 Daftar Isi

- [Tentang Lead Scoring Portal](#-tentang-lead-scoring-portal)
- [Fitur Utama](#-fitur-utama)
  - [1. Dashboard Analytics](#1-dashboard-analytics)
  - [2. Manajemen Leads](#2-manajemen-leads)
  - [3. Analitik Prediksi](#3-analitik-prediksi)
  - [4. Monitor Auto-Predict](#4-monitor-auto-predict)
- [Cara Menggunakan Platform](#-cara-menggunakan-platform)
  - [1. Login ke Platform](#1-login-ke-platform)
  - [2. Mengelola Data Leads](#2-mengelola-data-leads)
  - [3. Melihat Dashboard Analytics](#3-melihat-dashboard-analytics)
  - [4. Upload Data via CSV](#4-upload-data-via-csv)
- [Tim Pengembang](#-tim-pengembang)

---

## 💡 Tentang Lead Scoring Portal

Lead Scoring Portal adalah platform berbasis web yang menggunakan teknologi Machine Learning (ML) untuk memprediksi probabilitas nasabah bank berlangganan produk deposito berjangka. Platform ini membantu tim sales mengidentifikasi dan memprioritaskan leads dengan potensi tinggi, sehingga meningkatkan efisiensi dan conversion rate.

### Manfaat Utama

- 🎯 **Prioritas Leads** - Identifikasi leads dengan probabilitas tinggi secara otomatis
- 📊 **Analitik Real-time** - Dashboard dengan metrik dan visualisasi data terkini
- ⚡ **Prediksi Otomatis** - Sistem auto-predict berjalan setiap 2 menit
- 🔍 **Filter Lanjutan** - Pencarian dan filter multi-parameter untuk menemukan leads spesifik
- 📤 **Bulk Upload** - Import data customer dalam jumlah besar via CSV
- 🔐 **Keamanan Data** - Autentikasi berbasis JWT dengan role-based access control

---

## ✨ Fitur Utama

### 1. Dashboard Analytics

**Lokasi**: Halaman utama setelah login (`/dashboard`)

**Fitur:**

- **Total Leads Card** - Menampilkan total customer dengan trend bulanan
- **High Priority Leads** - Jumlah leads dengan probability score ≥50%
- **Average Score** - Rata-rata skor prediksi semua leads
- **Top Priority Leads Table** - 6 customer dengan skor tertinggi
- **Monthly Trend Chart** - Visualisasi trend 6 bulan terakhir

**Cara Mengakses:**

Setelah login, Anda akan langsung diarahkan ke halaman Dashboard. Di sini Anda dapat melihat overview lengkap tentang performa leads dan prediksi.

### 2. Manajemen Leads

**Lokasi**: Menu "Lead List" di sidebar (`/dashboard/leadList`)

**Fitur:**

- **Pencarian Nama** - Cari customer berdasarkan nama, pekerjaan, pendidikan, atau status pernikahan
- **Filter Prioritas** - Filter berdasarkan skor: All / High (≥75%) / Medium (50-75%) / Low (<50%)
- **Filter Lanjutan** - Panel filter dengan 6 parameter:
  - **Rentang Usia** - Filter berdasarkan usia minimum dan maksimum
  - **Jenis Pekerjaan** - Pilih dari 11+ kategori pekerjaan
  - **Tingkat Pendidikan** - Primary, Secondary, Tertiary
  - **Status Pernikahan** - Single, Married, Divorced
  - **Housing Loan** - Filter berdasarkan kepemilikan pinjaman rumah
  - **Personal Loan** - Filter berdasarkan kepemilikan pinjaman pribadi
- **Tambah Lead Baru** - Form untuk menambahkan customer baru
- **Edit & Hapus** - Kelola data customer yang sudah ada
- **Upload CSV** - Import data customer dalam jumlah besar
- **Batch Predict** - Prediksi untuk multiple customer sekaligus

**Cara Menggunakan Filter Lanjutan:**

1. Klik tombol "Advanced Filters" di bagian atas halaman Lead List
2. Panel filter akan muncul dengan berbagai opsi
3. Isi filter sesuai kebutuhan (misalnya: usia 30-50, pekerjaan technician, pendidikan secondary)
4. Badge "Active" akan muncul jika ada filter yang aktif
5. Hasil akan otomatis ter-update saat filter berubah
6. Klik "Clear Filters" untuk mereset semua filter

### 3. Analitik Prediksi

**Lokasi**: Menu "Analytics" di sidebar (`/dashboard/analytics`)

**Fitur:**

- **Total Predictions** - Jumlah total prediksi yang telah dilakukan
- **Average Score** - Rata-rata skor probabilitas
- **Priority Distribution** - Distribusi leads berdasarkan prioritas:
  - High Priority (≥75%) - Hijau
  - Medium Priority (50-75%) - Kuning
  - Low Priority (<50%) - Merah
- **Coverage Statistics** - Statistik coverage prediksi:
  - Customer dengan prediksi
  - Customer tanpa prediksi
- **Conversion Rate** - Persentase prediksi positif (will_subscribe = true)
- **Visual Charts** - Grafik batang dan progress bar untuk visualisasi data

**Kegunaan:**

Halaman ini membantu Anda memahami performa keseluruhan sistem prediksi dan mengidentifikasi area yang perlu perhatian lebih.

### 4. Monitor Auto-Predict

**Lokasi**: Menu "Admin" di sidebar (`/dashboard/admin`) - **Hanya untuk Admin**

**Fitur:**

- **Status Sistem** - Indikator apakah cron job sedang berjalan atau idle
- **Cron Enabled** - Status aktif/nonaktif auto-predict
- **Schedule** - Jadwal eksekusi (default: setiap 2 menit)
- **Last Run** - Waktu eksekusi terakhir
- **Next Run** - Prediksi waktu eksekusi berikutnya
- **Total Runs** - Counter total eksekusi
- **Cache Statistics** - Statistik performa cache:
  - Jumlah prediksi yang di-cache
  - Cache hits vs misses
  - Hit rate percentage
- **Manual Trigger** - Tombol untuk memicu prediksi secara manual

**Catatan:**

Fitur ini hanya dapat diakses oleh user dengan role **Admin**. User dengan role **Sales** tidak akan melihat menu ini di sidebar.

---

## 📝 Cara Menggunakan Platform

### 1. Login ke Platform

#### Langkah 1: Akses Halaman Login

Buka browser Anda dan akses URL platform Lead Scoring Portal. Anda akan melihat halaman login seperti gambar di bawah ini.

![Halaman Login - Form login dengan field email dan password](profileLogin.svg)

#### Langkah 2: Masukkan Kredensial

Masukkan email dan password Anda:

**Default Login (untuk testing):**

- **Admin**:
  - Email: `admin@leadscoring.com`
  - Password: `password123`
- **Sales**:
  - Email: `sales1@leadscoring.com`
  - Password: `password123`

#### Langkah 3: Klik Tombol Login

Setelah memasukkan kredensial, klik tombol "Login" untuk masuk ke dashboard.

**Catatan Keamanan:**

- Pastikan Anda menggunakan kredensial yang valid
- Token JWT akan disimpan di browser untuk autentikasi
- Jika token expired, Anda akan otomatis diarahkan ke halaman login

---

### 2. Mengelola Data Leads

#### Langkah 1: Akses Halaman Lead List

Setelah login, klik menu **"Lead List"** di sidebar kiri untuk mengakses halaman manajemen leads.

![Halaman Lead List - Tampilan daftar leads dengan filter dan search bar](profileLeadList.svg)

#### Langkah 2: Mencari Leads

Gunakan **search bar** di bagian atas untuk mencari customer berdasarkan:

- Nama
- Pekerjaan
- Pendidikan
- Status pernikahan

Contoh: Ketik "John" untuk mencari semua customer dengan nama mengandung "John".

#### Langkah 3: Filter Berdasarkan Prioritas

Gunakan **tab filter** di bawah search bar:

- **All** - Tampilkan semua leads
- **High** - Leads dengan skor ≥75%
- **Medium** - Leads dengan skor 50-75%
- **Low** - Leads dengan skor <50%

#### Langkah 4: Menggunakan Filter Lanjutan

1. Klik tombol **"Advanced Filters"** untuk membuka panel filter
2. Isi filter sesuai kebutuhan:
   - **Min Age / Max Age**: Masukkan rentang usia (contoh: 30-50)
   - **Job**: Pilih jenis pekerjaan dari dropdown
   - **Education**: Pilih tingkat pendidikan
   - **Marital**: Pilih status pernikahan
   - **Housing Loan**: Pilih Yes/No/All
   - **Personal Loan**: Pilih Yes/No/All
3. Badge **"Active"** akan muncul jika ada filter yang aktif
4. Hasil akan otomatis ter-update
5. Klik **"Clear Filters"** untuk mereset

![Panel Advanced Filters - Tampilan filter lanjutan dengan berbagai opsi](profileAdvancedFilters.svg)

#### Langkah 5: Menambah Lead Baru

1. Klik tombol **"Add Customer"** di bagian atas halaman
2. Form modal akan muncul
3. Isi semua field yang diperlukan:
   - Name (Nama)
   - Age (Usia)
   - Job (Pekerjaan)
   - Marital (Status Pernikahan)
   - Education (Pendidikan)
   - Contact (Tipe Kontak)
   - Month & Day of Week
   - Campaign, Pdays, Previous, Poutcome
   - Balance (Opsional)
4. Klik **"Save"** untuk menyimpan
5. Sistem akan otomatis melakukan prediksi untuk customer baru

![Form Tambah Customer - Modal form untuk menambah customer baru](profileAddCustomer.svg)

#### Langkah 6: Melihat Detail Lead

1. Klik pada card lead untuk melihat detail lengkap
2. Modal detail akan muncul menampilkan:
   - Informasi lengkap customer
   - Skor prediksi terbaru
   - Probabilitas berlangganan
   - History prediksi (jika ada)
3. Dari modal ini, Anda dapat:
   - **Edit** customer
   - **Delete** customer
   - **Predict** ulang untuk customer ini

![Modal Detail Lead - Tampilan detail lengkap customer dengan skor prediksi](profileLeadDetail.svg)

#### Langkah 7: Batch Predict

1. Centang beberapa leads yang ingin diprediksi
2. Klik tombol **"Batch Predict"**
3. Sistem akan melakukan prediksi untuk semua leads yang dipilih
4. Progress akan ditampilkan di notifikasi

---

### 3. Melihat Dashboard Analytics

#### Langkah 1: Akses Dashboard

Setelah login, Anda akan langsung diarahkan ke halaman Dashboard. Atau klik menu **"Dashboard"** di sidebar.

![Halaman Dashboard - Overview metrics dan top priority leads](profileDashboard.svg)

#### Langkah 2: Memahami Metrik

Dashboard menampilkan 4 kartu metrik utama:

1. **Total Leads** - Total jumlah customer dengan indikator trend bulanan
2. **High Priority** - Jumlah leads dengan skor ≥50%
3. **Avg Score** - Rata-rata skor prediksi
4. **Monthly Trend** - Grafik trend 6 bulan terakhir

#### Langkah 3: Melihat Top Priority Leads

Di bagian bawah dashboard, terdapat tabel **"Top Priority Leads"** yang menampilkan 6 customer dengan skor tertinggi. Tabel ini menampilkan:

- Nama customer
- Usia
- Pekerjaan
- Skor prediksi
- Status (Will Subscribe / Won't Subscribe)

Klik pada baris tabel untuk melihat detail lengkap customer.

#### Langkah 4: Mengakses Analytics Detail

Klik menu **"Analytics"** di sidebar untuk melihat analitik prediksi yang lebih detail, termasuk:

- Distribusi prioritas (High/Medium/Low)
- Conversion rate
- Coverage statistics
- Visual charts

![Halaman Analytics - Statistik prediksi dengan visualisasi chart](profileAnalytics.svg)

---

### 4. Upload Data via CSV

#### Langkah 1: Download Template CSV

1. Klik menu **"Lead List"** di sidebar
2. Klik tombol **"Upload CSV"** di bagian atas halaman
3. Di modal yang muncul, klik **"Download Template"**
4. File CSV template akan terunduh dengan nama `customer_template.csv`

**Format Template CSV:**

```csv
name,age,job,marital,education,default,housing,loan,contact,month,day_of_week,campaign,pdays,previous,poutcome,balance
John Doe,30,technician,married,secondary,false,true,false,cellular,may,mon,2,999,0,unknown,1500.50
Jane Smith,45,management,single,tertiary,false,false,false,telephone,jun,fri,1,999,0,success,2500.75
```

#### Langkah 2: Menyiapkan File CSV

1. Buka file template yang sudah diunduh
2. Isi data customer sesuai format template
3. Pastikan:
   - Header kolom sesuai dengan template
   - Format data benar (boolean: `true`/`false`, angka untuk usia, dll)
   - Tidak ada baris kosong di tengah file
   - Encoding file adalah UTF-8

**Catatan Penting:**

- Kolom `balance` adalah opsional (bisa dikosongkan, akan default ke 0)
- Kolom boolean (`default`, `housing`, `loan`) harus berisi `true` atau `false`
- Usia harus antara 18-100
- Pastikan semua kolom required terisi

#### Langkah 3: Upload File CSV

1. Klik tombol **"Upload CSV"** di halaman Lead List
2. Di modal yang muncul, klik **"Choose File"** atau drag & drop file CSV
3. File yang dipilih akan muncul di preview
4. Klik **"Upload"** untuk memproses file
5. Sistem akan:
   - Memvalidasi struktur CSV
   - Memvalidasi setiap baris data
   - Menampilkan summary hasil upload
   - Menyimpan data yang valid ke database
   - Otomatis melakukan prediksi untuk customer baru

![Modal Upload CSV - Tampilan upload CSV dengan drag & drop](profileCSVUpload.svg)

#### Langkah 4: Memeriksa Hasil Upload

Setelah upload selesai, Anda akan melihat notifikasi dengan informasi:

- Total records dalam file
- Jumlah records yang valid
- Jumlah records yang invalid (beserta error-nya)
- Jumlah customer yang berhasil dibuat

Jika ada error, periksa pesan error untuk mengetahui baris mana yang bermasalah dan perbaiki file CSV Anda.

**Contoh Response:**

```json
{
  "success": true,
  "message": "CSV upload processed",
  "summary": {
    "totalRecordsInFile": 100,
    "validRecords": 95,
    "invalidRecordsDuringValidation": 5,
    "successfullyCreated": 94,
    "failedToCreate": 1
  }
}
```

---

## 🔐 Role & Akses

### Admin

User dengan role **Admin** memiliki akses penuh ke semua fitur:

- ✅ Dashboard Analytics
- ✅ Manajemen Leads (CRUD)
- ✅ Upload CSV
- ✅ Analytics & Reports
- ✅ **Auto-Predict Monitor** (khusus admin)
- ✅ Register user baru

### Sales

User dengan role **Sales** memiliki akses terbatas:

- ✅ Dashboard Analytics
- ✅ Manajemen Leads (CRUD)
- ✅ Upload CSV
- ✅ Analytics & Reports
- ❌ Auto-Predict Monitor (tidak dapat diakses)
- ❌ Register user baru (hanya admin yang bisa)

---

## 🎯 Tips Penggunaan

### 1. Prioritaskan High Priority Leads

- Gunakan filter **"High Priority"** untuk melihat leads dengan skor ≥75%
- Fokus pada leads ini karena memiliki probabilitas tinggi untuk berlangganan
- Hubungi leads ini terlebih dahulu untuk meningkatkan conversion rate

### 2. Gunakan Filter Lanjutan untuk Segmentasi

- Kombinasikan beberapa filter untuk menemukan segment leads spesifik
- Contoh: Leads usia 30-50, pekerjaan management, dengan housing loan
- Simpan kombinasi filter yang sering digunakan

### 3. Monitor Auto-Predict

- Sebagai admin, pantau halaman Auto-Predict Monitor secara berkala
- Pastikan cron job berjalan dengan baik
- Periksa cache statistics untuk optimasi performa

### 4. Upload CSV untuk Bulk Import

- Gunakan fitur upload CSV untuk import data dalam jumlah besar
- Pastikan format CSV sesuai template untuk menghindari error
- Validasi data sebelum upload untuk memastikan kualitas

### 5. Gunakan Search untuk Quick Access

- Gunakan search bar untuk menemukan customer dengan cepat
- Search mendukung pencarian berdasarkan nama, pekerjaan, pendidikan, dan status pernikahan

---

## 🆘 Troubleshooting

### Masalah: Tidak bisa login

**Solusi:**

- Pastikan email dan password benar
- Periksa koneksi internet
- Clear cache browser dan coba lagi
- Hubungi admin jika masalah berlanjut

### Masalah: CSV upload gagal

**Solusi:**

- Pastikan format CSV sesuai template
- Periksa apakah semua kolom required terisi
- Validasi format data (boolean, angka, dll)
- Periksa ukuran file (max 10MB)
- Lihat pesan error untuk detail masalah

### Masalah: Prediksi tidak muncul

**Solusi:**

- Tunggu beberapa saat (auto-predict berjalan setiap 2 menit)
- Klik "Predict" manual untuk customer tertentu
- Periksa status Auto-Predict Monitor (untuk admin)
- Pastikan ML service berjalan dengan baik

### Masalah: Filter tidak bekerja

**Solusi:**

- Pastikan format input benar (angka untuk usia, dll)
- Clear semua filter dan coba lagi
- Refresh halaman
- Periksa koneksi ke backend

---

## 👥 Tim Pengembang

**Team A25-CS060** - Asah 2025

### Machine Learning Team

| ID           | Nama   | Institusi   |
| ------------ | ------ | ----------- |
| MC129D5Y1944 | [Nama] | [Institusi] |
| MC129D5X0173 | [Nama] | [Institusi] |


### Frontend & Backend Team

| ID           | Nama   | Institusi   |
| ------------ | ------ | ----------- |
| FC129D5Y1933 | Ahmad Faris Al Aziz | Institut Pertanian Bogor |
| FC211D5Y1095 | [Nama] | [Institusi] |
| FC229D5Y0897 | [Nama] | [Institusi] |

---

## 📞 Kontak & Support

Untuk pertanyaan atau bantuan lebih lanjut, silakan hubungi tim pengembang atau buka issue di repository GitHub.

---

**Versi Dokumen**: 1.0  
**Last Updated**: Desember 2025  
**Status**: ✅ Production Ready

---

<p align="center">
  <a href="https://leadscoring.example.com">www.leadscoring.example.com</a>
</p>
