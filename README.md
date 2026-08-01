# WebESK Al-Falah

Aplikasi web lokal berbasis data XLSX “Aplikasi Digitalisasi Sistem Kepegawaian dan Keuangan - Pondok Pesantren Al-Falah”.

## Cara menjalankan
1. Ekstrak ZIP.
2. Buka `index.html` menggunakan Chrome/Edge/Firefox.
3. Pilih peran dan masukkan PIN.

## Akun demo
- Administrator — 123456
- Mudir / Pimpinan — 111111
- Petugas SDM — 222222
- Bendahara — 333333
- Auditor Internal — 444444
- Viewer — 555555

## Hak akses
- Administrator: semua menu dan semua perubahan.
- Mudir: melihat semua ringkasan penting; mengubah evaluasi, penghargaan, dan audit.
- SDM: mengelola pegawai, kebutuhan, rekrutmen, pengembangan, evaluasi, penghargaan.
- Bendahara: mengelola RAPBS, kas masuk, dan kas keluar.
- Auditor: melihat laporan dan mengelola audit.
- Viewer: hanya membaca.

## Catatan keamanan
Versi ini adalah prototipe front-end lokal. PIN tersimpan di JavaScript dan data tersimpan di localStorage browser. Untuk penggunaan sungguhan, pindahkan autentikasi dan data ke backend/database, gunakan hash PIN/password, HTTPS, audit log, dan backup.


## Membuat tautan HTTPS

### Netlify
1. Buka Netlify dan masuk ke akun.
2. Pilih **Add new site** lalu **Deploy manually**.
3. Seret folder `WebESK-Al-Falah-HTTPS` atau file ZIP ke halaman deploy.
4. Netlify otomatis memberikan alamat seperti `https://nama-situs.netlify.app`.

### Vercel
1. Buka Vercel dan masuk ke akun.
2. Pilih **Add New Project**.
3. Unggah folder proyek atau hubungkan repository GitHub.
4. Pilih framework **Other** dan deploy.
5. Vercel otomatis memberikan alamat `https://nama-proyek.vercel.app`.

HTTPS disediakan otomatis oleh Netlify/Vercel.
