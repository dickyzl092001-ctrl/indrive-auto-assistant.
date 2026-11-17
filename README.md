# inDrive Auto Assistant

Aplikasi Android sederhana dengan Accessibility Service untuk membaca informasi order inDrive menggunakan Text-to-Speech Bahasa Indonesia dan, bila diaktifkan pengguna, mencoba menekan kontrol bertuliskan **Terima dengan harga**.

## Build

Gunakan GitHub Actions workflow `Build Android APK` di `.github/workflows/build-apk.yml`. Workflow memasang Android SDK packages secara terpisah, lalu menjalankan `:app:assembleDebug` dan mengunggah APK sebagai artifact.

## Penggunaan dan batasan

1. Instal APK dan buka aplikasi.
2. Aktifkan layanan aksesibilitas aplikasi melalui tombol pengaturan.
3. Atur Voice Alert dan Auto Accept dari aplikasi.
4. Auto Accept dinonaktifkan secara default dan harus diaktifkan secara sadar.

Aplikasi bergantung pada teks/struktur antarmuka inDrive yang diekspos melalui Accessibility. Perubahan aplikasi, bahasa, wilayah, atau versi Android dapat membuat deteksi tidak bekerja. Keberhasilan `ACTION_CLICK` tidak menjamin server inDrive menerima order. Auto Accept dapat menerima order yang tidak diinginkan; gunakan hanya saat kendaraan berhenti dan uji dengan hati-hati.
