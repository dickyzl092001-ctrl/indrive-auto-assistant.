# Membuat APK dari HP (GitHub Actions)

1. Unduh dan ekstrak ZIP project ini di HP.
2. Buka repository GitHub `indrive-auto-assistant`.
3. Unggah **isi folder** `IndriveAutoAssistant_AutoAccept` ke root repository (bukan folder luarnya). Pastikan `.github/workflows/build-apk.yml` ikut terunggah.
4. Commit perubahan ke branch `main`.
5. Buka tab **Actions**. Pilih workflow **Build Android APK** lalu tunggu sampai selesai.
6. Jika status hijau (Success), buka run tersebut, gulir ke **Artifacts**, lalu unduh `inDrive-AutoAssistant-debug`.
7. Ekstrak artifact dan instal `app-debug.apk` di HP.

Jika gagal, buka run yang merah dan salin **bagian pertama yang bertuliskan `FAILURE:` beserta 20-30 baris setelahnya**. Jangan kirim token, password, atau secret GitHub.

## Catatan fungsi
- Auto Accept harus diaktifkan sendiri dari aplikasi.
- Aktifkan layanan Accessibility untuk aplikasi ini melalui Pengaturan Android.
- Layanan hanya mencari tombol dengan teks `Terima dengan harga` pada layar aplikasi inDrive yang terdeteksi. Antarmuka/versi inDrive dapat berbeda sehingga fungsi tidak dijamin pada semua versi.
- Uji hanya saat kendaraan berhenti. Auto Accept dapat menerima order yang tidak diinginkan.
- APK debug bukan rilis Play Store. Android mungkin meminta izin instalasi dari sumber tersebut.
