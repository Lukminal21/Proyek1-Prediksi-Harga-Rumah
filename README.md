# Proyek 1: Prediksi Harga Rumah

**Deskripsi**  
Proyek pertama magang: Melakukan dataset audit dan data preparation (anti data leakage) untuk dataset Housing.csv (2000 baris).  
Fokus tahap ini:  
- Audit data (distribusi, outlier, korelasi, balance kategori)  
- Preparation: split → encoding → scaling  

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

**Status Proyek**  
Tahap audit & preparation selesai. Selanjutnya: modeling & evaluasi.
