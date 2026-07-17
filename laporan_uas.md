<!-- ============================================================ -->
<!-- Halaman Cover                                                 -->
<!-- ============================================================ -->

<div align="center">


# LAPORAN UJIAN AKHIR SEMESTER
## KECERDASAN BUATAN
### Prediksi Penyakit Jantung Menggunakan Algoritma Decision Tree dan K-Nearest Neighbor (KNN)

![Logo ITG](https://elearning.itg.ac.id/upload/logo/1634978306logo-putih-itg-512.png)

**Disusun oleh:**  
Moch Azriel Naufan H (2406046)  
Muhamad Thor!q Mustaq!m (2406045)




**Dosen Pengampu:**  
 Leni Fitriani, M.Kom.

**PROGRAM STUDI TEKNIK INFORMATIKA**  
**INSTITUT TEKNOLOGI GARUT**  
**2026**

</div>

---

<!-- ============================================================ -->
<!-- BAB 1: JUDUL PROYEK                                           -->
<!-- ============================================================ -->

# 1. Judul Proyek

**Prediksi Penyakit Jantung Menggunakan Algoritma Decision Tree dan K-Nearest Neighbor (KNN)**

**Domain Proyek (Latar Belakang)**

Penyakit jantung merupakan salah satu penyebab kematian tertinggi di dunia. Menurut data WHO, sekitar 17,9 juta orang meninggal setiap tahunnya akibat penyakit kardiovaskular (WHO, 2021). Deteksi dini sangat penting untuk mencegah komplikasi lebih lanjut. Namun, diagnosis penyakit jantung seringkali membutuhkan biaya mahal dan akses ke tenaga medis spesialis.

Perkembangan teknologi di bidang *machine learning* membuka peluang untuk mengembangkan sistem prediksi yang dapat membantu tenaga medis dalam mendiagnosis penyakit jantung secara lebih cepat dan akurat. Algoritma seperti Decision Tree dan K-Nearest Neighbor (KNN) terbukti efektif dalam klasifikasi data medis (Bhatt et al., 2023).

---

<!-- ============================================================ -->
<!-- BAB 2: BUSINESS UNDERSTANDING                                 -->
<!-- ============================================================ -->

# 2. Business Understanding

## 2.1 Permasalahan Dunia Nyata dan Literatur Review

Penyakit jantung seringkali terdeteksi pada stadium lanjut karena gejala yang tidak spesifik dan keterbatasan akses layanan kesehatan. Hal ini menyebabkan tingginya angka kematian akibat serangan jantung mendadak. Oleh karena itu, diperlukan sistem yang dapat memprediksi risiko penyakit jantung berdasarkan data medis sederhana seperti usia, tekanan darah, kadar kolesterol, dan riwayat kesehatan pasien.

Beberapa penelitian terdahulu telah menerapkan algoritma machine learning untuk klasifikasi penyakit jantung:

- Penelitian oleh **Bhatt et al. (2023)** menggunakan Decision Tree dan mencapai akurasi 89% dalam memprediksi penyakit jantung.
- **Ahmed et al. (2022)** membandingkan SVM, KNN, dan Logistic Regression, dan menemukan bahwa KNN memiliki akurasi tertinggi yaitu 87%.
- **Latha & Jeeva (2019)** mengkombinasikan beberapa algoritma dan menyimpulkan bahwa ensemble learning meningkatkan akurasi hingga 92%.

Berdasarkan literatur tersebut, proyek ini memilih dua algoritma yang paling sering digunakan dan memiliki performa baik: **Decision Tree** karena interpretabilitasnya yang tinggi, dan **KNN** karena kesederhanaannya dalam menangani data non-linear.

## 2.2 Tujuan Proyek

1. Mengembangkan model machine learning untuk memprediksi risiko penyakit jantung.
2. Membandingkan performa algoritma Decision Tree dan KNN.
3. Mengidentifikasi model terbaik berdasarkan metrik evaluasi (akurasi, precision, recall, F1-score).

## 2.3 User/Pengguna Sistem

- **Dokter dan Tenaga Medis:** Sebagai alat bantu diagnosis awal.
- **Pasien:** Untuk mengetahui risiko penyakit jantung secara dini.
- **Peneliti:** Sebagai dasar pengembangan sistem prediksi yang lebih canggih.

## 2.4 Solusi dan Manfaat Implementasi AI

- **Solusi:** Sistem prediksi berbasis web/aplikasi yang menerima input data medis pasien dan memberikan output berupa klasifikasi risiko penyakit jantung.
- **Manfaat:**
  - Diagnosis lebih cepat dan murah.
  - Deteksi dini penyakit jantung.
  - Membantu tenaga medis dalam pengambilan keputusan.

---

<!-- ============================================================ -->
<!-- BAB 3: DATA UNDERSTANDING                                     -->
<!-- ============================================================ -->

# 3. Data Understanding

## 3.1 Sumber Data

Dataset `heart_disease.csv` diperoleh dari **Kaggle** (Cleveland Heart Disease Dataset). Dataset ini merupakan dataset standar yang sering digunakan dalam penelitian klasifikasi penyakit jantung.

## 3.2 Deskripsi Setiap Fitur (Atribut)

| No | Fitur | Deskripsi | Tipe Data |
|----|-------|-----------|-----------|
| 1 | age | Usia pasien dalam tahun | Numerik |
| 2 | sex | Jenis kelamin (0 = Wanita, 1 = Pria) | Kategorik |
| 3 | cp | Tipe nyeri dada (0 = typical angina, 1 = atypical angina, 2 = non-anginal pain, 3 = asymptomatic) | Kategorik |
| 4 | trestbps | Tekanan darah istirahat (mm Hg) | Numerik |
| 5 | chol | Kadar kolesterol serum (mg/dl) | Numerik |
| 6 | fbs | Gula darah puasa > 120 mg/dl (0 = Tidak, 1 = Ya) | Kategorik |
| 7 | restecg | Hasil EKG istirahat (0 = normal, 1 = abnormal ST-T, 2 = hipertrofi ventrikel kiri) | Kategorik |
| 8 | thalach | Detak jantung maksimum yang dicapai | Numerik |
| 9 | exang | Angina akibat olahraga (0 = Tidak, 1 = Ya) | Kategorik |
| 10 | oldpeak | Depresi ST akibat olahraga relatif terhadap istirahat | Numerik |
| 11 | slope | Kemiringan segmen ST saat olahraga (0 = naik, 1 = datar, 2 = turun) | Kategorik |
| 12 | ca | Jumlah pembuluh darah utama yang diwarnai oleh fluoroskopi (0-3) | Numerik |
| 13 | thal | Thalassemia (0 = normal, 1 = fixed defect, 2 = reversible defect) | Kategorik |
| 14 | target | Diagnosis penyakit jantung (0 = tidak sakit, 1 = sakit) | Target |

## 3.3 Ukuran dan Format Data

- Jumlah sampel: **303** baris  
- Jumlah fitur: **13** fitur + 1 target  
- Format data: **CSV** (Comma Separated Values)

## 3.4 Tipe Data dan Target Klasifikasi

- Fitur numerik: age, trestbps, chol, thalach, oldpeak, ca  
- Fitur kategorik: sex, cp, fbs, restecg, exang, slope, thal (setelah encoding)  
- Target: **Biner** (0 = Tidak sakit, 1 = Sakit)

---

<!-- ============================================================ -->
<!-- BAB 4: EXPLORATORY DATA ANALYSIS (EDA)                       -->
<!-- ============================================================ -->

# 4. Exploratory Data Analysis (EDA)

## 4.1 Visualisasi Distribusi Data

Berikut adalah visualisasi distribusi data yang dilakukan:

### 4.1.1 Distribusi Target

![Distribusi Target](https://github.com/projectthq-itg/UAS-KecerdasanBuatan/blob/main/gambar/diagram1.png?raw=true)

Dari gambar terlihat bahwa data relatif seimbang antara kelas tidak sakit (220) dan sakit (83), meskipun terdapat ketidakseimbangan (72.6% tidak sakit vs 27.4% sakit).

### 4.1.2 Distribusi Usia

![Distribusi Usia](distribusi_usia.png)

Pasien dengan penyakit jantung cenderung berusia lebih tua (rata-rata 55-60 tahun) dibandingkan yang tidak sakit.

### 4.1.3 Distribusi Jenis Kelamin

![Distribusi Sex](distribusi_sex.png)

Mayoritas pasien adalah pria (sekitar 68%).

## 4.2 Analisis Korelasi Antar Fitur

![Heatmap Korelasi](heatmap_korelasi.png)

Dari heatmap, fitur yang berkorelasi positif tinggi dengan target adalah `ca` (0.48), `oldpeak` (0.48), `cp` (0.38), `exang` (0.36), dan `slope` (0.36). Fitur `thalach` memiliki korelasi negatif (-0.39).

## 4.3 Deteksi Data Tidak Seimbang

Data tidak seimbang dengan rasio perbedaan 0.452, sehingga perlu diperhatikan untuk menghindari bias model terhadap kelas mayoritas.

## 4.4 Insight Awal dari Pola Data

- Fitur `thalach` (detak jantung maksimum) dan `oldpeak` (depresi ST) adalah prediktor penting.
- Pasien dengan nyeri dada tipe 3 (asymptomatic) lebih banyak yang sakit.
- Tekanan darah dan kolesterol memiliki korelasi rendah dengan target.

---

<!-- ============================================================ -->
<!-- BAB 5: DATA PREPARATION                                       -->
<!-- ============================================================ -->

# 5. Data Preparation

## 5.1 Pembersihan Data

Dataset tidak memiliki nilai hilang (missing value) dan tidak ada duplikat, sehingga tidak perlu dilakukan imputasi atau penghapusan duplikat.

```python
print(df.isnull().sum())
print(df.duplicated().sum())
```

## 5.2 Encoding Data Kategorik

Kolom `thal` yang bertipe object di-encode menggunakan `LabelEncoder` menjadi numerik.

```python
from sklearn.preprocessing import LabelEncoder

for col in df.columns:
    if df[col].dtype == 'object':
        le = LabelEncoder()
        df[col] = le.fit_transform(df[col])
```

## 5.3 Normalisasi / Standardisasi Data Numerik

Semua fitur numerik distandarisasi menggunakan `StandardScaler` agar memiliki mean 0 dan standar deviasi 1, karena algoritma KNN sensitif terhadap skala.

```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)
```

## 5.4 Split Data

Data dibagi menjadi training (80%) dan testing (20%) dengan `train_test_split`.

```python
from sklearn.model_selection import train_test_split

X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```

Jumlah data training: 242 sampel, testing: 61 sampel.

---

<!-- ============================================================ -->
<!-- BAB 6: MODELING                                               -->
<!-- ============================================================ -->

# 6. Modeling

## 6.1 Pemilihan Algoritma

Dua algoritma dipilih:

1. **Decision Tree (DT)**
   - Kelebihan: Interpretabilitas tinggi, mudah divisualisasikan, tidak memerlukan normalisasi.
   - Kekurangan: Rentan overfitting jika tidak diatur kedalamannya.
   - Alasan: Cocok untuk data medis karena dokter dapat memahami logika keputusan.

2. **K-Nearest Neighbor (KNN)**
   - Kelebihan: Sederhana, efektif untuk data dengan batas keputusan non-linear.
   - Kekurangan: Lambat pada data besar, sensitif terhadap skala data.
   - Alasan: Memiliki performa baik pada dataset berukuran sedang seperti ini.

## 6.2 Implementasi Model

### 6.2.1 Decision Tree

```python
dt_model = DecisionTreeClassifier(
    random_state=42, 
    max_depth=5,
    min_samples_split=10,
    min_samples_leaf=5
)
dt_model.fit(X_train_scaled, y_train)
```

### 6.2.2 KNN

Pencarian nilai k optimal (1-15) dilakukan untuk mendapatkan performa terbaik.

```python
# Nilai k optimal = 11
knn_model = KNeighborsClassifier(n_neighbors=11)
knn_model.fit(X_train_scaled, y_train)
```

## 6.3 Perbandingan Model

| Model | Akurasi |
|-------|---------|
| Decision Tree | 80.33% |
| KNN (k=11) | **85.25%** |

KNN memberikan akurasi lebih tinggi dibandingkan Decision Tree pada dataset ini.

## 6.4 Visualisasi Model (Decision Tree)

![Decision Tree](decision_tree_visualization.png)

Pohon keputusan menunjukkan bahwa fitur `oldpeak`, `cp`, dan `thalach` menjadi node penting dalam pengambilan keputusan.

---

<!-- ============================================================ -->
<!-- BAB 7: EVALUATION                                             -->
<!-- ============================================================ -->

# 7. Evaluation

## 7.1 Confusion Matrix

### Decision Tree

| | Prediksi Tidak Sakit | Prediksi Sakit |
|---|----------------------|----------------|
| Aktual Tidak Sakit | 35 | 9 |
| Aktual Sakit | 3 | 14 |

### KNN (k=11)

| | Prediksi Tidak Sakit | Prediksi Sakit |
|---|----------------------|----------------|
| Aktual Tidak Sakit | 40 | 4 |
| Aktual Sakit | 5 | 12 |

## 7.2 Metrik Evaluasi

| Model | Accuracy | Precision (Sakit) | Recall (Sakit) | F1-Score (Sakit) |
|-------|----------|-------------------|----------------|------------------|
| Decision Tree | 0.8033 | 0.6087 | 0.8235 | 0.7000 |
| KNN | **0.8525** | **0.7500** | 0.7059 | 0.7273 |

## 7.3 Penjelasan Kinerja Model

Model **KNN** memiliki akurasi tertinggi (85.25%) dan precision yang lebih baik (0.75) dibandingkan Decision Tree. Decision Tree memiliki recall yang lebih tinggi (0.82) yang berarti lebih baik dalam menangkap kasus positif (sakit), namun precision lebih rendah, sehingga lebih banyak false positive.

KNN lebih seimbang dan memberikan performa keseluruhan yang lebih baik, sehingga dipilih sebagai model terbaik.

---

<!-- ============================================================ -->
<!-- BAB 8: KESIMPULAN DAN REKOMENDASI                             -->
<!-- ============================================================ -->

# 8. Kesimpulan dan Rekomendasi

## 8.1 Ringkasan Hasil Modeling dan Evaluasi

Proyek ini berhasil mengimplementasikan dua algoritma machine learning untuk memprediksi penyakit jantung menggunakan dataset Cleveland. Model KNN dengan k=11 mencapai akurasi 85.25%, sedangkan Decision Tree mencapai 80.33%. KNN menunjukkan performa yang lebih stabil dan unggul dalam metrik precision dan akurasi.

## 8.2 Apakah Tujuan Proyek Tercapai?

✅ **Ya**, tujuan proyek tercapai. Model yang dikembangkan mampu memprediksi risiko penyakit jantung dengan akurasi di atas 85%, yang cukup baik untuk digunakan sebagai alat bantu diagnosis awal.

## 8.3 Kelebihan dan Keterbatasan Model

| Kelebihan | Keterbatasan |
|-----------|--------------|
| Interpretabilitas tinggi (Decision Tree) | Hanya menggunakan 303 sampel data |
| Akurasi > 85% | Tidak mencakup data dari populasi yang beragam |
| Implementasi sederhana dan cepat | Belum diuji pada dataset eksternal |

## 8.4 Rekomendasi Perbaikan

1. **Dataset Lebih Besar:** Menggunakan dataset dengan ribuan sampel untuk meningkatkan generalisasi model.
2. **Algoritma Lain:** Menguji Random Forest, XGBoost, atau Neural Network untuk perbandingan lebih lanjut.
3. **Feature Engineering:** Menambahkan fitur baru seperti kombinasi rasio kolesterol/tekanan darah.
4. **Hyperparameter Tuning:** Melakukan Grid Search atau Random Search untuk optimasi parameter.
5. **Deployment:** Mengembangkan aplikasi web sederhana agar mudah digunakan oleh tenaga medis.

---

<!-- ============================================================ -->
<!-- BAB 9: REFERENSI                                              -->
<!-- ============================================================ -->

# 9. Referensi

1. Kohsasih, K. L., Sunario, D. S., Alvin, A., & Laurendio, F. (2025). Enhancing early heart disease detection through comparative analysis of random forest, decision tree, and K-NN models. *IT Journal Research and Development, 10*(2), 66–77. https://doi.org/10.25299/itjrd.2025.24703

2. Muttakin, M., Rusmana, N. R., & Ramadhani, D. (2025). Analisis perbandingan algoritma decision tree, random forest, KNN, dan SVM dalam prediksi penyakit jantung. *Journal of System & Technology (SYSTEC), 1*(2), 35–42. https://systec.ejournal.unri.ac.id/index.php/systec/article/view/18

3. Coronary heart disease prediction: A comparative study of machine learning algorithms. (2024). *Journal of Advances in Information Technology, 15*(1), 27–32. https://doi.org/10.12720/jait.15.1.27-32

4. Balhaf, K., Munassar, N. A., & Akoosh, L. M. S. (2025). Performance evaluation of machine learning algorithms for heart disease prediction using real-world data from Yemen. *2025 International Conference on Artificial Intelligence, Computer, Data Sciences and Applications (ACDSA)*, 1–7. https://doi.org/10.1109/ACDSA65407.2025.11166082

5. Regen, R., & Setiawan, H. (2024). Advancing cardiovascular risk prediction: A review of machine learning models and their clinical potential. *Journal of Electrical Technology UMY, 8*(2). https://journal.umy.ac.id/index.php/jet/article/view/25208

---

<!-- ============================================================ -->
<!-- BAB 10: LAMPIRAN                                             -->
<!-- ============================================================ -->

# 10. Lampiran

## 10.1 Dataset Mentah
- `data/heart_disease.csv` – Dataset asli yang digunakan.

## 10.2 Notebook Lengkap
- `uas_model.ipynb` – Seluruh kode dari EDA hingga evaluasi.

## 10.3 Grafik Tambahan
- `distribusi_target.png`
- `distribusi_usia.png`
- `distribusi_sex.png`
- `heatmap_korelasi.png`
- `korelasi_target.png`
- `knn_optimal_k.png`
- `perbandingan_akurasi.png`
- `confusion_matrix.png`
- `decision_tree_visualization.png`

## 10.4 Jurnal Referensi
Tersedia di folder `data/Jurnal/` (jurnal1.pdf – jurnal5.pdf).

---

<!-- ============================================================ -->
<!-- PENUTUP                                                       -->
<!-- ============================================================ -->

<div align="center">

*Laporan ini disusun sebagai tugas akhir mata kuliah Kecerdasan Buatan.*

**Disusun oleh:**  
Moch Azriel Naufan H (2406046)  
Muhamad Thor!q Mustaqim (2406045)

**Institut Teknologi Garut**  
2026

</div>
