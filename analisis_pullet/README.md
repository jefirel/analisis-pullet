# Demonstrasi Kemampuan Analisis Data Peternakan

**Catatan:** Data yang digunakan dalam laporan ini merupakan hasil simulasi (fiksi) yang dibuat untuk tujuan demonstrasi kemampuan analisis data. Angka tidak mencerminkan kondisi riil, namun metodologi dan pendekatan analisis dapat diterapkan pada data aktual.

**Disusun oleh:** Jefirel.A.P  
**Tanggal:** 25/03/2026  
**Jumlah Kandang:** 5 kandang  
**Periode:** 0–16 minggu (simulasi)

---

## 1. Ringkasan Eksekutif

Laporan ini menyajikan analisis data pemeliharaan pullet (0–16 minggu) pada 5 kandang ayam petelur strain Hy‑Line Brown. Analisis mencakup bobot badan, keseragaman (*uniformity*), koefisien variasi (CV), mortalitas, FCR, serta korelasi antar parameter. Meskipun data bersifat simulasi, pendekatan statistik dan interpretasi yang digunakan menggambarkan kemampuan analitis yang diperlukan dalam evaluasi performa peternakan.

| Parameter | Hasil Simulasi | Target Standar | Keterangan |
|-----------|----------------|----------------|------------|
| Bobot rata-rata minggu 16 | 1.241–1.255 g | 1.410–1.510 g | Di bawah target |
| Keseragaman minggu 16 | 68–77% | >85% | Perlu peningkatan |
| CV minggu 16 | 7,8–9,3% | <10% | Dalam batas wajar |
| Mortalitas total | 1,5–2,2% | <2% | Satu kandang di atas batas |
| FCR | ~5,3 | 2,2–2,8 | Jauh di atas target (indikasi kemungkinan kesalahan data) |

### Rekomendasi utama:
- Perbaiki bobot badan dan keseragaman dengan evaluasi pakan serta *grading*.
- Investigasi penyebab FCR sangat tinggi – validasi perhitungan pakan dan bobot.
- Fokus intervensi pada kandang dengan mortalitas tertinggi (K04) dan tiru praktik terbaik dari kandang dengan performa relatif lebih baik (K03).

---

## 2. Metodologi
- **Sumber data:** Simulasi data sampling 5% populasi per minggu (bobot individu, pakan, mortalitas).
- **Parameter yang dihitung:** Bobot badan (g), keseragaman (%), koefisien variasi (CV), mortalitas (%), *feed intake* (g/ekor/hari), FCR.
- **Tools analisis:** Excel, Python (Pandas, Matplotlib, Seaborn, Scipy).

---

## 3. Hasil Analisis

### 3.1 Bobot Badan vs Standar Hy‑Line Brown

Bobot badan aktual dibandingkan dengan standar strain menunjukkan bahwa pada minggu 1–5 bobot cenderung berlebih, tetapi setelah minggu 6 terjadi perlambatan dan bobot akhir minggu 16 rata-rata 12% di bawah batas bawah standar.

| Minggu | Standar (g) | Rata-rata Aktual (g) | Penyimpangan (%) |
|--------|-------------|----------------------|------------------|
| 1 | 70–80 | 109,5 | +37% |
| 2 | 115–145 | 191,8 | +32% |
| 3 | 190–220 | 272,1 | +24% |
| 4 | 270–320 | 348,4 | +9% |
| 5 | 360–420 | 425,9 | +1% |
| 6 | 470–520 | 460,0 | -2% |
| 7 | 570–640 | 543,1 | -5% |
| 8 | 680–760 | 618,9 | -9% |
| 9 | 780–880 | 697,9 | -11% |
| 10 | 885–995 | 767,9 | -13% |
| 11 | 995–1.105 | 866,1 | -13% |
| 12 | 1.095–1.205 | 940,3 | -14% |
| 13 | 1.175–1.295 | 1.013,8 | -14% |
| 14 | 1.265–1.365 | 1.107,1 | -12% |
| 15 | 1.345–1.445 | 1.186,5 | -12% |
| 16 | 1.410–1.510 | 1.246,2 | -12% |

> **Grafik:** *Tren Bobot Pullet dengan Pooled Standard Deviation*  
> **Insight:** Perlambatan pertumbuhan setelah minggu 5 mengindikasikan perlunya evaluasi manajemen pakan dan lingkungan di fase *grower–developer*.

---

### 3.2 Keseragaman (*Uniformity*)

Keseragaman dihitung sebagai persentase ayam dengan bobot dalam rentang ±10% dari rata-rata. Hasil menunjukkan bahwa keseragaman cenderung menurun setelah minggu 8 dan tidak mencapai target 85% di akhir periode. Kandang K03 memiliki keseragaman tertinggi (~77%), sementara K04 terendah (~68%).

> **Grafik:** *Keseragaman Minggu 16, urutan tertinggi*  
> **Insight:** Keseragaman yang rendah berkontribusi terhadap variasi bobot dan berpotensi menurunkan efisiensi pakan.

---

### 3.3 Koefisien Variasi (CV)

CV = (Std Dev / Rata-rata) × 100%. Target CV <10% untuk keseragaman yang baik.

