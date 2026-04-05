# Proyek 1: Prediksi Harga Rumah

**Deskripsi**  
Proyek pertama magang: Melakukan dataset audit dan data preparation (anti data leakage) untuk dataset Housing.csv (2000 baris).  
Fokus tahap ini:  
- Audit data (distribusi, outlier, korelasi, balance kategori)  
- Preparation: split → encoding → scaling  

**Link Download Dataset**
https://drive.google.com/file/d/156oowXooqRr_Y2NlZTR84fDSe8pTLjyd/view?usp=sharing)

**Struktur Notebook**  
1. Dataset Audit  
2. Data Preparation  

**Hasil Utama**  
- Dataset bersih, tidak ada missing/duplikat  
- Target Price hampir simetris (skewness -0.06)  
- Korelasi tertinggi: Area vs Price (lihat heatmap)  
- Data sudah siap untuk modeling (X_train_final & X_test_final)

**Cara Menjalankan**  
1. Buka di Google Colab  
2. Upload Housing.csv ke /content/sample_data/  
3. Run cell dari atas ke bawah

## Hasil Modeling Minggu ke-2

Telah diimplementasikan dua algoritma regresi sesuai roadmap:

- **Linear Regression** (baseline)  
  MAE: 243,241.98 | RMSE: 279,859.73 | R²: -0.0067 (-0.67%)

- **Random Forest Regressor**  
  MAE: 252,671.95 | RMSE: 292,329.63 | R²: -0.0984 (-9.84%)

**Insight:**
Kedua model masih memberikan R² negatif. Ini menunjukkan bahwa hubungan antar fitur dan harga rumah belum cukup kuat ditangkap oleh model regresi standar. Korelasi linier antar fitur rendah, dan kemungkinan besar hubungannya bersifat non-linear.

**Pelajaran & Rencana Selanjutnya:**
- Perlu feature engineering lebih mendalam (contoh: umur rumah, interaksi fitur)
- Akan mencoba algoritma yang lebih kuat seperti Gradient Boosting di minggu berikutnya
- Melakukan hyperparameter tuning pada Random Forest

Proyek saat ini sudah melewati tahap audit, preparation, dan modeling awal.
