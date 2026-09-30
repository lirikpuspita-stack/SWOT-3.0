# Methodology Note — v2

## 1. Scope
Analisis dimulai dari objek, tujuan, pertanyaan keputusan, horizon waktu, dan konteks. Tujuannya mengurangi SWOT yang terlalu umum.

## 2. Factor identification
- Strength / Weakness = faktor internal.
- Opportunity / Threat = faktor eksternal.
- Setiap faktor dapat disertai bukti/sumber yang dapat ditelusuri.
- Kepentingan dan urgensi dipakai hanya untuk mengurutkan perhatian (`importance × urgency`).

## 3. TOWS strategy formulation
Empat bentuk *matching*:
- SO: menggunakan strength untuk memanfaatkan opportunity;
- WO: memanfaatkan opportunity untuk mengurangi weakness;
- ST: menggunakan strength untuk merespons/mereduksi threat;
- WT: mengurangi weakness sekaligus membatasi exposure terhadap threat.

Teks strategi adalah template yang hanya memakai faktor yang dimasukkan pengguna dan dapat diedit.

## 4. Strategy prioritization
Empat kriteria skala 1–5:
- strategic relevance;
- expected impact;
- feasibility;
- risk.

Risk dibalik (`6 - risk`) agar arah skornya konsisten.

`Priority = ((R + I + F + (6 - Risk)) / 4) × 20`

Skor hanya alat bantu pengurutan; bukan probabilitas keberhasilan.

## 5. Evidence coverage
Evidence coverage = proporsi dua faktor asal strategi yang memiliki bukti/sumber. Coverage dilaporkan terpisah dari skor strategi.

## 6. Action plan
Strategi prioritas diterjemahkan ke langkah aksi, PIC, tenggat, KPI, dan target. Detail yang tidak tersedia tidak diisi sebagai fakta.

## 7. Business Model Canvas recommendation layer
BMC tetap menggunakan sembilan blok klasik. Pada v2, aplikasi menambahkan **lapisan rekomendasi/hipotesis**.

### 7.1 Prinsip
Rekomendasi BMC:
- tidak mengubah SWOT menjadi “fakta pelanggan” secara otomatis;
- hanya menggunakan konteks, tujuan, faktor, dan strategi yang sudah tersedia;
- menyatakan ketidakpastian secara eksplisit;
- membedakan **rekomendasi/hipotesis** dari **isian BMC final** pengguna.

### 7.2 Basis strategi per blok
Jika pengguna memetakan strategi secara manual, pemetaan itu menjadi basis utama. Jika tidak, aplikasi menggunakan urutan heuristik yang transparan:
- Key Partnerships: WO → SO → WT → ST
- Key Activities: SO → WO → ST → WT
- Key Resources: WO → ST → WT → SO
- Value Propositions: SO → ST → WO → WT
- Customer Relationships: ST → SO → WT → WO
- Channels: SO → WO → ST → WT
- Customer Segments: SO → WO → ST → WT
- Cost Structure: WT → WO → ST → SO
- Revenue/Funding Streams: SO → WO → ST → WT

Urutan tersebut **bukan hukum universal** dan tidak menambah skor. Ia hanya menentukan strategi mana yang lebih dahulu dipakai untuk menyusun contoh teks BMC saat pemetaan manual belum tersedia.

### 7.3 Guardrail anti-fake
- **Customer Segments:** memakai pihak yang disebut/tersirat langsung dari tujuan; bila tidak jelas, aplikasi meminta validasi, bukan membuat demografi baru.
- **Key Partnerships:** tidak membuat nama organisasi/mitra tertentu.
- **Cost Structure:** tidak membuat angka biaya.
- **Revenue/Funding Streams:** tidak menyatakan model pendapatan tertentu telah tersedia; hanya memberikan opsi uji sesuai jenis objek.
- **Value Proposition:** diturunkan dari tujuan dan strategi, lalu dinyatakan sebagai hipotesis manfaat yang perlu diuji.

## 8. Reporting
PDF/DOC menampilkan isi final BMC bila telah diterapkan pengguna. Jika belum, laporan tetap memuat **rekomendasi/hipotesis aplikasi** beserta basis strateginya dan label bahwa rekomendasi tersebut belum tervalidasi.