| Kandang | CV (%) Minggu 16 |
|---------|------------------|
| K01 | 9,32 |
| K02 | 8,76 |
| K03 | 7,86 |
| K04 | 9,36 |
| K05 | 8,86 |

**Rata-rata CV minggu 16:** 8,85%  
**Status:** Seluruh kandang memenuhi target CV <10%, namun variasi yang masih ada tetap mempengaruhi keseragaman secara keseluruhan.

---

### 3.4 Mortalitas Kumulatif

Mortalitas dihitung dari total kematian dan afkir. Kandang K04 melampaui target 2%, sementara kandang lain masih dalam batas wajar.

| Kandang | Mortalitas (ekor) | Mortalitas (%) |
|---------|-------------------|----------------|
| K01 | 15 | 1,5 |
| K02 | 19 | 1,9 |
| K03 | 17 | 1,7 |
| K04 | 22 | 2,2 |
| K05 | 17 | 1,7 |

> **Grafik:** *Mortalitas Kumulatif per Kandang*  
> **Insight:** Mortalitas tertinggi pada K04 perlu diinvestigasi (kemungkinan manajemen *brooding* atau kesehatan).

---

### 3.5 FCR (*Feed Conversion Ratio*)

FCR = total pakan (kg) / total bobot (kg). Nilai FCR yang diperoleh sangat tinggi (~5,3), jauh di atas standar industri (2,2–2,8).

| Kandang | FCR |
|---------|-----|
| K01 | 5,28 |
| K02 | 5,28 |
| K03 | 5,32 |
| K04 | 5,35 |
| K05 | 5,33 |

> **Insight:** Nilai FCR yang sangat tidak wajar mengindikasikan kemungkinan kesalahan data (misalnya satuan pakan dalam ton bukan kg) atau terdapat masalah serius dalam konversi pakan. Dalam analisis nyata, langkah pertama adalah memverifikasi perhitungan dan unit.

> **Grafik:** *Heatmap FCR*

---

### 3.6 Analisis Korelasi

Analisis korelasi (Pearson) dilakukan untuk melihat hubungan antar parameter (n=5 kandang).

| Parameter | Koefisien Korelasi (r) | p-value | Interpretasi |
|-----------|------------------------|--------|--------------|
| CV Minggu 6 vs Keseragaman Minggu 16 | -0,241 | 0,696 | Tidak signifikan |
| Keseragaman Minggu 8 vs FCR | -0,286 | 0,641 | Tidak signifikan |
| Mortalitas Awal vs Keseragaman Akhir | -0,152 | 0,807 | Tidak signifikan |
| *Feed Intake* vs Bobot Akhir | +0,469 | 0,425 | Tidak signifikan (namun menunjukkan kecenderungan positif) |

> **Grafik:** *Matriks Korelasi*  
> **Insight:** Dengan jumlah sampel yang sangat kecil (n=5), tidak ada hubungan yang signifikan secara statistik. Namun, korelasi positif antara *feed intake* dan bobot akhir (r = 0,469) sejalan dengan prinsip bahwa asupan pakan yang lebih tinggi cenderung meningkatkan bobot badan.

---

## 4. Rekomendasi

### Prioritas 1 – Tinggi
- **Perbaikan bobot badan dan keseragaman:**  
  Evaluasi program pakan (kualitas, frekuensi, distribusi). Lakukan *grading* (pemisahan) pada ayam dengan bobot di bawah rata-rata untuk diberi perlakuan pakan khusus.
- **Investigasi Kandang K04:**  
  Periksa kualitas air, ventilasi, kepadatan, dan riwayat kesehatan. Identifikasi penyebab mortalitas tinggi (2,2%).

### Prioritas 2 – Sedang
- **Validasi FCR:**  
  Periksa kembali satuan pakan (pastikan dalam kg, bukan ton) dan hitung ulang FCR. Jika data benar, lakukan audit manajemen pakan dan kesehatan.
- ***Benchmark* ke K03:**  
  K03 memiliki CV terbaik dan mortalitas rendah. Dokumentasikan praktik manajemennya untuk diterapkan di kandang lain.

### Prioritas 3 – Rendah
*(Tidak disebutkan lebih lanjut dalam dokumen)*

---

## 5. Kesimpulan
1. Bobot badan dan keseragaman di bawah standar, mengindikasikan perlunya intervensi pada manajemen pakan dan *grading*.
2. CV masih dalam batas wajar, namun tidak cukup untuk mencapai target keseragaman.
3. Mortalitas sebagian besar kandang masih dapat diterima, kecuali K04 yang perlu perhatian.
4. FCR sangat tinggi – perlu validasi data sebelum mengambil kesimpulan.
5. Korelasi tidak signifikan akibat jumlah sampel kecil, namun metode analisis yang diterapkan sudah sesuai.

Laporan ini menunjukkan bahwa meskipun data bersifat simulasi, pendekatan analisis yang sistematis (deskriptif, statistik, korelasi) mampu memberikan wawasan untuk pengambilan keputusan manajerial.

---

## Lampiran
- Dataset simulasi: `laporan_sampling_pullet.csv`
- Notebook analisis: `analisis_pullet.ipynb`
- Visualisasi: folder `/visualisasi`

---

## Lisensi
Laporan ini dilisensikan di bawah MIT License.

*Laporan disusun sebagai demonstrasi kemampuan analisis data.*