
# 🐟 LeleKu — Catfish Farm Management
> *"Manage Your Farm, Grow Your Business."*

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)

LeleKu adalah aplikasi mobile bertema *Catfish Farm Management System* yang dirancang untuk membantu pemilik peternakan lele dalam mengelola kegiatan operasional usaha. Aplikasi ini memungkinkan admin untuk memantau stok lele, mengelola pesanan pelanggan, mencatat pendapatan, dan melihat riwayat aktivitas dalam satu platform.

Proyek ini dikembangkan menggunakan Flutter dan Dart sebagai implementasi pembelajaran pengembangan aplikasi mobile, dengan Supabase sebagai layanan backend dan PostgreSQL sebagai database.

---

## 📋 Fitur Utama

| Fitur | Deskripsi |
| :--- | :--- |
| 📊 **Dashboard** | Menampilkan ringkasan stok, pendapatan, dan pesanan terbaru. |
| 🐟 **Stock Management** | Mengelola stok lele masuk dan keluar, berat stok, serta kategori ukuran. |
| 📦 **Order Management** | Membuat dan mengelola pesanan pelanggan beserta detail pesanan. |
| 💰 **Income Tracking** | Menampilkan ringkasan pendapatan dan statistik penjualan. |
| 📜 **Activity History** | Menampilkan riwayat aktivitas stok, pesanan, dan transaksi. |
| 🧾 **Order Details** | Menampilkan detail pelanggan, jumlah stok yang dibeli, dan rincian pembayaran. |
| ➕ **Add Stock** | Mencatat penambahan stok lele beserta hasil penimbangan dan pemeriksaan. |
| 👤 **Admin Access** | Menyediakan akses aplikasi untuk admin atau pemilik peternakan. |
| 📱 **Mobile UI** | Tampilan mobile dengan desain minimalis dan dominasi warna hijau. |

---

## 🔄 Alur Sistem

```text
Admin Login
     |
     v
Dashboard
     |
     +----> Manajemen Stok
     |          |
     |          +----> Tambah Stok
     |          |
     |          +----> Catat Stok Keluar
     |
     +----> Data Pesanan
     |          |
     |          +----> Buat Pesanan
     |          |
     |          +----> Detail Pesanan
     |
     +----> Pendapatan
     |
     +----> Riwayat Aktivitas
     |
     v
Admin Logout
```

**Alur pengelolaan stok:**

```text
Input Data Stok
       |
       v
Validasi Data
       |
       v
Simpan Data Stok
       |
       v
Perbarui Ringkasan Stok
       |
       v
Tampilkan Riwayat Aktivitas
```

**Alur pengelolaan pesanan:**

```text
Input Data Pelanggan
       |
       v
Pilih Rincian Pesanan
       |
       v
Hitung Berat dan Total Harga
       |
       v
Konfirmasi Pesanan
       |
       v
Perbarui Stok dan Data Transaksi
       |
       v
Tampilkan Detail Pesanan
```

---

## 🛠️ Tech Stack

- **Frontend:** Flutter
- **Programming Language:** Dart
- **Backend & Authentication:** Supabase
- **Database:** PostgreSQL
- **State Management:** Riverpod (opsional, sesuai implementasi)
- **Navigation:** GoRouter (opsional, sesuai implementasi)
- **Charts:** FL Chart (opsional, sesuai implementasi)
- **Development Tools:** Flutter SDK, Dart SDK, Git, GitHub
- **UI/UX Design:** Figma

### Konsep Flutter

- Widget dan Widget Composition
- StatelessWidget dan StatefulWidget
- State Management untuk memperbarui tampilan aplikasi
- Form Input dan Validasi Data
- Navigasi antarhalaman
- Integrasi API dan Database
- CRUD (Create, Read, Update, Delete)
- Asynchronous Programming menggunakan `async` dan `await`
- Data Modeling untuk stok, pesanan, dan transaksi

---

## 📁 Struktur Project

```text
leleku/
├── android/
├── ios/
├── assets/
│   ├── images/
│   └── icons/
├── lib/
│   ├── core/
│   │   ├── constants/
│   │   ├── theme/
│   │   └── utils/
│   ├── models/
│   ├── services/
│   │   └── supabase_service.dart
│   ├── features/
│   │   ├── auth/
│   │   ├── dashboard/
│   │   ├── stock/
│   │   ├── orders/
│   │   ├── income/
│   │   └── activity_history/
│   ├── shared/
│   │   ├── widgets/
│   │   └── navigation/
│   ├── app.dart
│   └── main.dart
├── test/
├── pubspec.yaml
└── README.md
```

---

## 🚀 Cara Menjalankan Project

**1. Clone repository**

```bash
git clone https://github.com/username/leleku.git
cd leleku
```

**2. Install dependencies**

```bash
flutter pub get
```

**3. Konfigurasi Supabase**

Siapkan proyek Supabase, kemudian konfigurasi URL proyek dan publishable key melalui environment configuration yang digunakan aplikasi.

Pastikan konfigurasi autentikasi dan kebijakan Row Level Security (RLS) telah diterapkan sebelum menggunakan data produksi.

**4. Jalankan aplikasi**

```bash
flutter run
```

**5. Jalankan pengujian**

```bash
flutter test
```

> Pastikan Flutter SDK, Dart SDK, Android Studio atau perangkat Android, serta konfigurasi proyek sudah sesuai sebelum menjalankan aplikasi.

---

## 📌 Catatan Pengembangan

- Aplikasi dirancang untuk satu jenis aktor, yaitu admin atau pemilik peternakan.
- Fitur manajemen stok mencakup pencatatan berat lele dan perubahan stok.
- Fitur pesanan mencakup data pelanggan, rincian pembelian, dan pembayaran.
- Data pendapatan dihitung berdasarkan transaksi yang tercatat.
- Supabase dan PostgreSQL digunakan apabila integrasi backend telah diterapkan.
- Struktur folder dapat disesuaikan dengan implementasi aktual proyek.
- Package tambahan digunakan sesuai kebutuhan fitur aplikasi.

---

## 🔮 Future Development

- Dashboard dengan statistik operasional yang lebih lengkap.
- Penyempurnaan pencatatan stok dan riwayat penimbangan.
- Pengelolaan status pesanan dan pembayaran.
- Filter dan pencarian riwayat transaksi.
- Laporan pendapatan berdasarkan periode.
- Ekspor laporan transaksi ke PDF atau Excel.
- Notifikasi stok dan pesanan.
- Pengembangan fitur backup dan keamanan data.

---

<p align="center">
  <strong>LELEKU</strong><br>
  <em>"Manage Your Farm, Grow Your Business."</em><br><br>
  Made with Flutter and Dart for Catfish Farm Management.
</p>
