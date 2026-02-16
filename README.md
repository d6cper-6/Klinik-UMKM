
# 🦷 KLINIK UMKM - Sistem Rekam Medis Klinik Gigi

Aplikasi web **Rekam Medis Klinik Gigi** berbasis frontend dengan penyimpanan lokal (localStorage). Dibangun untuk memudahkan pencatatan pasien, riwayat kunjungan, serta dilengkapi fitur backup/restore dan cetak dokumen.

🔗 **Demo:** [Link Demo Netlify/Vercel]  
📦 **Repo:** [Link GitHub Repository]

---

## 📋 **Daftar Isi**
- [Fitur Utama](#fitur-utama)
- [Struktur File](#struktur-file)
- [Teknologi yang Digunakan](#teknologi-yang-digunakan)
- [Cara Install & Menjalankan](#cara-install--menjalankan)
- [Panduan Penggunaan](#panduan-penggunaan)
- [Fitur Backup & Restore](#fitur-backup--restore)
- [Fitur Cetak (Print)](#fitur-cetak-print)
- [Keamanan](#keamanan)
- [Pengembangan Selanjutnya](#pengembangan-selanjutnya)
- [Kontak & Dukungan](#kontak--dukungan)

---

## ✨ **Fitur Utama**

### 1. **Manajemen Pasien**
- ✅ Tambah pasien baru dengan form lengkap
- ✅ Edit data pasien
- ✅ Hapus data pasien
- ✅ Lihat detail pasien
- ✅ Nomor Rekam Medis otomatis (format: RM-TAHUN-NOMOR)

### 2. **Pencarian & Filter**
- 🔍 Cari berdasarkan Nomor Rekam Medis
- 🔍 Cari berdasarkan Nama Pasien
- 🔍 Cari berdasarkan Alamat

### 3. **Backup & Restore Data**
- 💾 Export ke JSON (full backup)
- 📊 Export ke CSV (untuk analisis Excel)
- 📥 Import dari JSON (restore data)
- 📥 Import dari CSV (tambah data)

### 4. **Fitur Cetak**
- 🖨️ Print langsung ke printer
- 📄 Simpan sebagai PDF
- 🎨 Tampilan khusus untuk cetak (print-friendly)

### 5. **Keamanan Sederhana**
- 🔐 Halaman Login (username: `admin_klinik`, password: `adminklinik123`)
- ✏️ Edit judul klinik dengan password (`qwerty`)
- 🚪 Logout dengan backup wajib

### 6. **Responsive Design**
- 📱 Tampilan optimal di smartphone
- 💻 Tampilan desktop
- 📟 Support semua browser modern

---

## 📁 **Struktur File**

```
klinik-umkm/
│
├── 📄 index.html              # Halaman Login
├── 📄 dashboard.html          # Halaman Utama (setelah login)
├── 📄 form-pasien.html        # Form tambah pasien baru
├── 📄 form-pasien-edit.html   # Form edit pasien
├── 📄 list-pasien.html        # Daftar semua pasien + pencarian
├── 📄 detail-pasien.html      # Detail pasien + fitur print
├── 📄 import.html             # Halaman import/export data
├── 📄 logout.html             # Halaman logout dengan backup
└── 📄 README.md               # Dokumentasi proyek
```

---

## 🛠️ **Teknologi yang Digunakan**

| Teknologi | Kegunaan |
|-----------|----------|
| HTML5 | Struktur halaman |
| CSS3 | Styling & responsive design |
| JavaScript | Logika aplikasi |
| LocalStorage | Penyimpanan data di browser |
| GitHub | Version control & hosting kode |
| Netlify/Vercel | Deployment otomatis |

---

## 🚀 **Cara Install & Menjalankan**

### **Prasyarat**
- Web browser modern (Chrome, Firefox, Edge, dll)
- Akun GitHub
- Akun Netlify atau Vercel (opsional untuk hosting)

### **Langkah-langkah**

#### **1. Download / Clone Repository**
```bash
git clone https://github.com/username/klinik-umkm.git
cd klinik-umkm
```

#### **2. Buka di Browser**
- Buka file `index.html` langsung di browser
- Atau gunakan Live Server di VS Code

#### **3. Login ke Aplikasi**
```
Username: admin_klinik
Password: adminklinik123
```

#### **4. Deploy ke Netlify (Opsional)**
1. Push kode ke repository GitHub
2. Login ke [Netlify](https://netlify.com)
3. Klik "New site from Git"
4. Pilih repository GitHub Anda
5. Deploy (tanpa pengaturan khusus)

#### **5. Deploy ke Vercel (Opsional)**
1. Push kode ke GitHub
2. Login ke [Vercel](https://vercel.com)
3. Klik "New Project"
4. Import repository GitHub
5. Deploy

---

## 📖 **Panduan Penggunaan**

### **1. Halaman Login**
- Masukkan username dan password yang benar
- Setelah login akan diarahkan ke dashboard

### **2. Dashboard**
- **Edit Judul Klinik**: Klik icon pensil di samping judul, masukkan password `qwerty`
- **Menu Utama**: 
  - "Pasien Baru" → Tambah pasien
  - "Daftar List Pasien" → Lihat semua pasien
- **Dropdown (☰) di pojok kanan**:
  - Import/Restore → Manajemen backup
  - Logout → Keluar aplikasi

### **3. Form Pasien Baru**
- Isi semua data yang diperlukan (tanda * wajib diisi)
- Nomor RM akan otomatis tergenerate
- Klik "Simpan" untuk menyimpan data

### **4. Daftar Pasien**
- Gunakan kolom pencarian untuk mencari pasien
- Klik tombol aksi per baris:
  - 👁️ Detail → Lihat detail pasien
  - ✏️ Edit → Ubah data pasien
  - 🗑️ Hapus → Hapus data pasien

### **5. Detail Pasien**
- Lihat informasi lengkap pasien
- **Fitur Cetak**:
  - "Print ke Printer" → Cetak langsung
  - "Simpan sebagai PDF" → Simpan ke file PDF

### **6. Import/Export Data**
- **Export JSON**: Backup semua data
- **Export CSV**: Backup untuk Excel
- **Import JSON**: Restore dari file JSON
- **Import CSV**: Tambah data dari CSV

### **7. Logout**
- Backup data terlebih dahulu (wajib)
- Centang "Saya sudah melakukan backup"
- Masukkan password admin
- Klik "Logout"

---

## 💾 **Fitur Backup & Restore**

### **Format JSON**
- Backup lengkap semua field data pasien
- Cocok untuk restore penuh
- Contoh struktur:
```json
[
  {
    "noRm": "RM-2024-0001",
    "namaLengkap": "Budi Santoso",
    "nik": "1234567890123456",
    ...
  }
]
```

### **Format CSV**
- Backup dengan format tabel
- Bisa dibuka di Microsoft Excel
- Header: No RM, Nama Lengkap, NIK, BPJS, dll

### **Cara Backup**
1. Buka menu Import/Restore (dropdown di dashboard)
2. Pilih "Export JSON" atau "Export CSV"
3. File akan otomatis terdownload

### **Cara Restore**
1. Buka menu Import/Restore
2. Pilih file JSON atau CSV
3. Klik Import
4. Konfirmasi (untuk JSON akan mengganti semua data)

---

## 🖨️ **Fitur Cetak (Print)**

### **Print ke Printer**
- Klik tombol "Print ke Printer" di halaman detail pasien
- Pilih printer yang tersedia
- Hasil cetak sudah diformat rapi

### **Simpan sebagai PDF**
- Klik tombol "Simpan sebagai PDF"
- Di dialog print, pilih "Save as PDF"
- Tentukan lokasi penyimpanan

### **Tampilan Print**
- Header dengan logo & nama klinik
- Data pasien tersusun rapi
- Riwayat kunjungan
- Footer dengan tanda tangan

---

## 🔐 **Keamanan**

### **Login**
- Username: `admin_klinik`
- Password: `adminklinik123`

### **Edit Judul Klinik**
- Password: `qwerty`
- Hanya yang tahu password bisa mengubah nama klinik

### **Logout**
- Wajib backup data
- Password login diperlukan untuk konfirmasi

### **Penyimpanan**
- Data tersimpan di localStorage browser masing-masing
- Tidak ada data yang dikirim ke server
- Backup manual diperlukan untuk memindahkan data

---

## 🚧 **Pengembangan Selanjutnya**

Fitur yang bisa ditambahkan di masa depan:

- [ ] **Riwayat Kunjungan** - Catatan kunjungan per pasien
- [ ] **Laporan Statistik** - Grafik kunjungan, penyakit terbanyak
- [ ] **Jadwal Praktik** - Manajemen jadwal dokter
- [ ] **Antrian** - Sistem nomor antrian
- [ ] **Resep Digital** - Catatan resep obat
- [ ] **Invoice & Pembayaran** - Sistem billing
- [ ] **Multiple User** - Admin, Dokter, Kasir
- [ ] **Cloud Sync** - Sinkronisasi ke cloud (Firebase)
- [ ] **QR Code** - Scan untuk akses cepat data pasien

---

## 🤝 **Kontak & Dukungan**

Jika ada pertanyaan atau ingin melanjutkan pengembangan:

- **Author**: [Nama Anda]
- **Email**: [email@example.com]
- **GitHub**: [github.com/username]
- **Dibuat**: 2024
- **Versi**: 1.0.0

---

## 📝 **Lisensi**

Proyek ini dilisensikan di bawah **MIT License** - lihat file [LICENSE](LICENSE) untuk detail lebih lanjut.

---

## 🙏 **Credit**

Terima kasih kepada:
- Semua kontributor
- Pengguna yang memberikan masukan
- Komunitas open source

---

**Selamat menggunakan!** 🎉

Dibuat dengan ❤️ untuk kemajuan UMKM Klinik Gigi Indonesia
```

## 🎯 **Apa yang Ada di README.md Ini:**

1. **Pendahuluan** - Gambaran umum proyek
2. **Fitur Utama** - Daftar lengkap fitur dengan emoji
3. **Struktur File** - Tabel file dan fungsinya
4. **Teknologi** - Stack yang digunakan
5. **Cara Install** - Langkah-langkah setup
6. **Panduan Penggunaan** - Tutorial lengkap per halaman
7. **Fitur Backup** - Penjelasan format JSON & CSV
8. **Fitur Print** - Cara mencetak dan PDF
9. **Keamanan** - Password dan sistem login
10. **Roadmap** - Fitur yang bisa ditambahkan nanti
11. **Kontak** - Informasi pengembang

## 📌 **Cara Menggunakan README.md:**

1. **Simpan file ini sebagai `README.md`** di root folder proyek
2. **Edit bagian-bagian yang perlu**:
   - Ganti `[Link Demo]` dengan URL deploy
   - Ganti `[Link GitHub]` dengan URL repo
   - Ganti informasi kontak (email, username GitHub)
3. **Push ke GitHub** - README akan tampil di halaman utama repo

Dengan README ini, ketika Anda kembali ke proyek setelah beberapa waktu, Anda tinggal membaca dokumentasi untuk mengingat kembali semua fitur dan cara kerjanya. Juga berguna jika ingin mengajak orang lain berkontribusi.
