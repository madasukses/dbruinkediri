# 📋 SIM-DBR
### Sistem Informasi Manajemen Daftar Barang Ruangan
**UIN Syekh Wasil Kediri**

---

## Tentang

SIM-DBR adalah aplikasi web untuk mengelola inventaris aset barang ruangan (DBR) di lingkungan UIN Syekh Wasil Kediri. Dibangun sebagai aplikasi single-page yang ringan, bisa diakses dari browser maupun HP.

---

## Fitur

- **Dashboard** — ringkasan total aset, kondisi baik/perbaikan/rusak per unit
- **Master Data** — kelola barang, lokasi ruangan, PIC/Kasub Bag, dan user
- **Input DBR** — input dan verifikasi kondisi barang per ruangan
- **Laporan** — rekap per ruangan dengan export PDF berkop UIN
- **Multi role** — Super Admin (Bagian Umum) dan Admin Fakultas
- **Responsive** — bisa dipakai di HP maupun desktop
- **Dark/Light mode**

---

## Stack

| Layer | Teknologi |
|-------|-----------|
| Frontend | HTML + Vanilla JS (single file) |
| Database | Supabase (PostgreSQL) |
| Hosting | GitHub Pages |

---

## Role & Akses

| Role | Siapa | Akses |
|------|-------|-------|
| `superadmin` | Bagian Umum | Penuh — semua unit, kelola user |
| `admin_fakultas` | Admin per unit | Edit data unit sendiri saja |

---

## Struktur Project

```
sim-dbr/
├── index.html              ← Aplikasi utama
├── images/
│   └── uin.png             ← Logo UIN Syekh Wasil Kediri
├── supabase_schema.sql     ← Schema database Supabase
└── README.md
```

---


## Penggunaan

### Alur Input DBR

```
Login → DBR → Input / Verifikasi
→ Pilih Gedung → Pilih Ruangan
→ Tambah Barang (nama autocomplete dari master)
→ Isi Qty & Kondisi (Baik / Perbaikan / Rusak)
→ Simpan
```

### Cetak PDF DBR

```
Laporan → cari ruangan → klik tombol PDF
→ halaman cetak terbuka otomatis
→ Save as PDF atau Print
```

---

## Lisensi

Untuk penggunaan internal UIN Syekh Wasil Kediri.
