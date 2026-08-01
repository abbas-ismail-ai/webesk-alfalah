# Al-Falah Digital

Prototipe website profesional untuk menerapkan workbook **Aplikasi Digitalisasi Sistem Kepegawaian dan Keuangan — Pondok Pesantren Al-Falah**.

## Menjalankan aplikasi

Cara paling mudah: buka `index.html` dengan browser.

Untuk pengujian yang lebih stabil:

```bash
cd alfalah_web_app
python -m http.server 8080
```

Lalu buka `http://localhost:8080`.

## Akun demo

| Peran | Username | Password | Akses utama |
|---|---|---|---|
| Administrasi | `admin` | `admin123` | Lihat dan edit seluruh data; kelola hak akses |
| Mudir | `mudir` | `mudir123` | Lihat seluruh modul, tanpa edit |
| Bendahara | `bendahara` | `bendahara123` | Edit RAPBS, Kas Masuk, dan Kas Keluar; lihat laporan |
| Pengelola SDM | `sdm` | `sdm123` | Edit modul kepegawaian |
| Auditor Internal | `auditor` | `audit123` | Lihat keuangan dan edit Audit Internal |
| Kepala Unit Tahfidz | `kepala.tahfidz` | `unit123` | Akses SDM terbatas pada unit Tahfidz |
| Pegawai | `hasan` | `pegawai123` | Lihat data pribadi, evaluasi, penghargaan, dan pengembangan |

## Modul

Dashboard, Profil Lembaga, Database Pegawai, Perencanaan SDM, Rekrutmen, Pengembangan SDM, Evaluasi Kinerja, Penghargaan dan Pembinaan, RAPBS/RKAS, Kas Masuk, Kas Keluar, Buku Kas Umum, Realisasi Anggaran, Laporan Keuangan, Audit Internal, Manajemen Akses, dan Log Aktivitas.

## Fitur

- Kontrol akses berbasis peran.
- Tambah, edit, dan hapus data sesuai izin.
- Penyaringan data Kepala Unit dan Pegawai.
- Dashboard dan laporan dihitung ulang dari data sumber.
- Buku Kas Umum serta saldo berjalan otomatis.
- Realisasi anggaran per program.
- Audit internal dan log aktivitas.
- Ekspor CSV, cetak, dan cadangan JSON.
- Penyimpanan perubahan menggunakan `localStorage`.

## Catatan konsistensi data

Website menghitung total anggaran dari lima baris RAPBS/RKAS menjadi **Rp49.500.000**. Pada KPI Dashboard workbook, nilai tersebut terbaca `0`, sementara tabel RAPBS/RKAS dan Laporan Realisasi mendukung total Rp49.500.000. Aplikasi memakai perhitungan dari data sumber agar laporan konsisten.

## Batasan keamanan

Versi ini adalah prototipe frontend. Login, kata sandi, dan izin berada di JavaScript/localStorage dan tidak cukup aman untuk produksi. Penerapan nyata perlu:

- backend dan database;
- autentikasi server dengan hash kata sandi;
- otorisasi pada API/server;
- validasi transaksi dan persetujuan berjenjang;
- audit log yang tidak dapat diedit pengguna;
- HTTPS, enkripsi, pencadangan, dan pemulihan data.
