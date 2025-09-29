# M1-Telco-Churn-Prediction
Proyek prediksi customer churn Telco untuk Tugas M1 - Final Block

## 1 Problem Statement 
Fokus: Mengurangi Churn Pelanggan pada Perusahaan Telekomunikasi. 
Perusahaan Telco menghadapi tantangan signifikan dengan tingkat churn pelanggan bulanan yang rata-rata 26.5% (berdasarkan dataset historis). Tingkat churn yang tinggi ini menyebabkan kerugian pendapatan dan peningkatan biaya akuisisi pelanggan baru yang mahal. Kami bertujuan membangun model Klasifikasi Machine Learning yang mampu mengidentifikasi pelanggan berisiko tinggi (churn) setidaknya 30 hari sebelumnya. Nilai bisnisnya adalah memungkinkan tim retention melakukan intervensi yang ditargetkan (penawaran diskon, peningkatan layanan) untuk menurunkantingkat∗churn∗sebesar5% dalam 6 bulan pertama implementasi.

## 2 Scope Awal

In-Scope : 
- Membangun model klasifikasi biner untuk memprediksi probabilitas churn (1/0) pelanggan. 
- Menggunakan data historis dari layanan, kontrak, charges, dan demografi yang tersedia (sesuai dataset Telco Churn). 
- Melakukan data cleaning, feature engineering dasar (seperti One-Hot Encoding), dan pelatihan model baseline (Regresi Logistik). 
- Evaluasi model menggunakan F1-Score.

Out-Scope : 
- Pengembangan dan implementasi real-time dashboard atau API untuk penyebaran model. 
- Analisis sentimen dari sumber luar (media sosial, call center logs). 
- Pengembangan model prediktif untuk Lifetime Value (LTV) pelanggan. 
- Pembuatan strategy atau penawaran retensi (menjadi tanggung jawab tim Marketing).


## 3. Metrik Evaluasi Awal (SMART)

Metrik utama yang digunakan untuk menilai performa model adalah **F1-Score** pada kelas Churn (kelas positif), karena metrik ini menyeimbangkan antara Precision (keakuratan prediksi churn) dan Recall (kemampuan deteksi kasus churn berisiko tinggi).

| Metrik | Nilai | Keterangan |
| :--- | :--- | :--- |
| **Metrik Utama** | F1-Score (Kelas Churn) | Metrik yang menyeimbangkan Precision dan Recall. |
| **Baseline** | **0.61** | Hasil yang dicapai oleh model Baseline (Regresi Logistik) dari eksplorasi awal. |
| **Target** | **≥ 0.75** | Target yang ingin dicapai pada fase pemodelan lanjutan (dengan teknik seperti Random Forest atau XGBoost) untuk meningkatkan daya deteksi pelanggan berisiko tinggi. |

## 4 Etika & Privasi
Risiko & Mitigasi: 
Risiko Etika: Model klasifikasi rentan terhadap bias diskriminatif jika fitur seperti gender atau SeniorCitizen secara tidak adil memengaruhi keputusan churn atau jika penawaran retensi hanya ditargetkan pada kelompok tertentu. Risiko Privasi: Data yang digunakan (riwayat tagihan, penggunaan layanan) bersifat sensitif. Mitigasi: Kami akan anonimisasi kolom customerID di awal proses. Kami akan secara berkala melakukan audit fairness metric untuk memastikan model tidak mendiskriminasi berdasarkan fitur demografi, dan kami akan membatasi akses ke data mentah hanya pada tim proyek inti.
