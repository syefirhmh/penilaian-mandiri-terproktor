# Panduan pasang ujian mandiri

## 1. Firebase (sekitar 10 menit, gratis)
1. Buka console.firebase.google.com, buat project baru (Google Analytics boleh dimatikan).
2. Build > Firestore Database > Create database > pilih lokasi (mis. asia-southeast2 Jakarta) > mode production.
3. Build > Authentication > Get started > aktifkan Email/Password. Tab Users > Add user: isi email dan sandi guru.
4. Project settings (ikon roda gigi) > Your apps > ikon web (</>) > daftarkan app > salin isi `firebaseConfig`.
5. Firestore > tab Rules: tempel isi `firestore.rules` (ganti `guru@contoh.com` dengan email guru) > Publish.

## 2. Isi config.js
Tempel nilai firebaseConfig ke `config.js` dan ubah `TEACHER_EMAIL` (sama dengan di rules).

## 3. Taruh online
Buka app.netlify.com/drop, seret folder ini (index.html, config.js). Kamu dapat link seperti https://nama.netlify.app. Vercel atau GitHub Pages juga bisa.

## 4. Pakai
- Link murid: https://nama.netlify.app
- Link guru: https://nama.netlify.app/#guru (masuk dengan email dan sandi tadi), lalu buat atau impor soal dan klik Simpan dan terbitkan.

Jika login gagal karena domain, tambahkan domain Netlify di Authentication > Settings > Authorized domains.
