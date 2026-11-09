# Everloop — Sidik Jari APK

Repo ini adalah **sumber kedua** untuk memeriksa keaslian aplikasi Everloop untuk Android.
Ia sengaja disimpan di luar server Everloop. Kalau suatu saat server kami dibobol dan berkas
APK, SHA-256, serta sidik jarinya diganti bersamaan, angka di sini tidak ikut berubah, sehingga
penggantian itu ketahuan.

Unduh aplikasi hanya dari **https://everloop.amincloud.id**, lalu cocokkan angkanya dengan
tabel di bawah.

## Sidik jari APK

Semua rilis ditandatangani dengan **satu sertifikat yang sama**. Kalau sidik jari sertifikat
di APK Anda berbeda dari baris di bawah, **jangan pasang** APK itu.

| Versi | Tanggal | SHA-256 sertifikat penanda tangan | SHA-256 berkas APK (arm64) |
|---|---|---|---|
| _belum ada rilis_ | – | – | – |

## Cara memeriksa

1. **Di HP, setelah aplikasi terpasang:** buka **Profil → Tentang Aplikasi**. Sidik jari
   sertifikat di sana harus sama dengan tabel di atas.
2. **Di komputer, sebelum memasang:**
   ```
   apksigner verify --print-certs everloop.apk
   ```
   Baris `Signer #1 certificate SHA-256 digest` harus sama dengan kolom sertifikat.
   SHA-256 berkasnya bisa dihitung dengan `certutil -hashfile everloop.apk SHA256` (Windows)
   atau `sha256sum everloop.apk` (Linux/macOS).
3. **Pembaruan aman dengan sendirinya:** Android menolak memasang pembaruan yang
   ditandatangani sertifikat lain di atas aplikasi Everloop yang sudah terpasang.

---
Tim forever · everloop888@gmail.com
