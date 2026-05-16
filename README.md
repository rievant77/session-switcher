# Session Switcher 2

Browser extension untuk menyimpan dan beralih antar sesi (session) pada website. Berguna untuk mengelola banyak akun pada satu situs tanpa perlu login/logout berulang kali.

## Fitur

- **Simpan Sesi** — Simpan cookies dan local/session storage dari tab aktif sebagai sesi bernama
- **Switch Sesi** — Beralih antar sesi yang tersimpan dengan satu klik
- **Sesi Per-Domain** — Setiap sesi disimpan berdasarkan domain, sehingga tidak saling mengganggu
- **New Session** — Buat sesi baru (bersih) tanpa data apapun
- **Clear Session** — Hapus semua data sesi pada domain aktif
- **Rename & Delete** — Kelola sesi yang tersimpan
- **Replace Session** — Timpa sesi yang sudah ada dengan data sesi saat ini
- **Export/Import** — Backup dan restore sesi dalam format JSON
- **Grid & List View** — Tampilan daftar sesi bisa diubah sesuai preferensi
- **Cross-Browser** — Mendukung Chrome (Manifest V3) dan Firefox (Gecko)

## Instalasi

### Chrome / Edge / Brave
1. Buka `chrome://extensions/`
2. Aktifkan **Developer mode**
3. Klik **Load unpacked** dan pilih folder project ini

### Firefox
1. Buka `about:debugging#/runtime/this-firefox`
2. Klik **Load Temporary Add-on**
3. Pilih file `manifest.json` dari folder project ini

## Cara Penggunaan

1. Buka website yang ingin dikelola sesinya
2. Klik ikon extension **Session Switcher**
3. Klik menu **⋮** → **Save Current Session** untuk menyimpan sesi aktif
4. Untuk beralih, klik sesi yang tersimpan di daftar
5. Halaman akan otomatis di-reload dengan sesi yang dipilih

## Permissions

| Permission | Kegunaan |
|---|---|
| `storage` | Menyimpan data sesi |
| `cookies` | Membaca dan menulis cookies per domain |
| `tabs` | Mendapatkan URL tab aktif dan reload halaman |
| `activeTab` | Akses ke tab yang sedang aktif |
| `scripting` | Inject script untuk mengelola localStorage/sessionStorage |

## Struktur Project

```
session-switcher/
├── manifest.json          # Konfigurasi extension
├── background/
│   └── index.js           # Service worker (cookie & storage handler)
├── popup/
│   ├── index.html         # UI popup
│   ├── index.js           # Logic popup (session management)
│   └── style.css          # Styling
└── assets/
    └── icons/             # Ikon extension (16, 32, 48, 128px)
```

## Lisensi

Fork dari Session Switcher original.
