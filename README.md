# Everloop — Sidik Jari APK

Repo ini adalah **sumber kedua** untuk memeriksa keaslian aplikasi Everloop untuk Android.
Ia sengaja disimpan di luar server Everloop. Kalau suatu saat server kami dibobol dan berkas
APK, SHA-256, serta sidik jarinya diganti bersamaan, angka di sini tidak ikut berubah, sehingga
penggantian itu ketahuan.

Unduh aplikasi hanya dari halaman **https://everloop.amincloud.id/app**, lalu cocokkan angkanya dengan
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
| 1.0.3 (kode 4) | 10 November 2026 | `6a7484b7123898b4f435844e30b971ad2a3e4a9fb832417a43bc83c33cbd9502` | `d637eb885683d9ea28a7ea232ea51e552851a2164c964c0b279a059b41eed41b` |
| 1.0.2 (kode 3) | 9 November 2026 | `550ef45a75047334aa09d9ed6e99700ca812e00d6b5ea8e48604028833be85a1` | `dad19110f6b6b2ae721abf2e1ef9bf1aff82fa0ae4c30ffe1a533d661292f6a8` |
| 1.0.1 (kode 2) | 9 November 2026 | `e6f62797afe41cc5a3786138e2ef2d225cfe1163c319031262a79dcaf69e803e` | `bd92f5e7bbb2e27bb36277fdf55b6df93062dfbe6c8f1aa9a09a80e5542f3eb7` |
| 1.0.0 (kode 1) | 9 November 2026 | `01817c02e1014cd4019958df1a195e15968ed35f4fcb06641858fceed8d6549f` | `d199dc1917a17bbe4f1c988fa2deb00da6b9188b43e48e62f353fe2dffbe0db8` |

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
