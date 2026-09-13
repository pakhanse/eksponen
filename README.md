# Modul Interaktif Eksponen dan Bentuk Akar

**Pengembang: Handis Setioko, M.Pd.**  
SMAN 1 Manggar · Matematika Kelas X / Fase E · 2026

## Dua cara menggunakan

1. **HTML mandiri:** buka file `index.html` yang diberikan terpisah dengan browser modern. Materi, simulasi, game, latihan, evaluasi, dan refleksi langsung berjalan tanpa internet. File ini sudah memuat CSS dan JavaScript; tidak memerlukan instalasi atau library eksternal.
2. **Paket GitHub/PWA:** ekstrak ZIP ini dan unggah seluruh isinya ke repositori GitHub. Pertahankan struktur folder, terutama `icons/`. Jangan mengunggah hanya ZIP-nya.

## Menayangkan melalui GitHub Pages

1. Buat repositori atau gunakan repositori yang sudah tersedia.
2. Unggah `index.html`, `sw.js`, `manifest.webmanifest`, `.nojekyll`, dan folder `icons` ke akar repositori.
3. Pada pengaturan GitHub Pages, pilih publikasi dari branch tempat file disimpan dan folder akar (`/(root)`). Simpan pengaturan.
4. Setelah publikasi selesai, buka URL Pages yang diberikan GitHub. Untuk repositori proyek, seluruh referensi aset memakai path relatif agar tetap bekerja pada subfolder repositori.

[Dokumentasi resmi GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

## Offline dan PWA

- Versi HTML terpisah dapat dibuka langsung dari penyimpanan perangkat tanpa jaringan.
- Versi ZIP mengaktifkan `enablePWA: true`. Buka melalui HTTPS (misalnya GitHub Pages) atau localhost agar service worker dapat bekerja.
- Buka sekali saat online dan tunggu halaman selesai dimuat. Materi inti disimpan dalam cache; kunjungan berikutnya dapat bekerja offline.
- Pemasangan aplikasi melalui menu browser bergantung pada dukungan perangkat. Pada perangkat yang mendukungnya, pilih pemasangan aplikasi atau Tambahkan ke Layar Utama.
- PWA tidak diaktifkan ketika file dibuka melalui `file://`. Seluruh fitur pembelajaran tetap dapat berjalan.

## Mode Guru

**PIN awal: `2026`**

PIN bisa diganti pada `MODULE_CONFIG.teacherPIN` di dalam `index.html`. Ini pembatas antarmuka sederhana, bukan perlindungan keamanan; kunci jawaban berada dalam sumber HTML. Tidak ada akun, backend, atau pengumpulan data antarsiswa secara daring.

Mode Guru menyediakan pengaturan 10–15 soal, nilai minimum, timer 1–180 menit, kunci dan pembahasan, skor tim, pemilih siswa, serta reset data siswa dengan konfirmasi. Perubahan evaluasi berlaku pada percobaan baru. Timer yang aktif tetap berjalan ketika siswa berpindah menu atau menutup halaman; jawaban yang sudah tersimpan dinilai setelah batas waktu tercapai.

## Konfigurasi

Cari `const MODULE_CONFIG` pada HTML. Identitas, nama guru/pengembang, instansi, tahun, alokasi waktu, ketuntasan, jumlah soal, timer, PIN, suara, tema, IFP, dan gamifikasi diatur di sana. Pengaturan guru tersimpan di browser dan mengesampingkan pengaturan awal evaluasi. Bank evaluasi terdapat dalam `SOURCE.evaluation`; indeks kunci jawaban dimulai dari 0.

## Fitur dan cakupan

- Lima bab sumber: sifat eksponen, pangkat rasional dan bentuk akar, fungsi eksponen, persamaan, pertidaksamaan.
- Apersepsi, materi bertahap, pemeriksaan konsep, eksplorasi lipatan dan luas, drag-and-drop dengan tap/keyboard fallback.
- Simulasi pertumbuhan/peluruhan, zona cahaya laut, mikroalga, dan bak air hujan.
- Proyek terpadu Linear atau Eksponensial: minimal delapan pasangan data, tabel selisih/rasio, dan dua titik uji.
- Quiz Battle, Match It!, Challenge Timer, Mystery Box, XP, streak, dan badge.
- Delapan latihan campuran dengan bantuan bertahap; evaluasi 15 soal dengan urutan dan opsi acak.
- Hasil, analisis per bab, review jawaban, cetak, unduh ringkasan teks, refleksi, dan exit ticket.
- Tampilan responsif, Mode IFP, fullscreen (sesuai dukungan browser), mode gelap, dan suara opsional.

Progres dihitung dari 16 kegiatan: tujuan, apersepsi, 5 bab, 3 eksplorasi, kesimpulan simulasi, proyek, satu game, 8 latihan yang selesai, evaluasi, dan refleksi. Proyek dan refleksi ditandai berdasarkan penyelesaian kegiatan, bukan penilaian otomatis kualitas alasan. Guru tetap menilai hasil proyek dan tulisan siswa.

## Penyimpanan dan penggunaan kelas

Progres disimpan dalam localStorage pada browser, profil, perangkat, dan alamat yang sama. Gunakan satu profil untuk satu siswa; simpan ringkasan sebelum berganti siswa. Menghapus data browser atau berpindah perangkat/alamat tidak memindahkan progres. Mode privat dapat membatasi penyimpanan. Tidak ada sinkronisasi kelas atau server.

Mode IFP memperbesar tampilan dan meminta fullscreen ketika didukung. Semua aktivitas pencocokan mendukung pilih kartu lalu pilih tujuan, termasuk dengan Tab dan Enter. Gunakan menu hamburger pada layar kecil. Efek suara tidak diputar otomatis.

## Sumber

Diadaptasi dari `Modul_Eksponen_dan_Bentuk_Akar_STEM_Fase_E [Siswa].docx` karya Handis Setioko, M.Pd., dengan konteks Belitung Timur dan alokasi 20 JP termasuk proyek. Modul sumber merujuk lembar kerja Vol. 3A “Pangkat” Surya Institute untuk urutan konsep serta gradasi latihan. Soal digital disesuaikan untuk interaksi dan umpan balik. Semua angka simulasi lokal merupakan data ilustrasi, bukan pengukuran lapangan.
