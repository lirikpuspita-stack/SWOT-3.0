# Strategic SWOT → BMC — Simple GitHub Edition v2

Aplikasi statis satu halaman untuk membantu organisasi/proyek/produk/l layanan menyusun alur yang ringkas dan dapat ditelusuri:
1. mendefinisikan konteks keputusan;
2. mengidentifikasi Strengths, Weaknesses, Opportunities, dan Threats berbasis bukti;
3. membentuk alternatif strategi TOWS (SO, WO, ST, WT);
4. memprioritaskan strategi secara transparan;
5. menerjemahkan strategi terpilih menjadi rencana aksi; dan
6. menyusun **contoh/rekomendasi Business Model Canvas (BMC) sebagai hipotesis awal** yang diturunkan dari tujuan, faktor SWOT, dan strategi prioritas.

## Perubahan utama v2

- Sembilan blok BMC kini memiliki **contoh/rekomendasi otomatis** yang sedekat mungkin dengan masalah dan rekomendasi strategis yang dimasukkan pengguna.
- Rekomendasi BMC selalu diberi label **CONTOH / HIPOTESIS**, bukan fakta.
- Setiap rekomendasi menampilkan **basis strategi** yang digunakan.
- Jika strategi belum dipetakan manual ke blok BMC, aplikasi menggunakan aturan pemetaan heuristik yang transparan hanya untuk membentuk hipotesis awal.
- Tombol **Gunakan rekomendasi ini** tersedia pada setiap blok.
- Tombol **Terapkan Semua Rekomendasi** mengisi sembilan blok sekaligus setelah konfirmasi bila ada isian lama.
- Laporan PDF/DOC tetap menampilkan rekomendasi/hipotesis BMC walaupun pengguna belum menyalinnya ke kolom final.
- Data v1 dimigrasikan otomatis dari `localStorage` bila tersedia.

## Prinsip metodologis

- **SWOT adalah analisis situasi**, bukan algoritme prediksi.
- S/W diperlakukan sebagai faktor internal; O/T sebagai faktor eksternal.
- Setiap faktor menyediakan kolom **bukti/sumber**.
- Prioritas faktor = `Kepentingan × Urgensi` (1–25), hanya sebagai heuristic pengurutan.
- TOWS digunakan untuk *matching*: SO, WO, ST, WT.
- Prioritas strategi = rata-rata empat penilaian skala 1–5: relevansi, dampak, kelayakan, dan kebalikan risiko; dikonversi menjadi 0–100.
- Kualitas/kelengkapan bukti dilaporkan terpisah dari skor strategi.
- BMC adalah **desain/hipotesis** yang harus diuji. Aplikasi tidak boleh menyatakan nama pelanggan, mitra, harga, biaya, atau sumber pendapatan spesifik sebagai fakta bila data tersebut tidak diberikan.

## Logika rekomendasi BMC

Aplikasi menggunakan data yang tersedia dengan urutan prioritas berikut:
1. strategi yang dipetakan pengguna ke blok BMC;
2. jika tidak ada pemetaan manual, strategi prioritas yang paling relevan dengan fungsi blok BMC;
3. tujuan strategis dan konteks keputusan;
4. faktor S/W/O/T prioritas.

Contoh: pada **Key Resources**, aplikasi menghubungkan kekuatan yang perlu dipertahankan dengan kelemahan yang perlu ditutup. Pada **Value Propositions**, aplikasi menghubungkan tujuan strategis dengan strategi prioritas. Pada **Revenue/Funding Streams**, aplikasi hanya memberikan alternatif mekanisme yang perlu diuji sesuai jenis objek; aplikasi tidak mengklaim bahwa salah satu mekanisme pasti tersedia.

## Ekspor

- **Cetak / PDF** → gunakan dialog cetak browser dan pilih “Save as PDF”.
- **Export DOC** → menghasilkan file `.doc` yang dapat dibuka Microsoft Word/LibreOffice.
- **Reset** → menghapus semua data aplikasi dari `localStorage` setelah konfirmasi.

## Deploy GitHub Pages

1. Buat repository GitHub.
2. Upload seluruh isi folder ini ke root repository.
3. Pastikan `index.html` berada di root.
4. Buka **Settings → Pages**.
5. Pilih **Deploy from a branch → main → /(root)**.
6. Simpan.

Tidak membutuhkan backend, database, Node.js, atau proses build.

## Batasan

Aplikasi tidak mengklaim validitas prediktif, kausal, atau probabilistik. Kualitas keluaran tetap bergantung pada kualitas faktor, bukti, penilaian pengguna, dan validasi stakeholder. Rekomendasi BMC dimaksudkan untuk mempercepat perumusan **hipotesis model bisnis/operasi**, bukan menggantikan riset pelanggan, analisis biaya, analisis pasar, atau keputusan manajemen.

Footer aplikasi: `@ramakertamukti`.
