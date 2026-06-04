# SIM-DBR — Sistem Informasi Manajemen Daftar Barang Ruangan

Aplikasi inventaris aset ruangan berbasis web. Frontend statis (HTML/CSS/JS) di-host via GitHub Pages atau Vercel, backend menggunakan Google Apps Script sebagai API, dan data tersimpan di Google Sheets.

## Stack

| Layer    | Teknologi              |
|----------|------------------------|
| Frontend | HTML + Vanilla JS      |
| Backend  | Google Apps Script     |
| Database | Google Sheets          |
| Hosting  | GitHub Pages / Vercel  |

## Struktur Project

```
sim-dbr/
├── index.html              ← Aplikasi utama (single file)
├── apps-script/
│   ├── Code.gs             ← Backend API (deploy ke Apps Script)
│   └── appsscript.json     ← Manifest Apps Script
├── docs/
│   └── SETUP.md            ← Panduan setup lengkap
└── README.md
```

## Role & Akses

| Role             | Siapa              | Akses                          |
|------------------|--------------------|-------------------------------|
| `superadmin`     | Kepala Bag. Umum   | Penuh semua unit + kelola user |
| `bmn`            | Staf Bag. Umum     | Lihat & laporan semua unit     |
| `admin_fakultas` | Admin per unit     | Edit data unit sendiri saja    |

## Setup Cepat

Lihat **[docs/SETUP.md](docs/SETUP.md)** untuk panduan lengkap.

### Ringkasan

1. Import `SIM_DBR_GoogleSheet_Template.xlsx` ke Google Drive
2. Buka **Extensions → Apps Script**, paste isi `apps-script/Code.gs`
3. Isi `SS_ID` di Code.gs dengan Spreadsheet ID
4. Deploy sebagai Web App → salin URL
5. Isi `API_URL` di `index.html` dengan URL tadi
6. Push ke GitHub → aktifkan GitHub Pages

## Lisensi

MIT
