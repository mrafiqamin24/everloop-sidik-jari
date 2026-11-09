# Everloop — Sidik Jari APK

Repo ini adalah **sumber kedua** untuk memeriksa keaslian aplikasi Everloop untuk Android.
Ia sengaja disimpan di luar server Everloop. Kalau suatu saat server kami dibobol dan berkas
APK, SHA-256, serta sidik jarinya diganti bersamaan, angka di sini tidak ikut berubah, sehingga
penggantian itu ketahuan.

Unduh aplikasi hanya dari **https://everloop.amincloud.id**, lalu cocokkan angkanya dengan
tabel di bawah.

## Sidik jari APK

Semua rilis ditandatangani dengan **satu sertifikat yang sama**:

**SHA-256 sertifikat:**
```
7B:2F:D5:CE:E0:E9:98:03:1A:DB:CC:14:D9:98:E7:25:A6:AE:42:70:A6:D9:E9:C3:2A:78:86:4A:04:03:91:A0
```
Berlaku sampai 27 Maret 2054. Kalau sidik jari sertifikat di APK Anda berbeda dari angka di atas,
**jangan pasang** APK itu.

SHA-256 berkas APK berbeda untuk setiap rilis:

| Versi | Tanggal | SHA-256 berkas APK (arm64) | SHA-256 berkas APK (universal) |
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
