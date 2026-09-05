# 📝 Penilaian Ujian Mahasiswa (UTS & UAS)

Aplikasi web satu file untuk menilai ujian mahasiswa dari file Excel official kampus.
Upload → petakan kolom → cari Nama/NIM → beri nilai UTS/UAS → download hasilnya
dengan format asli tetap terjaga.

## ✨ Fitur

- **Upload Excel** (`.xlsx`, `.xls`, `.csv`) via klik / drag & drop
- **Deteksi header otomatis** — melewati baris info (Mata Kuliah, Tahun Ajaran, …)
  dan menemukan baris `NIM | Nama Mahasiswa | … | Nilai UTS | Nilai UAS`
- **Pemetaan kolom fleksibel** — format Excel beda-beda tetap bisa dipakai,
  termasuk opsi *buat kolom baru* dan pilihan baris header manual
- **Abaikan footer otomatis** — baris non-mahasiswa (tanda tangan, kode verifikasi) difilter
- **Cari & nilai** by Nama/NIM, full keyboard:
  `↑`/`↓` navigasi, `Enter` pilih, `Esc` bersihkan, `/` fokus cari,
  `Alt+U`/`Alt+A` ganti UTS/UAS, `Enter` di skor = simpan
- **Tabel canggih** — sortir (klik judul kolom), filter
  (Belum UTS / Belum UAS / Belum lengkap / Lengkap), pagination,
  badge warna nilai (≥80 hijau, 60–79 kuning, <60 merah), edit inline
- **Undo** — semua perubahan nilai bisa dibatalkan (tombol / `Ctrl+Z`)
- **Hapus nilai per kolom** (UTS / UAS saja)
- **Download Excel yang setia format** — font & size, format angka (`90,00`),
  lebar kolom, merge, dan proteksi sheet dipertahankan (via ExcelJS)
- **Dark mode** 🌙/☀️ + stepper progres Upload → Pemetaan → Nilai → Download
- **Otomatis tersimpan** di browser (`localStorage`), tetap ada setelah refresh

## 🚀 Cara menjalankan

Tidak perlu install apa pun. Pilih salah satu:

1. **Langsung** — buka `penilaian-mahasiswa/index.html` di browser
   (butuh internet sekali untuk memuat library CDN).
2. **Local server** (opsional):
   ```bash
   cd penilaian-mahasiswa
   python -m http.server 8000
   # buka http://localhost:8000
