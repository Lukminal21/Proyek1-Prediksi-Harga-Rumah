# Proyek 1: Prediksi Harga Rumah

Proyek ini merupakan bagian dari program Magang.

Fokus proyek kali ini adalah **membangun model prediksi harga rumah** menggunakan dataset dari Kaggle.

**Link Download Dataset**
https://drive.google.com/file/d/156oowXooqRr_Y2NlZTR84fDSe8pTLjyd/view?usp=sharing)

## 📋 Deskripsi Proyek
- **Dataset** : House Price Prediction Dataset  
- **Jumlah Data** : 2000 baris × 10 kolom  
- **Target** : `Price` (harga rumah dalam USD)  
- **Tujuan** : Melakukan data preparation dan baseline modeling untuk memprediksi harga rumah.

Notebook ini (`Poyek1_Prediksi_Harga_Rumah.ipynb`) terdiri dari:

1. **Import Library**
2. **Load Dataset**
3. **Dataset Audit & Exploratory Data Analysis (EDA)**  
   - Melihat bentuk data (`shape`)
   - Informasi dataset (`info()`)
   - Cek missing values
   - Cek missing value tersembunyi
   - Cek data duplikat
   - Statistik deskriptif numerik (`describe()`)
   - Statistik deskriptif kategorikal
   - Deteksi outlier pada target `Price` menggunakan IQR
   - Eksplorasi nilai unik kolom kategorikal (`value_counts`)

4. **Baseline Modeling**
   - Linear Regression
   - Random Forest Regressor
   - Evaluasi metrik (R² Score)
   - Cek overfitting (Train R² vs Test R²)

## 🔍 Temuan dari Dataset Audit
- Dataset berukuran **2000 baris × 10 kolom**
- Tidak ada **missing value**
- Tidak ada **data duplikat**
- Tidak ditemukan outlier ekstrem pada kolom `Price` menggunakan metode IQR
- Kolom kategorikal: `Location` (4 kategori), `Condition` (4 kategori), `Garage` (2 kategori)

## 📊 Hasil Baseline Modeling

**Linear Regression**  
- R² Score pada test set: **-0.0067**

**Random Forest Regressor**  
- R² Score pada test set: **-0.0984**

**Cek Overfitting:**
- Train R² : **0.0079**
- Test R²  : **-0.0081**

## 💡 Insight & Kesimpulan

- Kedua model (Linear Regression dan Random Forest) menghasilkan **R² negatif**.
- Artinya, model **tidak lebih baik** daripada sekadar memprediksi harga menggunakan nilai rata-rata saja.
- Model mengalami **underfitting** yang cukup parah.
- Fitur yang tersedia saat ini (Area, Bedrooms, Bathrooms, Floors, YearBuilt, Location, Condition, Garage) **belum cukup kuat** untuk menangkap pola harga rumah.
- Diperlukan **feature engineering** yang lebih mendalam di tahap selanjutnya.

## 🛠️ Teknologi yang Digunakan
- Python
- Pandas & NumPy
- Scikit-learn (LinearRegression, RandomForestRegressor)
- Matplotlib & Seaborn (untuk visualisasi)


**Catatan**:  
Proyek ini masih dalam tahap awal. Performa model saat ini rendah karena keterbatasan fitur. Akan dilanjutkan dengan feature engineering dan model yang lebih advanced di minggu berikutnya.
