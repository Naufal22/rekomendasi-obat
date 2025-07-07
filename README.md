# Rekomendasi Kombinasi Obat untuk Pasien Faringitis
Proyek Kerja Praktik – Semester 6  
Program Studi Informatika Medis – Universitas Teknologi Yogyakarta  
Studi Kasus: Puskesmas Mlati II Sleman

## Deskripsi Proyek
Proyek ini bertujuan membangun model machine learning untuk memberikan rekomendasi kombinasi obat pada pasien faringitis (ICD-10: J02). Model dirancang berdasarkan data rekam medis pasien yang telah dikumpulkan dan diproses dalam bentuk multi-label classification.

## Dataset
- Jumlah data pasien: 128 pasien
- Fitur input: umur, jenis kelamin, tekanan darah, berat badan, diagnosis, dll.
- Target label: 8 jenis obat (multi-label, bisa lebih dari satu label per pasien)

## Metodologi
1. **Preprocessing**
   - Imputasi data hilang
   - Encoding diagnosis
   - Pembuatan fitur tambahan (seperti IMT, MAP)
   - Seleksi pasien dengan ≥3 obat
2. **Modeling**
   - Algoritma: Random Forest (Multi-label)
   - Teknik balancing: SMOTE
   - Seleksi fitur: Permutation Importance
3. **Evaluasi**
   - Mikro/makro F1-score
   - Hamming Loss
   - Accuracy per-label
   - Kesesuaian Obat per pasien

## Hasil
Model menunjukkan performa yang baik dalam memprediksi kombinasi obat, dengan evaluasi berbasis mikro-F1 menunjukkan akurasi tinggi pada label mayoritas. Model ini dapat dijadikan pondasi awal untuk sistem rekomendasi klinis di masa depan.

## Teknologi
- Python
- Scikit-learn
- Pandas, Seaborn, Matplotlib

## Catatan
Model ini dikembangkan sebagai bagian dari tugas kerja praktik akademik dan tidak digunakan untuk keputusan medis nyata tanpa validasi klinis lebih lanjut.
