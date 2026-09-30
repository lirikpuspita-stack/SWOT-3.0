# Validation Notes — v2

## Static checks
- `index.html` self-contained: HTML, CSS, dan JavaScript berada dalam satu file.
- Tidak memerlukan library JavaScript eksternal.
- Sintaks JavaScript diperiksa dengan `node --check`.
- Tersedia empat kuadran SWOT, TOWS, prioritas strategi, action plan, sembilan blok BMC, rekomendasi BMC, PDF/print, DOC export, local save, dan reset.

## Formula checks

### Factor priority
Importance = 5 dan Urgency = 4:
`5 × 4 = 20/25`.

### Strategy priority
Relevance = 5, Impact = 4, Feasibility = 4, Risk = 2:
- reverse risk = `6 − 2 = 4`
- mean = `(5 + 4 + 4 + 4) / 4 = 4.25`
- priority = `4.25 × 20 = 85/100`

### Evidence coverage
Satu strategi memiliki dua faktor asal:
- keduanya memiliki bukti = 100%
- satu memiliki bukti = 50%
- tidak ada bukti = 0%

Evidence coverage tidak mengubah strategy score.

## BMC recommendation checks
Pengujian logika dengan contoh terkontrol menghasilkan teks rekomendasi non-kosong untuk seluruh 9 blok:
- Key Partnerships
- Key Activities
- Key Resources
- Value Propositions
- Customer Relationships
- Channels
- Customer Segments
- Cost Structure
- Revenue/Funding Streams

Setiap blok menyertakan basis strategi. Bila tidak ada pemetaan manual, basis dipilih menggunakan aturan heuristik yang didokumentasikan di `METHODOLOGY.md`.

## Interpretation safeguards
- Rekomendasi BMC selalu disebut **contoh/hipotesis**.
- Aplikasi tidak membuat nama mitra, angka biaya, harga, volume pasar, atau demografi spesifik tanpa input pengguna.
- Revenue/Funding Streams memberi alternatif mekanisme untuk diuji, bukan menyatakan sumber dana tertentu pasti tersedia.
- Laporan PDF/DOC dapat memuat rekomendasi BMC walaupun belum diterapkan ke kolom final, dan memberi label bahwa isinya adalah hipotesis.
- Reset meminta konfirmasi dan menghapus key v2 serta key legacy v1 dari `localStorage`.

## Migration
Jika data versi lama masih berada pada `strategic_swot_bmc_simple_v1`, v2 akan membacanya sebagai fallback, kemudian penyimpanan berikutnya menggunakan key `strategic_swot_bmc_simple_v2`.
